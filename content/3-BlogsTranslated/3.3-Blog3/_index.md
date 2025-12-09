---
title: "Blog 3: Strands Agents and the Model-Driven Approach"
date: "2025-09-20"
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

## **[AWS Open Source Blog](https://aws.amazon.com/blogs/opensource/)**

# Strands Agents and the Model-Driven Approach

by Arron Bailiss on 12 SEP 2025 in[ ](https://aws.amazon.com/blogs/opensource/category/artificial-intelligence/)[Artificial Intelligence](https://aws.amazon.com/blogs/opensource/category/artificial-intelligence/),[ ](https://aws.amazon.com/blogs/opensource/category/open-source/)[Open Source](https://aws.amazon.com/blogs/opensource/category/open-source/),[ ](https://aws.amazon.com/blogs/opensource/category/post-types/technical-how-to/)[Technical How-To](https://aws.amazon.com/blogs/opensource/category/post-types/technical-how-to/)[ ](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/)[Permalink](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/)[ ](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/#Comments)[Comments](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/#Comments)[ ](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/#)[Share](https://aws.amazon.com/blogs/opensource/strands-agents-and-the-model-driven-approach/#)

Until recently, building AI agents meant wrestling with complex orchestration frameworks. Developers wrote intricate state machines, pre-defined workflows, and extensive error-handling code to shepherd language models through multi-step tasks. We needed to construct complex decision trees to handle cases of “what if the API call fails?” or “what if the user asks something unexpected?” Despite the effort, agents would break when they encountered unforeseen situations.

The Strands Agents SDK adopts a **model-driven approach** that eliminates this fragility entirely. Instead of trying to anticipate and program for every possible scenario, we let modern large language models self-steer their behavior, making intelligent decisions about tool usage and adapting flexibly to whatever happens. This approach is more durable, with better resilience because it allows models to reason about problems dynamically. When an API call fails, the model doesn’t crash – it reasons about alternatives. When a user asks something unexpected, the model doesn’t follow a pre-defined “I don’t understand” path – it figures out how to help, using the available tools. The model’s reasoning capability handles edge cases better than any state machine we could write.

The model-driven approach comes from the real-world experience of AWS teams building production agents for[ ](https://kiro.dev/)[Kiro](https://kiro.dev/),[ ](https://aws.amazon.com/q/developer/)[Amazon Q Developer](https://aws.amazon.com/q/developer/), and[ ](https://aws.amazon.com/glue/)[AWS Glue](https://aws.amazon.com/glue/). What we discovered fundamentally changed how we thought about agent architecture: the orchestration frameworks we previously built to guide models were now getting in the way of what modern LLMs could do naturally.

However, using the model as the orchestrator doesn’t mean sacrificing developer control. Strands offers a clean, simple interface that gets you started in minutes, while providing powerful configurability for when you need it. Integrated evaluation tools help you understand and validate the agent’s behavior, ensuring you maintain confidence even as the models make autonomous decisions. This balance of simplicity and flexibility is what makes the model-driven approach practical for both rapid prototyping and production systems. Strands grows with you.

In this post, we’ll explore how the model-driven approach emerged from real-world production experience and show you practical patterns for building agents that can think for themselves.

## **When orchestration becomes a constraint**

Traditional agent frameworks emerged when language models needed a lot of hand-holding. Developers built complex state machines, pre-defined workflows, and intricate coordination logic because the models couldn’t reliably reason about their next steps. We would write hundreds of lines of code just to handle the flow between “gather information,” “analyze data,” and “provide response” – and still end up with agents that broke when users asked questions in unexpected ways.

The AWS teams I worked with to build Amazon Q Developer experienced this directly. Initially, we used traditional orchestration frameworks, but changes in product requirements and user behavior required significant scientific and engineering effort to calibrate the system to handle new use cases. Machine learning (ML) routers and classifiers would return brittle outputs for guardrails – static text like “I’m sorry, I cannot answer that question” – without offering alternatives or explanations in a way that was interactively helpful and appeared intelligent.

**Modern models are sophisticated enough to orchestrate themselves.** This was the critical insight that changed everything for us. While structured workflows still have their place – especially for compliance requirements or well-defined business processes – the model-driven approach eliminates the need for rigid orchestration in most scenarios.

When the Q Developer teams transitioned to the model-driven approach, the system could flexibly handle changing product requirements and respond coherently no matter what happened. Instead of brittle guardrail responses, the agent could offer alternatives and use the guardrail’s output as context for the model to understand why it couldn’t answer certain inputs. This allowed for a single personality and tone across multi-agent systems, enabling engineers across Amazon to contribute their domain expertise while maintaining coherence. It also provided the right context to the model at the right time with powerful tools for helpful, intelligent responses.

When you give a model tools, it doesn’t just mechanically execute them. It reasons about the best approach, considers multiple strategies, and adjusts its behavior based on what it discovers. A model analyzing a performance issue might start with system metrics, realize the true bottleneck is in the database, pivot to query analysis, and then propose both immediate fixes and long-term architectural improvements – all without being explicitly programmed for that sequence.

The operational benefits were transformative. What previously took months of development now took weeks. Our teams could rapidly leverage the latest Large Language Model (LLM) features like tool calling, expansive and interleaved thinking, multi-agent systems, meta agents,[ ](https://modelcontextprotocol.io/docs/getting-started/intro)[MCP](https://modelcontextprotocol.io/docs/getting-started/intro), and[ ](https://a2a-protocol.org/latest/)[A2A](https://a2a-protocol.org/latest/) – all while keeping a simple developer interface that could be fully customized for deploying AI agents in production.

This philosophy extends beyond single agents. Whether you’re building a simple data analysis agent or a complex multi-agent system, the model decides when to collaborate with other agents, when to delegate tasks, when to dive deeper into a problem, and when to provide a final answer.

## **The agent loop: Where intelligence meets action**

The heart of this philosophy is the [agent loop](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/agents/agent-loop/) – a natural cycle of reasoning and action that mirrors how intelligent systems think and work. This approach builds on the ReAct pattern ([ReAct: Synergizing Reasoning and Acting in Language Models](https://react-lm.github.io/)), which demonstrated how language models could generate both reasoning traces and task-specific actions in an interleaved manner, creating a greater synergy between thinking and acting.

The model engages in a continuous reasoning process, asking questions like:

- _"What am I trying to achieve here?"_

- _"What information do I need?"_

- _"Which tool will be most effective?"_

- _"How do these results change my understanding?"_

- _"Should I continue exploring or provide an answer?"_

This internal reasoning process is what makes model-driven agents powerful. They aren't just executing pre-defined steps – they are thinking, adapting, and evolving their approach in real-time.

## **Guiding intelligence through context**

While the model self-steers its behavior, that behavior is shaped by the context it receives. In the model-driven approach, you guide the agent’s intelligence not through rigid control structures, but through carefully constructed context that includes system prompts, tool specifications, and conversation history.

Think of it like hiring a skilled consultant. You don't micromanage their every step – instead, you give them clear objectives, explain what resources are available, and provide relevant background information. The model-driven approach works the same way.

[System prompts](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/agents/prompts/) establish the agent’s role and objectives – they set the foundational identity and high-level goals that guide every decision-making process. Instead of dictating concrete steps, effective system prompts describe what success looks like and provide principles for decision-making. Instead of “First check the database, then validate input, then process the request,” you might write “You efficiently and accurately help users analyze their data, always validating input before processing.”

[Tool specifications](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/tools/tools_overview/) define the boundaries of capability and guide usage – they communicate not just which tools are available, but how and when they should be used. Well-designed tool descriptions become part of the model’s reasoning process. A tool description like “Use this tool for complex mathematical calculations that require high precision” helps the model appropriately choose between a calculator tool and writing Python code.

[Conversation history](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/agents/conversation-management/) maintains task continuity and evolving context – it provides the specific details that enable agents to maintain coherence across interactions. As conversations get longer, this context management becomes critical to maintaining performance while retaining relevant information. Context management is critical for model-driven agents – it is the difference between an agent that maintains coherent, intelligent conversations and one that loses track of crucial details or hits token limits. Strands provides a simple interface that allows developers to define the agent’s system prompts, tools, and context management behavior without getting lost in the complexity of implementation.

Sliding window approaches retain recent messages and discard older ones: simple and effective. Summarization techniques retain critical information from longer conversations within token limits – better for complex, evolving discussions. The goal is to provide the model with the most relevant context to make good decisions for your specific use case.

This represents a major shift from procedural programming to contextual programming. Instead of writing “if this, then that” logic, you are creating the context that helps the model figure out the best approach on its own.

from strands import Agent

from strands_tools import calculator, file_write, python_repl

Simple: Get started in seconds
agent = Agent(

    tools=[calculator, file_write, python_repl],

    system_prompt="You are a helpful assistant that can perform calculations and verify them with code."

)

The model autonomously decides: calculate first, then verify with code
agent("Calculate the compound interest on $10,000 at 5% annually for 10 years")

This design philosophy is carried throughout Strands. You can build complex agents without getting lost in configuration, yet every aspect remains customizable when your use case demands it.

## **Scaling model-driven agents with Strands**

The model-driven approach scales naturally while maintaining a clean developer experience. A single agent equipped with the right tools can handle complex tasks that would traditionally require multiple specialized components. When you do need multiple agents, the models coordinate themselves through several proven patterns. Strands offers four primary approaches for multi-agent coordination, each suited for different use cases:

- **Agents-as-Tools:** Hierarchical systems where specialists act as intelligent tools

- **Swarms:** Autonomous collaboration with self-organizing groups of agents

- **Graphs:** Structured workflows with defined execution paths

- **Meta-Agents:** Dynamic agents that can modify their own coordination behavior

Whether you are building simple hierarchies or complex adaptive systems, Strands keeps the interface clean while providing the configurability needed for production systems.

## **Agents-as-Tools: Hierarchical Intelligence**

When a single agent needs specialized expertise, [agents-as-tools](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/multi-agent/agents-as-tools/) turn other agents into intelligent tools. This creates natural hierarchies where an orchestrator agent delegates to specialists, maintaining a clear separation of responsibility while leveraging the model-driven approach at every level. How does the orchestrator agent decide which specialist to consult? The model reasons about the request the same way it reasons about tool selection. When a user asks “Plan a business trip to Tokyo and research market opportunities there,” the orchestrator recognizes that this requires both travel planning and market research expertise. It might consult the travel advisor first to understand the logistics, and then use those constraints to guide the research analyst’s work.

from strands import Agent, tool

@tool

def research_analyst(request: str) -> str:

    """Research specialist for market analysis"""

    research_agent = Agent(

        system_prompt="You are a research specialist who gathers and analyzes market information.",

        tools=[web_search, calculator]

    )

    return str(research_agent(request))

@tool

def travel_advisor(request: str) -> str:

    """Travel planning specialist for logistics and recommendations"""

    travel_agent = Agent(

        system_prompt="You are a travel planning specialist who helps with logistics, bookings, and recommendations.",

        tools=[flight_search, hotel_search, weather_api]

    )

    return str(travel_agent(request))

Orchestrator decides when to consult specialists and how to synthesize their input
executive_assistant = Agent(

    system_prompt="You coordinate with specialists to provide comprehensive assistance.",

    tools=[research_analyst, travel_advisor]

)

The orchestrator model decides which specialists to consult and how to synthesize their input – no pre-defined workflow is needed. This pattern works well when you need clear boundaries of expertise and want the models to delegate with a leading primary agent.

## **Swarms: Autonomous Collaboration**

[Swarms](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/multi-agent/swarm/) allow agents to collaborate autonomously in a self-organizing way, deciding when to hand off tasks to one another. This works well for creative collaboration and emergent problem-solving, where multiple perspectives add value.

Consider a market research project where you need to analyze a new product opportunity. A traditional method might follow a rigid sequence: research → analyze → write. But real research is messier – you might discover during analysis that you need supplementary data, or realize while writing that a different analytical framework would be more compelling.

from strands import Agent

from strands.multiagent import Swarm

researcher = Agent(name="researcher", system_prompt="You research topics thoroughly...")

analyst = Agent(name="analyst", system_prompt="You analyze data and create insights...")

writer = Agent(name="writer", system_prompt="You write comprehensive reports...")

Agents coordinate autonomously through model-driven handoffs
market_research_team = Swarm([researcher, analyst, writer])

In a swarm, the researcher might start gathering information, then hand off to the analyst when they’ve found interesting patterns. The analyst might spot gaps and hand back to the researcher for more specific data. The writer might join the conversation early to help shape the research direction based on what will make a compelling story.

The key difference from agents-as-tools is shared context. In hierarchies, the orchestrator decides what information is passed between specialists. In swarms, all agents have access to the same conversation history, allowing for more fluid collaboration and high-level instructions. You can tell a swarm “research this market opportunity” without specifying exactly how the work should be divided – the agents figure it out themselves based on their shared understanding of the evolving task.

Swarms trade predictable execution for emergent capabilities, making them ideal for complex research tasks, brainstorming sessions, and creative projects where the best approach isn't clear at the outset.

## **Graphs: Structured Workflows**

[Graphs](https://strandsagents.com/latest/documentation/docs/user-guide/concepts/multi-agent/graph/) provide defined workflows where execution follows pre-determined paths. While the individual agents within a graph use model-driven execution, the graph structure ensures specific sequences and dependencies are maintained.

This pattern excels for business processes that require mandatory checkpoints or compliance requirements. For instance, a financial analysis process might require research → risk assessment → regulatory review → final proposal, with each step building on the last and some steps requiring specific sign-offs.

from strands import Agent

from strands.multiagent import GraphBuilder

builder = GraphBuilder()

builder.add_node(researcher, "research")

builder.add_node(analyst, "analysis")

builder.add_node(writer, "report")

builder.add_edge("research", "analysis")

builder.add_edge("analysis", "report")

graph = builder.build()

AWS teams have used graphs to orchestrate data pipelines, where certain transformations must happen in sequence, and for compliance processes, where audit trails require specific step-by-step documentation. The model-driven approach still applies within each node – the research agent can adjust its methodology based on what it discovers – but the overall flow remains predictable.

The trade-off for graphs is their rigidity. If the analyst discovers they need supplementary research, they cannot directly request it – the workflow would need to complete and potentially restart. This makes graphs ideal for well-understood processes but less suited for exploratory or creative work.

## **Meta-Agents: Flexible Coordination**

Meta-agents are single agents equipped with tools that allow them to think about thinking – they can dynamically generate other agents, orchestrate workflows, and engage in recursive problem-solving. They represent the ultimate expression of the model-driven approach: agents that can self-architect their own coordination techniques.

Think of a meta-agent as a senior architect who can not only solve a problem but also decide how to structure the problem-solving approach. When faced with a complex challenge, it might reason: “This requires both deep research and creative synthesis. I should generate a swarm of specialists and then use a graph to ensure the final deliverable meets quality standards.”

from strands import Agent

from strands_tools import graph, swarm, use_agent, think, workflow

meta_agent = Agent(

    system_prompt="You can dynamically create specialized agents and orchestrate complex workflows.",

    tools=[graph, swarm, use_agent, think, workflow]

)

Meta-agents excel in dynamic systems that evolve over time. The key benefit is their added layer of dynamism – they can generate agents that weren’t pre-defined, evolve new tools for emergent needs, adapt their coordination strategies based on changing conditions, and evolve their problem-solving approach as they learn more about the domain.

Unlike the other patterns where you pre-define agents and tools, meta-agents can create new specialists and custom-build tools on demand. Analyzing a new technology trend? The meta-agent can generate domain-specialist agents for legal implications, market dynamics, and technical feasibility – agents that didn’t exist until that specific need arose. It can also evolve specialized tools for data harvesting, analytical frameworks, or report formats tailored to that specific domain.

This dynamic agent and tool creation allows systems to grow and adapt rather than follow fixed patterns.

## **Building confidence through evaluation**

The model-driven approach requires robust [evaluation](https://strandsagents.com/latest/documentation/docs/user-guide/observability-evaluation/evaluation/) to build confidence that agents are performing as expected, especially as they are making autonomous decisions about tool usage and task coordination.

Since model-driven agents make dynamic decisions instead of following pre-determined paths, evaluation becomes both more critical and more nuanced. You need to assess not just whether the agent got the right answer, but whether it made good decisions about how to approach the problem.

The model-driven approach has changed how we think about evaluation itself. Traditional testing with static datasets becomes insufficient when agents flexibly adjust their behavior. This shift demands new evaluation patterns that match the intelligence of the systems being tested.

**LLM judges** provide a powerful method for evaluating agent responses at scale, but they must be carefully calibrated to align with end-user expectations. An LLM judge that prioritizes technical accuracy may overlook nuances that matter to real users, such as tone, helpfulness, or practical applicability.

**LLM-driven simulated users** allow for dynamic testing with evolving datasets, generating realistic interaction patterns that static test cases cannot capture. However, these simulated users must also be calibrated to behave like genuine end-users instead of idealized test scripts. The goal is authentic user behavior, not perfect user behavior.

Key evaluation aspects for model-driven agents include:

- **Tool choice appropriateness** – Did the agent select the right tool for the job?

- **Reasoning quality** – Was the agent’s approach logical?

- **Adaptability** – How well did the agent handle unexpected situations?

- **Efficiency** – Did the agent complete the task without unnecessary steps?

The non-deterministic nature of model-driven agents means you need statistically meaningful baselines and continuous evaluation to track performance over time. This investment in evaluation allows you to confidently deploy agents that make autonomous decisions.

## **The paradigm shift: From rigid control to dynamic adaptation**

The model-driven approach represents a fundamental shift in how we think about AI agents. Instead of trying to control every facet of agent behavior through complex orchestration, we provide the right tools, context, and goals, and then let the model dynamically determine the best approach on its own.

This shift solves a core problem: pre-defined logic struggles to handle an unpredictable world. Traditional frameworks break when users ask questions in unexpected ways, when APIs return unforeseen responses, or when business requirements change. They fail because they can only handle the situations developers anticipated and programmed.

Model-driven agents can adapt. When an API call fails, they reason about alternatives. When a user asks something unexpected, they figure out how to help using the available tools. When requirements change, they adjust their approach without code changes. This adaptability comes from leveraging the model’s reasoning capabilities instead of fighting against them.

The approach adopted in Strands allows agents to handle shifting demands and data while reducing the complexity developers need to manage. You can have both: the simplicity to get started fast and the power to configure everything when production demands it.

The model-driven approach is not about building better orchestration frameworks. It’s about realizing that modern LLMs have evolved beyond the need for such rigid guidance. By leveraging the model’s reasoning to orchestrate, we can build agents that are both more capable and easier to develop. This philosophy is the foundation on which everything else in Strands is built. Visit the [Strands Agents](https://strandsagents.com/latest/) website to try it today.

_Looking for more open source content? Be sure to follow [AWS Open Source](https://www.linkedin.com/company/awsopen/posts/?feedView=all) on LinkedIn!_

![Enter image alt description](/images/Blog/blog3/E015GUGD2V6-W0187GVFRG8-98d371d2068f-512.jpg)

### **Arron Bailiss**

Arron Bailiss is a Principal Engineer focused on AI agents at AWS, working at the intersection of artificial intelligence, machine learning, and robotics. He helps shape the future of developer tooling that empowers builders to create complex AI-driven applications.
