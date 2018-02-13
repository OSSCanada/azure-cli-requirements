# Azure CLI Version Requirements Files

This repo contains the requirements file for past Azure-CLI 2.0 versions.  The goal is to be able to install/rollback to a previous version of ```azure-cli``` using the ```pip``` command.

## Installing Previous Azure CLI version

Each Azure CLI version's ```requiements.txt``` file is stored in its respecitve directory. You can leverage any one of the respective ```requirements.txt``` file to install that version.  You can run the following command

```:bash
# Assuming you're in the 2.0.26 folder
pip install -r requirements.txt
```

## Get ```requirements.txt``` manually

You can grab the requirements.txt file manually by running the docker image for the specific ```azure-cli``` version you wish to target.

```:bash
# Get requirements.txt for v2.0.26
docker run -it --rm -v ${PWD}:/requirements azuresdk/azure-cli-python:2.0.26 pip freeze > requirements.txt
```