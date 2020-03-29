# safe_graph_data_COVID19
Work documenting and processing data provided by Safe Graph

This repo will have items documenting the data and R code I use for processing the data.

The data is provided by [Safe Graph](www.safegraph.com)  as part of their efforts to help researchers work on issue related to the COVID-19 outbreak. They are providing historical pattern data for people's movement and foot traffic, which is their main business.

If you down load data from AWS you can get an idea of the folder structure [here](https://github.com/ogletrees/safe_graph_data_COVID19/blob/master/file_structure_SafeGraph_AWS_20200327.txt).

If you are downloading from AWS here are some helpful bash commands (assuming you have setup credentials already).

``` bash
# This will list the files in 'historicpatterns' and give more info
aws s3 ls  --summarize --human-readable --recursive s3://sg-c19-response/historicpatterns/ --profile safegraph

# download all the files in a folder
aws s3 sync s3://sg-c19-response/historicpatterns/ /local_folder/ --profile safegraph

# download a specific file
aws s3 cp s3://sg-c19-response/historicpatterns/Apr19-AllPatterns-PATTERNS-2019_04-2020-03-23.zip /local_file_name --profile safegraph
```
