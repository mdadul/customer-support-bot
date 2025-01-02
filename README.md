# Customer Support Chatbot with a Small Model

This project implements a customer support chatbot using a small language model. The chatbot can handle initial support, billing support, and technical support, and can route users to the appropriate team based on their queries.
![image](https://github.com/user-attachments/assets/64dce739-e090-49ad-adec-cd6a01c5cb39)

## Project Structure

- `agent.ts`: The main TypeScript file that contains the chatbot implementation.
- `package.json`: Contains the project dependencies and scripts.
- `tsconfig.json`: TypeScript configuration file.
- `.gitignore`: Specifies files and directories to be ignored by Git.
- `.env`: Environment variables file (ignored by Git).
- `README.md`: Project documentation (this file).

## Dependencies

The project uses the following dependencies:

- `@langchain/community`: Provides the `ChatTogetherAI` model.
- `@langchain/core`: Core utilities for the LangChain framework.
- `@langchain/langgraph`: Provides annotations, memory savers, and state graph utilities.
- `@langchain/openai`: OpenAI integration for LangChain.
- `zod`: TypeScript-first schema declaration and validation library.
- `zod-to-json-schema`: Converts Zod schemas to JSON schemas.

## Setup

1. Clone the repository:
   ```sh
   git clone git@github.com:mdadul/customer-support-bot.git
   cd customer-support-bot
   ```
2. Install dependencies:

    ```sh
    bun install
    ```
3. Create a `.env` file with the necessary environment variables 
```
TOGETHER_AI_API_KEY
```

## Usage
To run the chatbot, execute the following command:

```
    bun run agent.ts
```

The chatbot will start a command-line interface (CLI) where you can interact with it. Type your queries and the chatbot will respond accordingly. To stop the chatbot, type stop.

## Implementation Details
The chatbot is implemented using a state graph with the following nodes:

* `initial_support`: Handles initial support queries and routes users to billing or technical support.
* `billing_support`: Handles billing support queries and can authorize refunds.
* `technical_support`: Handles technical support queries.
* `handle_refund`: Processes refunds if authorized.

The chatbot uses the `Meta-Llama-3.1-8B-Instruct-Turbo` model to generate responses. It also uses Zod schemas to validate the structure of the responses.


## Contributing
If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Make your changes and commit them with descriptive messages.
4. Push your changes to your fork.
5. Create a pull request to the main repository.
