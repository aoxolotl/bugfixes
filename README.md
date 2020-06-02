# bugfixes
Common errors encountered and how I fixed them. :bug:

## android
1. *Execution failed for task ':app:mergeReleaseResources'.*
Encountered while building a React Native project with `./gradlew assembleRelease`

Fix: 
Locate the resources mentioned in the error log and remove 
`$ rm -r app/src/main/res/{drawable-*,raw}`

Rerun `./gradlew assembleRelease`

## huggingface/transformers
1. While running `run_ner.py`:
`KeyError:''`
Check this page: https://github.com/huggingface/transformers/issues/4061
Could be either of the fixes mentioned there
