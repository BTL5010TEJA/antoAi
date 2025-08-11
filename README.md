# antoAi
Developed an AI-powered chatbot using AntoAI, enabling real-time, context-aware conversations. Integrated NLP for understanding queries, automated responses, and multi-platform deployment, improving user engagement, support efficiency, and response accuracy.
Screenshots of project:
<img width="1888" height="764" alt="Screenshot 2025-08-09 222011" src="https://github.com/user-attachments/assets/66992bfd-45c4-486a-9276-cb1c3f9b6a38" />
<img width="1917" height="790" alt="Screenshot 2025-08-09 221928" src="https://github.com/user-attachments/assets/8365ce98-50d4-4776-b5bf-af20d6067a84" />
The screenshots show the development of an AI chatbot using a **no-code/low-code platform, specifically n8n**. The project's name appears to be "antoAi," and the workflow is called "My workflow 2."

***

### Project Explanation

The goal of this project is to create an **AI Agent** that can have a conversation with a user. Instead of writing code from scratch, the developer is building the chatbot's logic using n8n's visual workflow builder. This approach allows for rapid development and easy management of the conversational flow.

The chatbot is being built to handle a specific problem, likely a mathematical or logical one, as suggested by the "Constraints and Approximations" and "We think of states as (a, b) ..." notes. It appears to be a problem involving probabilities or resource management (the "soup" example).

***

### Working of the AI Agent

The AI agent works by connecting several nodes in a workflow to create a chain of operations. Here's a breakdown of the visible components and their functions:

* **When chat message received:** This is the **trigger** node. It initiates the workflow every time a user sends a message to the chatbot. It acts as the entry point for the conversation.
* **AI Agent:** This is the core of the chatbot. It's a high-level node that orchestrates the entire conversational process. It's configured to use other nodes for its functionality, such as a language model and a memory component.
* **OpenAI Chat Model:** This node is a connection to the **OpenAI API**, which provides the large language model (LLM) that powers the AI's intelligence. It's responsible for processing the user's message, understanding the context, and generating a coherent and relevant response. The editor view shows specific instructions being given to this model, including a prompt about a "soup" problem and a crucial `formatting_instructions` block. This block tells the AI to format its final response in a specific way (likely JSON), which is a common practice for ensuring the output is machine-readable for subsequent steps in a workflow.
* **Simple Memory:** This node serves as the **memory** for the chatbot. It stores the history of the conversation, allowing the AI to maintain context. Without this, the AI would treat every message as a new, unrelated query. The simple memory node ensures that the AI agent can have a continuous, context-aware conversation.
* **Editor/Execution/Evaluations Tabs:** These tabs provide different views for managing the workflow.
    * **Editor:** The visual canvas for building the workflow.     * **Executions:** This tab (not shown in detail) would display a log of every time the workflow was run, including any errors or successful completions.
    * **Evaluations:** This tab is likely for testing and refining the AI's responses, allowing the developer to evaluate how well the model is performing against specific prompts.
* **Chat Window:** The chat window within the editor allows the developer to **test the chatbot in real time**. The notes on the left ("Constraints and Approximations") likely represent the problem's logic that the developer is trying to implement or debug while interacting with the AI agent.
