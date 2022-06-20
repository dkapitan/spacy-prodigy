# spacy-prodigy

## Introduction
This repo provides an end-to-end Docker-based NLP workbench with spaCy v3 and prodigy the core components:

- Use [spaCy v3](https://spacy.io) as the core NLP engine
  - [spaCy projects](https://spacy.io/usage/projects) with a `project.yml` for managing directories, assets and commands
  - Use [remote storage integration](https://spacy.io/usage/projects#remote) for storing data on AWS S3, Google Cloud Storage or Azure
  - Use [prodigy integration](https://spacy.io/usage/projects#prodigy) to start the annotation server for a tight feedback loop between data development and training
  - Use [spaCy pipelines](https://spacy.io/usage/processing-pipelines) for preprocessing within a project


- Use [prodigy](https://prodi.gy/) annotation tool
  - NB: you should have purchased a prodigy license and make the wheel file available

- Use Docker throughout the workflow such that it can be scheduled on a serverless cloud infrastructure
  - Use [multistage builds](https://docs.docker.com/develop/develop-images/multistage-build/) for optimizing images throughout the workflow (e.g. for training vs. inference)
  - Use modular design to allow use of orchestration tools like [AWS Batch with Step Functions](https://docs.aws.amazon.com/step-functions/latest/dg/connect-batch.html) or [Prefect](https://prefect.io)
  
