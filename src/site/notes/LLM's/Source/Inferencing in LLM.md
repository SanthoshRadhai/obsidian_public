---
{"dg-publish":true,"permalink":"/llm-s/source/inferencing-in-llm/","noteIcon":"","dg-note-properties":{}}
---



### KodeKloud : Understanding vLLM with a Hands On Demo [video](https://youtu.be/qdPkA5mxLhg?si=Ez0mWf2Qw-T9QeIx](https://youtu.be/qdPkA5mxLhg?si=Ez0mWf2Qw-T9QeIx))
- The above video explains what is inferencing and KV cache in LLM and how vLLM is fast and efficient in server LLM 

<iframe width="560" height="315" src="https://www.youtube.com/embed/qdPkA5mxLhg?si=j5QmyZVOei6a1V2k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


If you don't have time to watch the above video but still want to know what is inferencing continue reading......

### LLM inference

 > **LLM inference** is the process of running a pre-trained [large language model](https://www.ibm.com/think/topics/large-language-models) to generate output tokens for new input prompts, without updating the models learned parameters. During inference, the model processes the input through its transformer layers to predict the probability of possible next tokens. Then, the model generates the response one token at a time while using previously generated tokens as context. 

Read More on IBM [blog](https://www.ibm.com/think/topics/llm-inference)

![Pasted image 20261015183618.png](/img/user/LLM's/__Support/Pasted%20image%2020261015183618.png)
Figure 1.Configuration components of LLM apps. The center section contains the core configuration, including basic information, character settings, scenarios, and example dialogues. Five advanced functions (basic settings, memory, knowledge base, skills, and workflow) are distributed on both sides of the configuration area.


![Pasted image 20261015183808.png](/img/user/LLM's/__Support/Pasted%20image%2020261015183808.png)
Figure 2.Architecture of an LLM agent. The agent interacts with its environment by receiving user input and contextual signals. Perception handles multimodal inputs, which are processed in the brain for memory, reasoning, and knowledge retrieval. Actions are then produced as text, external tool usage, or embodied operations, completing the perception–cognition–action loop.

### Table 1.Representative LLM Agent Frameworks (as of Sept. 2025).

|                                                                                                           |                         |        |        |                                                                 |
| --------------------------------------------------------------------------------------------------------- | ----------------------- | ------ | ------ | --------------------------------------------------------------- |
| Framework                                                                                                 | Institution             | Launch | #Stars | Strengths                                                       |
| LangChain ([LangChain, 2022](https://arxiv.org/html/2503.04596v2#bib.bib53))                              | LangChain Inc.          | 2022   | 116k+  | Modular design, rich ecosystem, strong RAG support              |
| LangGraph ([LangChain Inc., 2024](https://arxiv.org/html/2503.04596v2#bib.bib55))                         | LangChain Inc.          | 2024   | 19k+   | Graph-based orchestration, deterministic multi-agent workflows  |
| AutoGen ([Microsoft, 2023](https://arxiv.org/html/2503.04596v2#bib.bib65))                                | Microsoft Research      | 2024   | 50k+   | Multi-agent conversations, layered architecture, AutoGen Studio |
| CrewAI ([CrewAI Inc., 2023](https://arxiv.org/html/2503.04596v2#bib.bib21))                               | CrewAI Inc.             | 2023   | 39k+   | Role-based orchestration, business-ready templates              |
| Semantic Kernel ([Microsoft Corporation, 2023](https://arxiv.org/html/2503.04596v2#bib.bib66))            | Microsoft               | 2023   | 26k+   | Deep Microsoft ecosystem integration, process orchestration     |
| LlamaIndex ([Liu, 2022](https://arxiv.org/html/2503.04596v2#bib.bib58))                                   | LlamaIndex              | 2022   | 45k+   | Strong RAG capabilities, rich data connectors, async workflows  |
| Google ADK ([Google DeepMind and Google Cloud, 2025](https://arxiv.org/html/2503.04596v2#bib.bib36))      | Google DeepMind / Cloud | 2025   | 13k+   | Gemini-native, enterprise integration, hierarchical agents      |
| OpenAI Swarm ([OpenAI, 2024](https://arxiv.org/html/2503.04596v2#bib.bib73))                              | OpenAI (experimental)   | 2024   | 20k+   | Lightweight routines, direct Python tool integration            |
| Pydantic AI ([Colvin and the Pydantic Team, 2024](https://arxiv.org/html/2503.04596v2#bib.bib20))         | Pydantic Team           | 2024   | 13k+   | Type-safe agents, durable execution, observability (Logfire)    |
| Smolagents ([Hugging Face, 2024](https://arxiv.org/html/2503.04596v2#bib.bib46))                          | Hugging Face            | 2024   | 23k+   | Minimalist “code-agents”, Hugging Face Hub integration          |
| AgentScope ([Alibaba DAMO Academy / ModelScope Team, 2024](https://arxiv.org/html/2503.04596v2#bib.bib7)) | Alibaba ModelScope      | 2024   | 13k+   | Agent-oriented programming, transparent modular design          |

>**Self-hosted** LLM services allow organizations and individuals to deploy and manage models on their own infrastructure instead of relying solely on commercial APIs. With the advent of open-source inference engines and **serving frameworks like Ollama, llama.cpp, and vLLM**, which enable the execution of models on local servers, clusters, or even edge devices, this paradigm has expanded quickly. **Self-hosting provides more control over privacy, customization, and cost than cloud-based APIs.** It also facilitates integration with domain-specific workflows and proprietary data sources. Nevertheless, it also presents significant difficulties in terms of resource management, deployment complexity, and security, necessitating both a strong system architecture and proficient operational knowledge.

![Pasted image 20261015184130.png](/img/user/LLM's/__Support/Pasted%20image%2020261015184130.png)
Figure 3.Architecture of self-hosted LLM service. The process starts from the user interface, where input queries are sent to the model serving framework. Queries may be embedded through an embedding model and stored in a vector database, which supports knowledge retrieval. The inference engine forwards requests to LLMs, runs inference, and generates outputs. Finally, results are returned to the user, completing the service pipeline.

![Pasted image 20261015184403.png](/img/user/LLM's/__Support/Pasted%20image%2020261015184403.png)
Figure 5.Three-layer architecture for the next frontier of LLM applications. The infrastructure layer provides foundational models, computing resources, communication networks, and data sources. The protocol layer coordinates interactions among agents, resources, and tools through standardized frameworks and protocols. The application layer delivers diverse application forms, where users interact with LLM-based systems for perception, planning, memory, and action.

### Table 3.Representative Agent Protocols.

|                                                                                    |                                                                       |                    |                                                      |                                                  |
| ---------------------------------------------------------------------------------- | --------------------------------------------------------------------- | ------------------ | ---------------------------------------------------- | ------------------------------------------------ |
| Entity                                                                             | Protocol                                                              | Proposer           | Key Techniques                                       | Core Problem Addressed                           |
| Context-Oriented                                                                   | MCP ([Anthropic, 2024](https://arxiv.org/html/2503.04596v2#bib.bib8)) | Anthropic          | RPC, OAuth                                           | Standardized tool invocation and context sharing |
| agent.json ([WildCardAI, 2025](https://arxiv.org/html/2503.04596v2#bib.bib106))    | WildCardAI                                                            | .well-known        | Unified agent discovery and metadata specification   |                                                  |
| Inter-Agent                                                                        | A2A ([Google, 2025](https://arxiv.org/html/2503.04596v2#bib.bib35))   | Google             | RPC, OAuth                                           | Secure peer-to-peer task delegation              |
| ANP ([Chang, 2024](https://arxiv.org/html/2503.04596v2#bib.bib15))                 | Gaowei Chang                                                          | JSON-LD, DID       | Decentralized discovery and collaboration            |                                                  |
| AITP ([Foundation, 2025](https://arxiv.org/html/2503.04596v2#bib.bib31))           | NEAR Foundation                                                       | Blockchain, HTTP   | Trustworthy interaction and transaction logging      |                                                  |
| AComP ([AI and Data, 2025a](https://arxiv.org/html/2503.04596v2#bib.bib4))         | IBM / Linux Foundation AI                                             | OpenAPI            | General-purpose communication across agents          |                                                  |
| AConP ([Cisco and LangChain, 2025](https://arxiv.org/html/2503.04596v2#bib.bib18)) | Cisco, LangChain                                                      | OpenAPI, JSON      | Standardized service integration for agent workflows |                                                  |
| ACP ([AI and Data, 2025b](https://arxiv.org/html/2503.04596v2#bib.bib5))           | IBM / Linux Foundation AI                                             | RESTful HTTP, MIME | Structured session-aware messaging and routing       |                                                  |
| Agora ([Marro et al., 2024](https://arxiv.org/html/2503.04596v2#bib.bib64))        | Oxford University                                                     | Protocol Document  | Scalable communication in large LLM networks         |                                                  |


The above pictures are copied from  

$LLM Applications: Current Paradigms and the Next Frontier$

$Xinyi Hou$
$[xinyihou@hust.edu.cn](mailto:xinyihou@hust.edu.cn)$
$Xinyi Hou and Yanjie Zhao$
$contributed equally to this work.$
$Huazhong University of Science and Technology,$
$Wuhan,$ 
$China.$

$Yanjie Zhao$
$[yanjie_zhao@hust.edu.cn](mailto:yanjie_zhao@hust.edu.cn)$
$Huazhong University of Science and Technology,$
$Wuhan,$
$China$

$Haoyu Wang$
$[haoyuwang@hust.edu.cn](mailto:haoyuwang@hust.edu.cn)$
$Haoyu Wang is the corresponding author (haoyuwang@hust.edu.cn).$
$Huazhong University of Science and Technology,$
$Wuhan,$
$China.$

Reference to Authors Paper : https://arxiv.org/html/2503.04596v2

