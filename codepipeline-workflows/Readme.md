## Pipeline-As-Code

The following json files provide a boilerplate to quickly provision a two stage, three stage ci/cd pipeline at aws.


### Pipeline Structure
---
Core structure of `pipeline`(dictionary object) involves the following:

1. `roleArn`
2. `stages`
3. `artifactStore`
4. `name`
5. `version`
6. `tags`

A couple of nuances associated with few of the fields which can be read by following the documentation provided at the bottom of this document.

### Pipeline Stages Stucture
---
Each stage containes the following,

1. `name`
2. `actions`

With `actions` taking the bulk of the pipeline-as-code. 


### Documentation
---
- https://docs.aws.amazon.com/codepipeline/latest/userguide/reference-pipeline-structure.html