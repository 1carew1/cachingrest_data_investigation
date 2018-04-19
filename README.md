# Caching Rest Data Investigation

## Run the project
To run this anaconda needs to be installed 

```
source activate py3
jupyter-notebook
```


## View the Results
You can click on the ipynb file in github or go to the link below :
https://nbviewer.jupyter.org/github/1carew1/cachingrest_data_investigation/blob/master/Cachingrest_Data_Investigation.ipynb

In general you can view any jupyter notebook publically available by appending the file location to : https://nbviewer.jupyter.org/url/
Or if hosted on github just use the github link after https://nbviewer.jupyter.org/

## Download the Data
The mysql data dump for the iterim can be accessed via : https://drive.google.com/file/d/1tVjDn-SpbBUKIxwhU-9hkkiKUN2ELqLd/view?usp=sharing

Note this data has only one run of each of the cache size tests, so only LRU from 128MB to 1024MB has been tested for hazelcast, redis, memcached and ehcache, once each.

## Required Installs
```
source activate py3
# For Mac
brew install mysql
# Instal python mysql
pip install pymysql
```
