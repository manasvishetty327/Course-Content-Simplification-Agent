# CLARIFI – Course Content Simplification Agent

CLARIFI is an AI agent prototype designed to turn complex academic and technical material into clearer, more accessible explanations. The project is implemented as an IBM watsonx.ai Agent Lab notebook using a LangGraph agent and an IBM Granite foundation model.

## What It Is Designed to Do

The agent instructions focus on helping learners understand academic content by:

- Identifying the main ideas and key concepts in supplied material.
- Rewriting technical language in simpler terms while preserving meaning.
- Organising explanations with headings, bullet points, and short sections.
- Adapting the depth of an explanation to the learner's level.
- Supporting alternative learning formats such as summaries, step-by-step explanations, FAQs, and glossaries.
- Encouraging responsible paraphrasing and attribution.

These are the agent's configured goals. Actual output quality depends on the input, model response, connected tools, and IBM Cloud environment.

## Implementation

The notebook uses:

- **IBM watsonx.ai** for foundation-model inference.
- **IBM Granite 3.3 8B Instruct** as the configured chat model.
- **LangGraph** to create and invoke the tool-using agent.
- **LangChain IBM integration** to connect to watsonx.ai.
- **IBM Agent Lab utility tools** configured in the notebook, including Google Search, DuckDuckGo, Wikipedia, WebCrawler, Weather, and Tavily Search.
- **Python** for the agent setup and invocation flow.

The notebook requests an IBM Cloud API key at runtime and reads the watsonx project or space identifier from the environment.

## Repository Contents

- [`clarifi_agent.ipynb`](./clarifi_agent.ipynb) — agent setup, model configuration, tool integration, instructions, and invocation example.
- [Agent Preview](./Agent%20Preview.png) — preview image.
- [Agent Response](./Agent%20Response.png) — example response image.
- [Deployed Agent](./deployed%20Agent.png) — deployment screenshot.
- [Results PDF](./COURSE%20CONTENT%20SIMPLIFICATION%20AGENT%20RESULTS.pdf) — project output and results.
- [Project presentation](./course%20content%20simplification%20agent%20ppt.pdf) — project overview.

## Running the Notebook

This repository contains an IBM watsonx.ai Agent Lab notebook rather than a standalone web application.

1. Open IBM watsonx.ai and create or select a project or space with the required foundation-model and Agent Lab access.
2. Import `clarifi_agent.ipynb` into the notebook environment.
3. Provide your IBM Cloud API key when prompted.
4. Configure the required project or space context and ensure the notebook's utility tools are available.
5. Run the notebook cells in order and enter a question or academic-content prompt when requested.

The notebook uses IBM-hosted services and configured utility tools. It is not an offline or locally runnable agent.

## Configuration and Security

- Never add IBM Cloud API keys or other credentials to the notebook.
- The notebook expects project or space configuration to be available in the execution environment.
- External utility tools may require service access, configuration, or their own credentials.
- Deployment screenshots and notebook configuration do not guarantee that a hosted endpoint is still active.

## Scope and Limitations

CLARIFI is an educational agent prototype. It is intended to assist with understanding and summarising learning material, not to replace original sources, instructors, or academic judgement. Generated explanations should be checked for accuracy, and source material should be cited appropriately.

## Author

**Manasvi Shetty**
