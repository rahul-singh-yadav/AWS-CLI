## Pipeline-As-Code

The following json files provide a boilerplate to quickly provision a two stage, three stage ci/cd pipeline at aws.


### Pipeline Structure
---
Core structure of `pipeline`(dictionary object) involves the following:

1. `roleArn`
2. `stages`
3. `artifactStore`: Required field
    - Contains the artifact bucket type and location for a pipeline with all actions in the same AWS Region.
    - Atleast one artifact bucket must exist per region.
4. `name`: pipeline name
5. `version`: A number, auto-incremented on each new deployments
6. `tags`

### Pipeline Stages Stucture
---
Each stage containes the following,

1. `name`
2. `actions`