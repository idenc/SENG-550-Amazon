# SENG 550 Amazon Review Dataset analysis

This repo contains a dataset which consists of samples from [this dataset](http://deepyeti.ucsd.edu/jianmo/amazon/index.html)
The version used was the 2018 5-core review dataset from all categories.
The original dataset is over 86 GB, while the sampled version is only 250 MB

## Installation
The Spark version used is 3.0.1. Download from [here](https://spark.apache.org/downloads.html) \
Create a Python virtual environment using
```
python -m venv venv
```
activate the virtual environment
```
source venv/bin/activate
```
on linux
```
venv/Scripts/activate.bat
```
on Windows

then install requirements using
```
pip install -r requirements.txt
```
then launch jupyter notebook using
```
jupyter notebook
```

## Citation:
**Justifying recommendations using distantly-labeled reviews and fined-grained aspects** \
Jianmo Ni, Jiacheng Li, Julian McAuley \
*Empirical Methods in Natural Language Processing (EMNLP),* 2019

The notebook is based off of [this GitHub repo](https://github.com/noahberhe/Lobbyists4America)

## Databricks Setup
* Use cluster runtime 6.4
* Spark config should have: 
  
    spark.serializer org.apache.spark.serializer.KryoSerializer

    spark.kryoserializer.buffer.max 1000M
    
    spark.databricks.delta.preview.enabled true
* Install the following libraries:
  * JohnSnowLabs:spark-nlp:2.4.0 Maven
  * spark-nlp pypi
  * wordcloud pypi
  * nltk pypi
  * textblob pypi
  
Attach the notebook to this cluster to start working on it

The data for the notebook is the music.json file.
