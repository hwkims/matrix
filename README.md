# Matrix Simulation: Interactive Agent-Based Environment

## Overview

This project is a web-based simulation environment inspired by "The Matrix," where users can observe and interact with AI-powered agents in a dynamic world. Agents have unique personalities, behaviors, and memories, driven by large language models (LLMs). Users can also participate directly through a player character, influencing the simulation's narrative and interacting with other agents. The simulation uses Supabase for real-time message synchronization and supports both Gemini and OpenAI LLMs.

## Features

*   **Interactive Agent Simulation:** Observe and interact with AI-powered agents as they move, talk, and exhibit unique behaviors.
*   **Player Character:** A playable character allows users to navigate the simulated world using touch or click and engage in conversations with other agents.
*   **LLM-Driven Conversations:** Agent dialogues are powered by large language models (LLMs) including Gemini and OpenAI.
*   **Real-time Messaging with Supabase:** Chat logs are synchronized across the interface using Supabase Realtime.
*   **Agent Personalities:** Each agent has unique characteristics, including:
    *   Name (from a predefined list)
    *   MBTI type (randomly generated)
    *   Money (a numeric value representing wealth)
    *   State (working or sleeping)
*   **Dynamic Environment:** Agents move around the simulation map, with realistic conversation ranges, behaviors, and reaction time.
*  **Selectable LLM:** User can select the LLM (Gemini, GPT, or Random) to interact with agents
*  **User-Friendly UI:** A UI designed for user interaction, including input fields for API keys, real-time conversation window and character information.

## Technologies Used

*   **HTML, CSS, JavaScript:** Front-end development and simulation logic.
*   **Supabase:** Realtime database and backend service for managing chat logs.
*   **Google Gemini API & OpenAI API:** Large language models used for powering agent conversations.
*   **HTML5 Canvas:**  Used for rendering the simulation environment and representing agent locations.

## Setup

1.  **Supabase Project:**
    *   Create a Supabase project and note down the project URL and anon key.
    *   Enable Realtime functionality.
    *   Create a `messages` table with the following columns:
        *   `sender` (TEXT, not null)
        *   `text` (TEXT, not null)
        *   `timestamp` (TIMESTAMP WITH TIME ZONE, not null)
2.  **API Keys:**
    *   Obtain Google Gemini or OpenAI API keys for Large Language Models
3.  **Download:** Download `index.html` and `bg.png` and `1.png` ~ `10.png` and `player.png` to the same local directory.
4.  **Configure `index.html`:**
    *  Replace  `'YOUR_SUPABASE_URL'` and `'YOUR_SUPABASE_ANON_KEY'` with your Supabase URL and anon key.
5.  **Run:** Open `index.html` in your web browser.
6.  **API Keys:** Enter Gemini or GPT API keys in the input fields provided.
7.  **Interact:** Click on the canvas to move the player character and type messages to interact with agents.

## Usage

*   **API Key Input:** Enter your Gemini or GPT API key in the respective input box on the top right corner.
*   **LLM Selection:** Select desired LLM from the dropdown. (Gemini, GPT, Random)
*   **Player Movement:** Use touch or click on the canvas to move the player character.
*   **Agent Interaction:** The player character can initiate and continue conversations by clicking on the map, where the closest agent will respond.
*   **Chatting with Agents:** Send messages through the input box at the bottom right corner, and they will be sent to the agents that the player is near.
*  **Agent Interactions:** Watch as agents move around the environment, engage in conversations among themselves based on proximity and availability.
*   **Dynamic Simulation:** Simulation will update dynamically, with agents reacting to events and engaging in a simulated reality.

## Notes

*   Ensure that `bg.png`, `1.png` to `10.png` and `player.png` are in the same directory as `index.html`.
*   This application works best with valid API Keys, and with Supabase setup.
*   Due to potential limitations of browser-based API calls, this application may not always perform optimally
*   If the LLM you select or have set as random has not been configured, the simulation will default to use Gemini.

## Contributing

Contributions are welcome! Please feel free to fork the repository, make improvements, and submit pull requests.

## License

This project is licensed under the [MIT License](LICENSE) (If you have a LICENSE.md file, replace this with actual link to the license, else you can remove this)
