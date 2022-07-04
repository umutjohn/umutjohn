@TODO: Deterministic Mini-batch Sequencing for Training Deep Neural Networks Subhankar Banerjee, Shayok Chakraborty
This readme file is an outcome of the CENG501 (Spring 2022) project for reproducing a paper without an implementation. See CENG501 (Spring 2022) Project List for a complete list of all paper reproduction projects.

1. Introduction
@TODO: Article,Deterministic Mini-batch Sequencing for Training Deep Neural Networks Subhankar Banerjee, Shayok Chakraborty,published 35th AAAI conference on Atificial Intelligence at 2021. The main goal of this project is to implement proposed alghoritm ,selecting and sequencing mini batches for training neural network. After implementing propesed alghoritm, obtained results will be compared with results obtained from SGD(Stoachastic Gradient Descent),DPP(Determinantal point process) and Submodular methods.  

1.1. Paper summary
@TODO: Summarize the paper, the method & its contributions in relation with the existing literature.
Generalization performance of the model is firmly related to mini batches which are used for computing gradients and updating parameters of the model during the backpropogation alghoritm(Gradient Descent). This leads to motivate to researcher devoloping intelligent sampling techniques rather than stoachastic ones.
In this paper, authors propose an algorithm to generate a deterministic sequence of mini-batches to train a deep neural network. Their alghoritm based on idea which is selecting mini batch such that the data distrubution represented by this selected mini batch and the already selected one, is closest to the distrubution of the unselected training samples. MMD(Maximum Mean Disperancy) metric is used for measuring the closness of these distrubutions.Mini batch selection method can be formulated as an optimization problem with minimizing MMD metrics between the distrubutions. MMD is a statistical metric to compute the difference in marginal probablity between two distrubutions,which is calculated as the difference between the emprical means of the two distrubutions after mapping onto a Reproducing Kernel Hilbert Space. Contributions in existing literature can be listed as follows:
* This is the first attempt to use MMD metric to select mini batches for training DNN.
* Mini batch sequencing strategy is determinsitic and it is independent from the network architecture,task type(regression,classification etc..) and data in hand.
* Benchmark experimental studies was implmented to test the generallizability of the model on cahallenging data set and other methods like DPP,Submodular and SGD.
* Contrary to most of the methods, mini batch sequence can be pre computed indipendently for a given task
* It doesnt require extensive hyper-parameter tunning
* Alghoritm is based on solving Lineer Programing Problem.
2. The method and my interpretation
2.1. The original method
@TODO: Explain the original method.
Orginal alghortim steps can be listed as :
1- Compute Gauissan distrubution function for each sample at unselected training set and store each value at matrix(Phi1).
$e^{i \pi} = -1$
2 - Compute normalize Gaussian distrubution function for each sampel at unselected training set and store each value at vector(Phi2)
3- Compute normalize Gaussian distrubution function for each sampel at already selected training set and store each value at vector(Phi3)
2.2. My interpretation
@TODO: Explain the parts that were not clearly explained in the original paper and how you interpreted them.

3. Experiments and results
3.1. Experimental setup
@TODO: Describe the setup of the original paper and whether you changed any settings.

3.2. Running the code
@TODO: Explain your code & directory structure and how other people can run it.

3.3. Results
@TODO: Present your results and compare them to the original paper. Please number your figures & tables as if this is a paper.

4. Conclusion
@TODO: Discuss the paper in relation to the results in the paper and your results.

5. References
@TODO: Provide your references here.

Contact
@TODO: Provide your names & email addresses and any other info with which people can contact you.
