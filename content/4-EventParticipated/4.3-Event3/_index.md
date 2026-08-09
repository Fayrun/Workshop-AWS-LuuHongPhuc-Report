---
title: "Event 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---

# AWS First Cloud AI Journey — Agent Forge Deep Dive

### Purpose of the Event

- Gain in-depth, up-to-date knowledge of **Amazon Bedrock AgentCore** — AWS's dedicated platform for building and operating AI agents at production scale.
- Get a real-world perspective from an AWS expert on IT industry trends and career direction advice for students/junior engineers.
- Get hands-on practice building a simple AI agent directly during the session.

### Key Highlights

#### Opening Talk — A Perspective on the IT Industry (Mr. Hieu)

- Shared an overview of the current tech market, especially the shift toward GenAI and Agentic AI and how it's reshaping the way businesses build software.
- Gave practical advice for IT students/junior engineers: focus on building a solid foundation (understanding systems deeply, not just chasing the newest tools), while staying adaptable to how fast AI technology is moving.
- Emphasized that AI-assisted coding tools will only become more common, but problem-solving skills and truly understanding the business problem remain what separates a great engineer from an average one.

#### Amazon Bedrock AgentCore (Mr. Nghia Tran)

The core presentation of the Deep Dive, introducing the components that take AI agents from a demo to a genuinely reliable production system.

**3 core feature groups:**

- **Memory** — lets an agent retain and retrieve context across multiple interactions, instead of every exchange being an isolated session with no "memory." This is the foundation for maintaining long conversational context and personalizing the experience per user.
- **Evaluations** — a set of tools for systematically evaluating the quality of an agent's responses, helping the development team measure accuracy and usefulness, and catch cases where the agent gives incorrect or misleading answers before shipping to production.
- **Observability** — the ability to observe and trace an agent's entire reasoning/action process (each tool call, each intermediate decision), making it much easier for the operations team to debug an agent that isn't behaving as expected — similar in spirit to how CloudWatch/X-Ray monitor traditional systems, but tailored to the specific nature of agents.

**Other supporting features:** Harness (a testing/packaging framework for agents), Policy (defining behavioral constraints for an agent), Identity (managing identity and permissions when an agent acts on a user's behalf against other systems)... — these play a supporting role, rounding AgentCore out into a full lifecycle platform for building agents, from development through to safe operation.

#### Hands-on Lab — Building an Agent with Bedrock AgentCore (Mr. Hai Anh)

- Hands-on practice building a simple AI agent on top of Amazon Bedrock AgentCore, applying the Memory/Observability concepts introduced earlier directly.
- Used **Kiro** (AWS's AI-assisted coding tool) to "vibe code" — writing code mostly by describing requirements in natural language, letting the AI generate a scaffold, then refining it to fit the real requirements.
- Got to experience the full flow from idea → prompt → working code firsthand, giving a much clearer picture of how AgentCore and AI-assisted coding tools shorten agent development time compared to writing everything by hand the traditional way.

### What I Learned

- Amazon Bedrock AgentCore provides a fairly complete toolset for taking an agent from an experimental idea to a production system, instead of having to build each piece (memory, logging, quality evaluation...) separately from scratch.
- Observability and Evaluations are easy to overlook when you're new to Agentic AI, but they matter just as much as the agent's core logic — because agents behave in a much more non-deterministic way than traditional software.
- AI-assisted coding tools like Kiro can significantly cut down the time from idea to working demo, but an engineer still needs a solid understanding of the system to steer and refine it correctly.

### How I'll Apply This to My Work

- Research Amazon Bedrock AgentCore Memory and consider its potential application in future versions of the SmartDocAI RAG chatbot to improve its ability to retain conversational context across multiple turns.
- Explore Amazon Bedrock AgentCore Observability and consider its potential application in future development to improve step-by-step tracing and monitoring of more complex RAG processing flows, building upon the current CloudWatch Logs/Alarms setup.
- Evaluate Kiro as a potential development support tool for future project stages, particularly for writing tests, creating small scripts, and automating repetitive coding tasks to improve development efficiency.

### Reflections After the Event

This Deep Dive gave me a much clearer picture of the gap between "getting an AI agent demo to work" and "building an AI agent reliable enough for production" — and Amazon Bedrock AgentCore is AWS's answer to exactly that gap. Mr. Hieu's opening talk also gave me extra motivation and a more grounded perspective on career growth in this field, especially with AI technology moving so fast. The hands-on lab with Kiro was the most enjoyable part of the session, giving me a concrete sense of how AI-assisted coding can support real work, not just something I'd only read about in theory.

#### Photos from the Event

![Agent Forge Deep Dive event photo](/images/4-EventParticipated/Event-08-08-2026.jpg)
