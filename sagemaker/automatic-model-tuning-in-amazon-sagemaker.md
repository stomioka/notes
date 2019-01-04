# Automatic Model Tuning in Amazon SageMaker

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Automatic Model Tuning in Amazon SageMaker](#automatic-model-tuning-in-amazon-sagemaker)
	- [Hyperparameters](#hyperparameters)
		- [Neural Networks](#neural-networks)
		- [Trees](#trees)
		- [Clustering](#clustering)
		- [Tuning](#tuning)
	- [SageMaker's method](#sagemakers-method)
	- [SageMaker integration](#sagemaker-integration)
		- [Hyperparameter Tuning](#hyperparameter-tuning)

<!-- /TOC -->

## Hyperparameters
* Large ingluence on performance
* grows exponentially
* non-linear/interaction


### Neural Networks
* Learning rate
* layers
* Regularization
* drop out

### Trees
* Number
* depth
* boosting step size

### Clustering

* Number
* Initialization
* Pre-processing

### Tuning

* manual
* grid search
* random search
* sobol

* meta model

## SageMaker's method
* Gaussian process regression models objective metric as a function of yperparameters
* Assumes smoothness
* low data
* confidence esimtates

Once the above predictive model is built, Bayesian optimization decides where to earch next
* explore and exploit
* gradient free<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Automatic Model Tuning in Amazon SageMaker](#automatic-model-tuning-in-amazon-sagemaker)
	- [Hyperparameters](#hyperparameters)
		- [Neural Networks](#neural-networks)
		- [Trees](#trees)
		- [Clustering](#clustering)
		- [Tuning](#tuning)
	- [SageMaker's method](#sagemakers-method)
	- [SageMaker integration](#sagemaker-integration)
		- [Hyperparameter Tuning](#hyperparameter-tuning)

<!-- /TOC -->

## SageMaker integration
![](images/ab62578e.png)
![](images/5349ead9.png)
![](images/847ca645.png)
![](images/3f0628ed.png)
![](images/464a264b.png)



``` python

hyperparameters = {
    'learning_rate': 0.1,
    'epoch': 20,
    'optimizer':'sgd'
}
```

* Hyperparameters can take
  * Continuous
  * integer
  * categorical

* Objective metric logged
`val-RMSE=([0-9\\\\.]+)`

* CloudWatch
* regex

### Hyperparameter Tuning

[@github](https://github.com/awslabs/amazon-sagemaker-examples/tree/master/yperparameter_tuning/mxnet_gluon_cifar10_random_search)
