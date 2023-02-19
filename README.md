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

## jupyter + setuptools
While importing a previously installed module in Jupyter
```ZipImportError: bad local file header```
This is likely to happen because 
1. Setuptools version is outdated / incompatible with python version
2. Module was reinstalled with `python setup.py install` while jupyter notebooks was already running

