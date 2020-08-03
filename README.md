# COVID-19 image data collection for zegami

This collection of Covid-19 xrays is taken from a project by the University of Montreal.
Please see the original repository here: https://github.com/ieee8023/covid-chestxray-dataset

In this fork we provide only the metadata and images which can be directly used to create a collection in Zegami.
We also provide a specimen configuration file which can be used for uploading to Zegami using our [CLI](https://github.com/zegami/zegami-cli).

## Instructions for use in the Zegami UI

**TODO** link to support page

* Create a new collection
* Select a 'Deepzoom' collection
* Drag and drop the metadata.csv file and the images folder onto the files area
* Await processing

## Instructions for using the Zegami CLI
Using the CLI is the best way to create large collections, especially where automated workflows are desirable.

#### Install the cli
```
pip install -r requirements.txt
```

#### Log in
If you don't already have an account, sign up for one at https://zegami.com

Once you have an account, log in with
```
zeg login
```

#### Create the collection
First you will need to determine the id for the project in which you wish to create the collection.
**TODO** explain how to get project id
```
zeg create collections --project <project id> --config covid_xrays.yaml
```
