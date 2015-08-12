Samosa:
version 0.01.01 
 
* An even easier, simpler and versatile alternative to [Lasagne](https://github.com/Lasagne/Lasagne).
* Promotes easy learnability and practice of theano.


## Who is this code most useful for ?

I wrote this code essentially for my labmates, those who are interested in starting deep CNNs to make a fast transition into theano. This will also be useful for industry when teting out prototypes. This might not be really useful for advanced deep learning researchers. If you are a serious researcher and you either find a bug or you want to just make suggestions please feel free, I will be grateful.  

***

## What is in this repository? 

The code that is here in this repository has the following features, among many others:
* CNNs with easy architecture management: The code has the ability to change architecture: with just small changes in some input parameters and immediately a whole new network can be created. One variable changes the number of MLP layers, number of nodes in each layer, activation functions and even dropout probabilities. You can also change number of CNN layers, their pooling and stride sizes. Basically any vanilla network that you can draw on a black board can be set up quite simply using a few input parameters. 

* Optimization techniques: This is where things change a lot and for someone who is getting into deep learning fresh without much theoretical machine learning, I am hoping it would be really helpful. With some flags and parameters in the boilerplate of the code, you could switch entire optimization methods, including gradient descent, adaGrad, rmsProp add momentums like Polyak Momentum, Nesterov’s accelerated gradients etc. One switch converts the whole networks into a max-margin formulation from a softmax formulation. I intended this for people in my lab, who wouldn’t now have to spend days reading the theory behind these methods , but just try them first and if they work, then think of reading them.   
   - Dropouts[1]
   - adaGrad[2]
   - Polyak Momentum[3]
   - Nesterov's Accelerated Gradients [4]
   - rmsProp [5]
   
* Data handling capabilities: I have provided features to setup data as simple matlab files that can be loaded in python and run in batches for training. Alternatively, I also have options for ‘pkl.gz’ files if you would like to cPickle and / or zip your data. Also provided a wrapper to [skdata's dataset](https://jaberg.github.io/skdata/) interface (under construction, as of now, I have cifar10, mnist, extended mnists ,caltech101, caltech256). 

* Data visualization capabilities: Visualize the activities of select images (random) from the trainset on each layer after select number of epochs of training. Also view filters after select number of epochs. If the input images are color, the first layer saves down color features. The only way to know if a networks is trained or not is by constantly visualizing the filters. I have provided ways to save down the filters and activations after every ( optionally after how many ever ) epochs and probe into the weights of the networks. 
   
More features will be added as and when I am implementing them. You can check the `to_do.txt` in the repository for expected updates.  I will add more detailed description of the implementation as and when I have time to so. But don't expect it soon.

*** 

## The story behind the repository

This project was something I was just building as a mental exercise for myself, just to get into deep learning. Surprisingly, it developed into a good flexible tool that was appreciated by people who I work with in both my lab and in my TA class. I am brushing it up and making it a public 'toolbox' of sorts and hope that it will be useful to try an architecture quickly with various different options or to quickly test out some datasets with some architecture design in mind.

*** 

## Installation.

Running this code essentially requires:

    1. python 2.x
    2. theano 0.7 +
    3. numpy 
    4. scipy
    5. skdata
    6. cPickle
    7. opencv (cv2)
    8. gzip

Most of these could be installed by installing [anaconda of continuum analytics](http://docs.continuum.io/anaconda/install.html) The code is reasonably well documented. It is not that difficult to find out from the boilerplate what is happening. 
Just `git clone` into a folder and run `__init__.py`. Change the setup of networks on the boilerplate. 

*** 

## Questions. 

Thanks for using my repository in the first place. I have questions being asked from basically students who are probably using my code for class projects and some researchers who are just getting into deep learning. If you have questions please email me. My email can be found in my website below at the signature or at my GitHub profile. I am going to compile some answers to FAQs as and when I can next. 

***
# References
[1]   Srivastava, Nitish, et al. "Dropout: A simple way to prevent neural networks from overfitting." The Journal of Machine Learning Research 15.1 (2014): 1929-1958.

[2]   John Duchi, Elad Hazan, and Yoram Singer. 2011. Adaptive subgradient methods for online learning and stochastic optimization. JMLR

[3]   Polyak, Boris Teodorovich. "Some methods of speeding up the convergence of iteration methods." USSR Computational Mathematics and Mathematical Physics 4.5 (1964): 1-17. Implementation was adapted from Sutskever, Ilya, et al. "On the importance of initialization and momentum in deep learning." Proceedings of the 30th international conference on machine learning (ICML-13). 2013.

[4]   Nesterov, Yurii. "A method of solving a convex programming problem with convergence rate O (1/k2)."   Soviet Mathematics Doklady. Vol. 27. No. 2. 1983. Adapted from [Sebastien Bubeck's](https://blogs.princeton.edu/imabandit/2013/04/01/acceleratedgradientdescent/) blog.

[5] Yann N. Dauphin, Harm de Vries, Junyoung Chung, Yoshua Bengio,"RMSProp and equilibrated adaptive learning rates for non-convex optimization", or arXiv:1502.04390v1

Parts of the code are directly lifted from [theano tutorials](http://deeplearning.net/software/theano/tutorial/) or from [Misha Denil's repository](https://github.com/mdenil). 

*** 

Thanks for using the code, hope you had fun.

Ragav Venkatesan
http://www.public.asu.edu/~rvenka10
