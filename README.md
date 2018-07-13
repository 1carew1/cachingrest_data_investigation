# Caching Rest Data Investigation

## Run the project
To run this anaconda needs to be installed 

```
source activate py3
jupyter-notebook
```


## Install Python3 and Jupyter
```
# Download Miniconda - python3 version
https://conda.io/miniconda.html - For Mac : https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
# Run the setup script
bash Miniconda3-latest-MacOSX-x86_64.sh
# Follow setup script and fill in info as necessary
# Create new termina and Create python3 environment
conda create -n py3
source activate py3
conda install jupyter
conda install seaborn
conda install -c conda-forge jupyter_contrib_nbextensions
conda install pymysql
# Start the notebook
jupyter-notebook
```

## View the Results
You can click on the ipynb file in github or go to the link below :
https://nbviewer.jupyter.org/github/1carew1/cachingrest_data_investigation/blob/master/Cachingrest_Data_Investigation.ipynb

In general you can view any jupyter notebook publically available by appending the file location to : https://nbviewer.jupyter.org/url/
Or if hosted on github just use the github link after https://nbviewer.jupyter.org/

## Download the Data
The mysql data file for the final results (as of 2018-07-14) can be accessed via : https://drive.google.com/file/d/1BcAg5hYOdYIijnp1-F6DYT2yuLKorgzS/view?usp=sharing

Once downloaded the data needs to be extracted and this will yield a cachetest.dump file - this dump was take from a MySQL 5.7 install.
To load in the data
```
mysql -u user -p -e "create database cachetest"
mysql -u user -p cachetest < cachetest.dump
```

The mysql data dump for the iterim (as of 2018-04-19) can be accessed via : https://drive.google.com/file/d/1tVjDn-SpbBUKIxwhU-9hkkiKUN2ELqLd/view?usp=sharing

Note this data has only one run of each of the cache size tests, so only LRU from 128MB to 1024MB has been tested for hazelcast, redis, memcached and ehcache, once each.
