# stance_event_forecsating

This project introduce a multi-stance agent for complex event forecasting.

>Q1: The novelty of the proposed method, a variant of improving CoT by using LLMs?

**1.Autonomous agent creation:**:

First, using a text embedding model, we cluster the questions into several clusters. Then a large language model analyzes the participants and roles related to each cluster and creates agents. Each agent contains a specific name, type, description and memory module. The memory module includes experience memory and historical memory. Experience memory refers to the experience from self-reflection on historical samples. Historical memory refers to the historcial forecasting results including the reasoning and answers. 

**2.Mutil-stance forecasting:**

Given a question, our agent retrieves multiple related agents from the agent collections. Then, each agent generates searching queries based on its own identity, retrieves news (using **Newscatcherapi** https://www.newscatcherapi.com/.) and videos from news websites and youtube, and makes forecasting based on the web information.

**3.Stance aggregation:**
We combine the analysis of multiple agents into several clusters based on their stances. Each cluster aggregate the analysis from multiple agents into a more comprehensive forecasting.

**4.Stance debating:**
We design a super agent that collects the analysis from the previous step, evaluates the credibility of analysis from different stances, and gives a final prediction.

