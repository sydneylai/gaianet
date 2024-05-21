# Boardroom Integration Specs

:::info
:bulb: This Scope of Work is is product specs that helps builders get context on integration requests.
:::

## :beginner: Product Info


- [**Boardroom**](https://www.home.boardroom.io/developers) - Governance Data for Builders and DAOs
    - Query proposals, delegates, discussions, ballots, and more with a high performance API for 350+ DAOs across chains. 

## :triangular_flag_on_post: Product Ideation

:::success
Ideas to get builders started but are not limited to the following:
:::

1. Create a Boardroom node with indexing protocol data
2. Create a Boardroom client-side app, a GPT that lives live in the forums for referencing
3. Boardroom has protocol DAO governance data API suite 
    - Can leverage data for node infrastructure, domain depolyment, and have them encourage developers to build a chatbot that could live on governance front-ends or active chats

## 📈  Scope of Work

:::success
More contextualized detail of how these products would work
:::

Here is a SOW Maintainers could help with:
- Boardroom have a massive amount of rich protocol DAO delegate data on top of onchain data
- Maintainers can build nodes for top delegates in the space using Boardroom's infra/ data
- Boardroom's current business model is selling that data back to delegates to make proper voting decisions
- Maintainers can enable agents in Farcaster, Telegram or directly in DAO governance forums powered by Boardroom

## :exclamation: Technical Requirements

:::success
Considerations as you're building
:::

**Hardware Requirements:**
* Apple M1-M3 processors or later (compatible with GaiaNet's official documentation)
* At least 16 GB of RAM

**Software Requirements:**
* GaiaNet SDK (version x.x.x) installed on the development machine
* Python 3.8 or later
* TensorFlow or PyTorch framework (optional, but recommended for custom GPT development)

**Model Development:**
* Design and develop a custom GPT model architecture using GaiaNet's APIs and SDK
* Implement training and inference functions for the GPT model
* Optimize the model for performance, scalability, and memory usage

**Integration:**
* Integrate the custom GPT model with various applications (e.g., natural language processing, chatbots, recommendation systems)
* Ensure seamless integration with GaiaNet's APIs and SDK

**Languages:** JS, TS, Go, Rust

**API Documents:** 

* Boardroom https://docs.boardroom.io/
* GaiaNet https://github.com/GaiaNet-AI

## :feet: Implementation

:::success
Implementation process describes how the review process will be conducted
:::

### :small_blue_diamond: Flow

:::warning
GaiaNet developers can support two technical reviews
:::

``` mermaid
graph TD;
Start-->Version1;
Version1-->Version2
Revision2-->Version2
Version2-->Version3
Revision3-->Version3;
Version3-->End;
```

**Testing Strategy**

Outline the approach to testing the project:

* Unit Testing: lead by open source leads
* Integration Testing: tested by integration partners
* System Testing: GaiaNet developers

### :small_blue_diamond: Example Specs

:::warning
Specs are ultimately dependent on what you decide to build
:::

| **Item**   | **Specs**   | **Note**  |
|:--------:  |:---------:  |:-------:  |
|Client-App  | Base, Arbitrum   |If built on Warpcast client|
|Governance data node           |             |     Described below      |
|            |             |           | 


**Functional Requirements**
* FR-1: The node shall efficiently crawl and index new blocks added to the [EVM compatible].
* FR-2: The node shall provide a robust query interface for searching and retrieving indexed data.
* FR-3: The node shall support filtering and sorting of search results based on specific criteria.
* FR-4: The node shall offer functionality for synchronizing with the blockchain in case of network interruptions.
* FR-5: The node shall implement mechanisms for handling high-volume data ingestion and querying.

**Non-Functional Requirements**

**Performance:**
* Indexing throughput: [Specify target block processing rate per second]
* Query response time: [Specify target response time for data retrieval]

**Scalability:**
* The node should be horizontally scalable to handle increasing data volume and query load

**Security:**
* The node shall implement secure communication protocols for data transmission
* Access to the node's functionalities should be controlled through proper authentication mechanisms (eg Chainlink, etc)
### :small_blue_diamond: Acceptance Criteria
:::warning
- The node successfully indexes and queries data from [Boardroom's API]
- The node meets performance benchmarks for indexing throughput and query response time
- The node can be deployed and scaled horizontally to handle increasing load
- All functionalities are documented and accessible through a well-defined API
:::



## 💬 Open Questions

:::success
Discuss other things that are not on the above. For example, any blind spot on our product specs?
:::

1. Open Source developers contribution will be tracked by XP
2. Developers who create 3 major product contributions will become official

### :small_blue_diamond: A checklist for stakeholders 
| Question                                        | Answer |
| ----------------------------------------------- |:------:|
| 1. What is the result you want?                 | a functioning, in-production product integration       |
| 2. Why is this result important?                |developers creating expansive functionality for other devs who need extensibility with their LLM dev tools|
| 3. How will you evaluate progress?              |progress is reviewed by core engineers and eventually developer experts|
| 4. How can you influence the result?            |Maintainers that showcase consistency in communication and contribution will be promoted in the ecosystem|
| 5. Who is responsible for the results?          |the open source developer|
| 6. How do you know you have achieved your goal? |when the product created is functional for developer adoption|
| 7. How often will you review?                   |async weekly, live-sync has 2 review cycles|