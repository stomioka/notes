# SageMaker Introduction

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [SageMaker Introduction](#sagemaker-introduction)
	- [SageMaker components](#sagemaker-components)
	- [No setup is necessary](#no-setup-is-necessary)
	- [High performance on demand](#high-performance-on-demand)
	- [Model deployment](#model-deployment)
	- [Create a notebook instance](#create-a-notebook-instance)
	- [Start notebook instance](#start-notebook-instance)
	- [Jupyter Dashboard](#jupyter-dashboard)
	- [Many example notebooks are available](#many-example-notebooks-are-available)
- [Running xgboost on SageMaker](#running-xgboost-on-sagemaker)
	- [Setup](#setup)
- [Define IAM role](#define-iam-role)

<!-- /TOC -->

## SageMaker components
![](images/6eda09be.png)

## No setup is necessary
![](images/db44bbdc.png)

## High performance on demand
![](images/9fac42a8.png)

## Model deployment
![](images/31ca5c9e.png)

You can specify a computer resurce you need for the model

## Create a notebook instance
![](images/edbabad0.png)

## Start notebook instance
![](images/e2b98320.png)

Now you can start either Jupyter or Jupuyter Lab

## Jupyter Dashboard
![](images/6014412a.png)

## Many example notebooks are available
![](images/dd1b5df2.png)

# Running xgboost on SageMaker
![](images/27effdc2.png)

## Setup

* First, define the **S3 bucket and prefix** that you want to use for training and model data. This should be within the same region as the Notebook instance, training, and hosting.
* The **IAM role** are used to give training and hosting access to your data.

``` python

bucket = '<your_s3_bucket_name_here>'
prefix = 'sagemaker/DEMO-xgboost-churn'

# Define IAM role
import boto3
import re
from sagemaker import get_execution_role

role = get_execution_role()

```

Then import some python libraries.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import io
import os
import sys
import time
import json
from IPython.display import display
from time import strftime, gmtime
import sagemaker
from sagemaker.predictor import csv_serializer
```

Then download data.
