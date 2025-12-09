---
title: "AWS Weekly Roundup: Strands Agents "
date: "2025-09-15"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

## **[AWS News Blog](https://aws.amazon.com/blogs/aws/)**

# AWS Weekly Roundup: Strands Agents 1M+ downloads, Cloud Club Captain, AI Agent Hackathon, and more (September 15, 2025)

_by [Channy Yun (윤석찬)](https://aws.amazon.com/blogs/aws/author/channy-yun/ "Posts by Channy Yun (윤석찬)") on 15 SEP 2025 in [Amazon CloudFront](https://aws.amazon.com/blogs/aws/category/networking-content-delivery/amazon-cloudfront/ "View all posts in Amazon CloudFront"), [Amazon EC2 Mac Instances](https://aws.amazon.com/blogs/aws/category/compute/amazon-ec2-mac-instances/ "View all posts in Amazon EC2 Mac Instances"), [AWS Cloud Development Kit](https://aws.amazon.com/blogs/aws/category/developer-tools/aws-cloud-development-kit/ "View all posts in AWS Cloud Development Kit"), [AWS CloudTrail](https://aws.amazon.com/blogs/aws/category/management-tools/aws-cloudtrail/ "View all posts in AWS CloudTrail"), [AWS Lambda](https://aws.amazon.com/blogs/aws/category/compute/aws-lambda/ "View all posts in AWS Lambda"), [AWS Trainium](https://aws.amazon.com/blogs/aws/category/artificial-intelligence/aws-trainium/ "View all posts in AWS Trainium"), [News](https://aws.amazon.com/blogs/aws/category/news/ "View all posts in News"), [Open Source](https://aws.amazon.com/blogs/aws/category/open-source/ "View all posts in Open Source"), [Startup](https://aws.amazon.com/blogs/aws/category/startup/ "View all posts in Startup")_

---

![](https://d2908q01vomqb2.cloudfront.net/da4b9237bacccdf19c0760cab7aec4a8359010b0/2025/09/13/2025-strands-agents-1m-download.jpg)

Last week, [Strands Agents](https://strandsagents.com/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el), AWS open source for agentic AI SDK, just hit **1 million downloads** and earned **3,000+ GitHub Stars** less than 4 months since [launching as a preview in May 2025](https://aws.amazon.com/blogs/opensource/introducing-strands-agents-1-0-production-ready-multi-agent-orchestration-made-simple/). With Strands Agents, you can build production-ready, multi-agent AI systems in a few lines of code.

We've continuously improved features including support for multi-agent patterns, A2A protocol, and Amazon Bedrock AgentCore. You can use [a collection of sample implementations](https://strandsagents.com/latest/documentation/docs/examples/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) to help you get started with building intelligent agents using Strands Agents. We always welcome your [contribution and feedback](https://github.com/strands-agents/sdk-python/blob/main/CONTRIBUTING.md) to our project including bug reports, new features, corrections, or additional documentation.

Here is the latest research article of Amazon Science about the [future of agentic AI and questions](https://www.amazon.science/blog/scientific-frontiers-of-agentic-ai?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) that scientists are asking about agent-to-agent communications, contextual understanding, common sense reasoning, and more. You can understand the technical topic of agentic AI with relatable examples, including one about our personal behaviors about leaving doors open or closed, locked or unlocked.

## Last week's Launches

Here are some launches that got my attention:

- [**Amazon EC2 M4 and M4 Pro Mac instances**](https://aws.amazon.com/blogs/aws/announcing-amazon-ec2-m4-and-m4-pro-mac-instances/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) – New M4 Mac instances offer up to **20%** better application build performance compared to M2 Mac instances, while M4 Pro Mac instances deliver up to **15%** better application build performance compared to M2 Pro Mac instances. These instances are ideal for building and testing applications for Apple platforms such as iOS, macOS, iPadOS, tvOS, watchOS, visionOS, and Safari.
- [**LocalStack integration in Visual Studio Code (VS Code)**](https://aws.amazon.com/blogs/aws/accelerate-serverless-testing-with-localstack-integration-in-vs-code-ide/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) – You can use LocalStack to locally emulate and test your serverless applications using the familiar VS Code interface without switching between tools or managing complex setup, thus simplifying your local serverless development process.
- [**AWS Cloud Development Kit (AWS CDK) Refactor (Preview)**](https://aws.amazon.com/blogs/devops/aws-cloud-development-kit-cdk-launches-refactor/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) – You can rename constructs, move resources between stacks, and reorganize CDK applications while preserving the state of deployed resources. By using [AWS CloudFormation's refactor capabilities](https://aws.amazon.com/about-aws/whats-new/2025/02/reshape-aws-cloudformation-stack-refactoring/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) with automated mapping computation, CDK Refactor eliminates the risk of unintended resource replacement during code restructuring.
- [**AWS CloudTrail MCP Server**](https://awslabs.github.io/mcp/servers/cloudtrail-mcp-server?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) – New AWS CloudTrail MCP server allows AI assistants to analyze API calls, track user activities, and perform advanced security analysis across your AWS environment through natural language interactions. You can explore more [AWS MCP servers](https://awslabs.github.io/mcp/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) for working with AWS service resources.
- [**Amazon CloudFront support for IPv6 origins**](https://aws.amazon.com/about-aws/whats-new/2025/09/amazon-cloudfront-ipv6-origins/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) – Your applications can send IPv6 traffic all the way to their origins, allowing them to meet their architectural and regulatory requirements for IPv6 adoption. End-to-end IPv6 support improves network performance for end users connecting over IPv6 networks, and also removes concerns for IPv4 address exhaustion for origin infrastructure.

For a full list of AWS announcements, be sure to keep an eye on the [What’s New with AWS?](https://aws.amazon.com/new/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) page.

## Other AWS News

Here are some additional news items that you might find interesting:

- [**A city in the palm of your hand**](https://www.aboutamazon.com/stories/ai-chips-aws-Trainium2-explain?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) – Check out this interactive feature that explains how our AWS Trainium chip designers think like city planners, optimizing every nanometer to move data at near light speed.
- [**Measuring the effectiveness of software development tools and practices**](https://www.amazon.science/blog/measuring-the-effectiveness-of-software-development-tools-and-practices?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) – Read how Amazon developers that identified specific challenges before adopting AI tools cut costs by **15.9%** year-over-year using our cost-to-serve-software framework (CTS-SW). They deployed more frequently and reduced manual interventions by **30.4%** by focusing on the right problems first.
- [**Become an AWS Cloud Club Captain**](https://builder.aws.com/content/30aH27Sct6i1eSqKOPEMzwwv3GN/become-an-aws-cloud-club-captain-applications-open?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) – Join a growing network of student cloud enthusiasts by becoming an AWS Cloud Club Captain! As a Captain, you’ll get to organize events and building cloud communities while developing leadership skills. Application window is open **September 1-28, 2025**.

## Upcoming AWS Events

Check your calendars and sign up for these upcoming AWS events as well as [AWS re:Invent](https://reinvent.awsevents.com/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) and [AWS Summits](https://aws.amazon.com/events/summits/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el):

- [**AWS AI Agent Global Hackathon**](https://info.devpost.com/blog/aws-ai-agent-global-hackathon?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) – This is your chance to dive deep into our powerful generative AI stack and create something truly awesome. From **September 8 to October 20**, you have the opportunity to create AI agents using AWS suite of AI services, competing for over **$45,000 in prizes** and exclusive go-to-market opportunities.
- [**AWS Gen AI Lofts**](https://aws.amazon.com/startups/lp/aws-gen-ai-lofts?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) – You can learn AWS AI products and services with exclusive sessions and meet industry-leading experts, and have valuable networking opportunities with investors and peers. Register in your nearest city: [Mexico City](https://aws.amazon.com/startups/lp/aws-gen-ai-loft-mexico-city?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) (September 30–October 2), [Paris](https://aws.amazon.com/startups/lp/aws-gen-ai-loft-paris?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) (October 7–21), [London](https://aws.amazon.com/startups/lp/aws-gen-ai-loft-london?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) (Oct 13–21), and [Tel Aviv](https://aws.amazon.com/startups/lp/aws-gen-ai-loft-tel-aviv?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) (November 11–19).
- [**AWS Community Days**](https://aws.amazon.com/events/community-day/?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) – Join community-led conferences that feature technical discussions, workshops, and hands-on labs led by expert AWS users and industry leaders from around the world: [Aotearoa](https://aws-community-day.nz/inperson.html) and [Poland](https://awscommunity.pl/) (September 18), [South Africa](https://www.awscommunityday.co.za/) (September 20), [Bolivia](https://www.facebook.com/awscommunitydaybolivia/) (September 20), [Portugal](https://awscommunityday.pt/) (September 27), [Germany](https://www.aws-community-day.de/) (October 7), and [Hungary](https://awscommunity.eu/) (October 16).

You can browse [all upcoming AWS events](https://aws.amazon.com/events/explore-aws-events?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el) and [AWS startup events](https://aws.amazon.com/startups/events?trk=769a1a2b-8c19-4976-9c45-b6b1226c7d20&sc_channel=el).

That’s all for this week. Check back next Monday for another Weekly Roundup!

— [Channy](https://linkedin.com/in/channy/)

---

TAGS: [Week in Review](https://aws.amazon.com/blogs/aws/tag/week-in-review/)

![Enter image alt description](/images/Blog/blog1/channyun_400x400.png)

### [Channy Yun (윤석찬)](https://aws.amazon.com/blogs/aws/author/channy-yun/ "Posts by Channy Yun (윤석찬)")

Channy is a Lead Blogger of AWS News Blog and Principal Developer Advocate for AWS Cloud. As an open web enthusiast and blogger at heart, he loves community-driven learning and sharing of technology.
