## Project Workflow

- Identify data set and use case
- ETL feature creation
- model definition and training
- model evaluation and tuning, deployment, documentation

The following figure represents a high level overview of different components in a production level deep learning system:

![ML products](infra_tooling.png)

## 1. Data Management
### 1.1 Data Sources
* Supervised deep learning requires a lot of labeled data
* Labeling own data is costly!
* Here are some resources for data:
  * Open source data (good to start with, but not an advantage)
  * Data augmentation (a MUST for computer vision, an option for NLP)
  * Synthetic data (almost always worth starting with, esp. in NLP)
### 1.2  Data Labeling
* Requires: separate software stack (labeling platforms), temporary labor, and QC
* Sources of labor for labeling:
  * Crowdsourcing (Mechanical Turk): cheap and scalable, less reliable, needs QC
  * Hiring own annotators: less QC needed, expensive, slow to scale
  * Data labeling service companies:
    * [FigureEight](https://www.figure-eight.com/)
* Labeling platforms:
  * [Diffgram](https://diffgram.com/): Training Data Software (Computer Vision)
  * [Prodigy](https://prodi.gy/): An annotation tool powered
by active learning (by developers of Spacy), text and image
  * [HIVE](https://thehive.ai/): AI as a Service platform for computer vision
  * [Supervisely](https://supervise.ly/): entire computer vision platform
  * [Labelbox](https://labelbox.com/): computer vision
  * [Scale](https://scale.com/) AI data platform (computer vision & NLP)

## References
- https://github.com/alirezadir/Production-Level-Deep-Learning
