# jef-docs
Jupyter Experiment Framework documentation

## Introduction

This set of Jupyter Notebooks explains installation of jef, its usage for running experiments, and the managing of experiments.

**Installation and general considerations**

```
Installation.ipynb
BeforeStarting.ipynb
```

**Using jef to run experiments**

```
experimentFormatSubmit.ipynb 
``` 

 ## Before Starting

### Python version

This jef distribution must be run with Python 3.6 .

### MongoDB

jef requires a MongoDB server running on any host where job submission, job execution, or experiment management is carried out. It is assumed that the MongoDB server does not require authentication.

### jobStarter

jef requires the program `jobStarter.pyc` to be running. For every instance of the program running, one job may run simultaneously on the server (hence, to have two jobs running on the server, start two instances). jobStarter starts jobs from the queue automatically. To stop jobs running, kill the instances of jobStarter.

The file `jobStarter.pyc` is included in this jef distribution and it will be found whereever pip places files from packages. For an Anaconda installation this is at `[PATH TO ANACONDA]/anaconda3/lib/python3.6/site-packages/[PACKAGE]` and `jobStarter.pyc` is found at `[PATH TO ANACONDA]/anaconda3/lib/python3.6/site-packages/jef/scripts/jobStarter.pyc`. It may be copied to another location if preferred.

`jobStarter.pyc` should be started in the working directory where you would like temporary experiment files to be created. It is invoked with
```
python [PATH TO JOBSTARTER]/jobStarter.pyc
```

## Installing jef

* you need to get a download user name and password from Pax (at present use username=`pypi` and password=`pax1385`)
* from a terminal command line:
```
[user@localhost ~]$ pip install --trusted-host ec2.paxculturastudios.com --extra-index-url  http://ec2.paxculturastudios.com:8080 jef
```
* enter the user name and password at the prompts
* if it works jef will be downloaded and installed
* start an interactive python session by typing `python` at the command-line prompt (the version of Python has to be 3.6; you can ensure Python 3 is running by typing `python3` instead of `python`, although this will not guarantee the subversion is 3.6
* at the Python interactive prompt:
```
>>> import jef
```
* if there are no error messages it means that jef has been correctly installed and is now ready to be used in your code


 

 



**Managing Experiments**

 
``` 
listExperiments.ipynb
haltJob.ipynb
haltAllJobs.ipynb
listQueue.ipynb 
wipeQueue.ipynb
deleteFromQueue.ipynb 
plotResults.ipynb
wipeQueue.ipynb
getSettings.ipynb 
getSource.ipynb 
``` 

