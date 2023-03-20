## Pipeline-As-Code

The following json files provide a boilerplate to quickly provision a two stage, three stage ci/cd pipeline at aws.


### Pipeline Structure
---
Core structure of `pipeline` (dictionary object) involves the following:

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

With *actions* taking the bulk of the pipeline-as-code. Find below a skeleton for reference:

```
[
                {
                   "inputArtifacts": [
                        An input artifact structure, if supported for the action category
                    ],
                   "name": "ActionName",
                   "region": "Region", 
                   "namespace": "source_namespace", 
                   "actionTypeId": {
                        "category": "An action category",
                        "owner": "AWS",
                        "version": "1"
                        "provider": "A provider type for the action category",
                   },
                   "outputArtifacts": [
                        An output artifact structure, if supported for the action category
                   ],
                   "configuration": {
                        Configuration details appropriate to the provider type
                   },
                   "runOrder": A positive integer that indicates the run order within the stage,
                }
            ]
```


### Documentation
---
- https://docs.aws.amazon.com/codepipeline/latest/userguide/reference-pipeline-structure.html