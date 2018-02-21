## Fast Homomorphic Evaluation of Deep Discretized Neural Networks

This repository contains the code that allows to replicate the results presented in the [paper](ia.cr/2017/1114) by Florian Bourse and Michele Minelli and Matthias Minihold and Pascal Paillier.


## Abstract
The rise of Machine Learning as a Service (MLaaS) multiplies scenarios where one faces a privacy dilemma: either sensitive user data must be revealed to the entity that evaluates the cognitive model (e.g., in the Cloud), or the model itself must be revealed to the user so that the evaluation can take place locally. Fully Homomorphic Encryption (FHE) offers an elegant way to reconcile these conflicting interests in the Cloud-based scenario and also preserve non-interactivity. However, due to the inefficiency of existing FHE schemes, most applications prefer to use Somewhat Homomorphic Encryption (SHE), where the complexity of the computation to be performed has to be known in advance, and the efficiency of the scheme depends on this global complexity.

In this paper, we present a new framework for homomorphic evaluation of neural networks, that we call FHE-DiNN, whose complexity is strictly linear in the depth of the network and whose parameters can be set beforehand. To obtain this scale-invariance property, we rely heavily on the bootstrapping procedure. We refine the recent FHE construction by Chillotti et al. (ASIACRYPT 2016) in order to increase the message space and apply the sign function (that we use to activate the neurons in the network) during the bootstrapping. We derive some empirical results, using TFHE library as a starting point, and classify encrypted images from the MNIST dataset with more than 96% accuracy in less than 1.7 seconds.

Finally, as a side contribution, we analyze and introduce some variations to the bootstrapping technique of Chillotti et al. that offer an improvement in efficiency at the cost of increasing the storage requirements.


## Category / Keywords:
Fully Homomorphic Encryption, Neural Networks, Bootstrapping, MNIST


## Authors and Affiliations
**[Florian Bourse](http://www.di.ens.fr/~fbourse)** - Orange Labs, Applied Crypto Group, Cesson-Sévigné, France  
**[Michele Minelli](http://www.di.ens.fr/~minelli)** - École normale supérieure, CNRS, INRIA, PSL Research Univeristy  
**[Matthias Minihold](http://www.cits.rub.de/personen/minihold.html)** - Horst Görtz Institut für IT-Security, Ruhr-Universität Bochum  
**[Pascal Paillier](https://www.cryptoexperts.com)** - CryptoExperts


## Dependencies
Our C++ code depends on a Fast Fully Homomorphic Encryption Library over the Torus [TFHE](https://github.com/tfhe/tfhe) or an extention with improvements therof called [windowed TFHE](https://github.com/MatthiasMi/tfhe/tree/windowed).
