# InSTA: Towards Internet-Scale Training For Agents

![Pipeline Overview](https://data-for-agents.github.io/static/images/pipeline_overview.png)

**Brandon Trabucco (1) Gunnar Sigurdsson (2) Robinson Piramuthu (2) Ruslan Salakhutdinov (1)**

**(1) Carnegie Mellon University, Machine Learning Department (2) Amazon**

The predominant approach for training web navigation agents gathers human demonstrations for a set of popular websites and hand-written tasks, but it is becoming clear that human data are an inefficient resource. We develop a pipeline to facilitate Internet-scale training for agents without laborious human annotations. In the first stage, an LLM generates tasks for 150k diverse websites. In the next stage, LLM agents complete tasks and produce trajectories. In the final stage, an LLM reviews the trajectories and judges their success. Language models are competitive with human annotators, detecting and filtering out harmful content with an accuracy of 97%, generating feasible tasks with an 89% rate, and judging successful trajectories with an 82.6% accuracy. Scaling the pipeline, agents based on Llama 3.1 70B solve 16.7% of tasks for 150k sites. Training on the data generated by our pipeline is competitive with training on human demonstrations. In data-limited settings derived from Mind2Web and WebLINX, we improve Step Accuracy by up to +89.5% and +122.1% respectively for agents trained on mixtures of data from our pipeline, and human data. When training agents with all available human data from these benchmarks, agents fail to generalize to diverse real sites, and adding our data improves their generalization by +149.0% for WebLINX and +156.3% for Mind2Web. Code available at: [data-for-agents.github.io](https://data-for-agents.github.io).

[website](https://data-for-agents.github.io)    |    [paper](https://arxiv.org/abs/2502.06776)    |    [data](https://huggingface.co/datasets/data-for-agents/insta-150k)

## InSTA-150k Task Generation

This repository will contain the official task generation code for our paper.

### Roadmap

* today: 150k tasks released
* 3 days: web environment released
* 1 week: traces for agent actions released
* 2 weeks: second round of data collection using Llama 3.3 70B
* 4 weeks: multimodal traces released
