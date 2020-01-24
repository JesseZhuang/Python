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

  ### 1.3. Data Storage
* Data storage options:
  * **Object store**: Store binary data (images, sound files, compressed texts)
    * [Amazon S3](https://aws.amazon.com/s3/)
    * [Ceph](https://ceph.io/) Object Store
  * **Database**: Store metadata (file paths, labels, user activity, etc).
    * [Postgres](https://www.postgresql.org/) is the right choice for most of applications, with the best-in-class SQL and great support for unstructured JSON.
  * **Data Lake**: to aggregate features which are not obtainable from database (e.g. logs)
    * [Amazon Redshift](https://aws.amazon.com/redshift/)
  * **Feature Store**: store, access, and share machine learning features
 (Feature extraction could be computationally expensive and nearly impossible to scale, hence re-using features by different models and teams is a key to high performance ML teams).
    * [FEAST](https://github.com/gojek/feast) (Google cloud, Open Source)
    * [Michelangelo Palette](https://eng.uber.com/michelangelo/) (Uber)
* Suggestion: At training time, copy data into a local or networked **filesystem** (NFS). <sup>[1](#fsdl)</sup>

### 1.4. Data Versioning
* It's a "MUST" for deployed ML models:
  **Deployed ML models are part code, part data**. <sup>[1](#fsdl)</sup>  No data versioning means no model versioning.
* Data versioning platforms:
  * [DVC](https://dvc.org/): Open source version control system for ML projects
  * [Pachyderm](https://www.pachyderm.com/): version control for data
  * [Dolt](https://www.liquidata.co/): versioning for SQL database

## References
- https://github.com/alirezadir/Production-Level-Deep-Learning
