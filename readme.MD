## DDoS Detection using Machine Learning Algorithms
▪ A distributed denial of service (DDoS) attack is a malicious attempt to make an online service unavailable to users, usually by temporarily interrupting or suspending the services of its hosting
 server.

▪ DoS and DDoS are major threat to any legitimate clients using network services. One should be aware of these attacks. 

▪ In this project, we are going to detect different DDoS attacks by various methods and evaluate their performance. This is a Classification task. These  DDoS detectors could be used for future
  reference.

Common DDoS attack types:

1)UDP Flood
2)TCP_SYN Flood
3)ICMP Flood

Explore more about them for better knowledge on DDoS attacks.

▪ Dataset :  The cleaned.csv file is KD99 generated dataset. It is located in 'dataset' directory

▪ Language and version : Python 3.x 

▪ Packages             : numpy, sklearn, pickle, tqdm, pandas, seaborn and matplotlib.

▪ Techniques           : K-Nearest Neighbours, Decision tree, Multi-layer Perceptron and Logistic Regression. 

▪ Platforms            : Jupyter Notebook and IDLE


▪ 3 .ipynb files on 3 different DDoS attacks implementing all Machine Learning Algorithms in each file.

▪ 2 .py files which is train.py and test.py for fitting our best models with trained and test data.  


In each .ipynb files I have distinguished each model's performance and used the best 2 models in train.py. 

TRAINING OUR MODEL (This will take certain amount of time)
   go to Anaconda prompt and execute the below command
 
      python train.py icmp 0

   This will actually train the data set on "icmp" protocol with the KNN model.
   If you wish to use the Decision tree model:

      python train.py icmp 1

   You can even change the protocol from the choices "udp", "tcp_syn" and "icmp". 
   So if you want to use tcp_syn protocol type and train it with KNN model type:

      python train.py tcp_syn 0
   
   At the end of executing this command you will get something like this:

    Data preprocessing done.
    The model has been fit.
    Save the fitted model?(y/n)

   asking you to save the pre-trained model for future use. type "y" and press enter
   The model is saved using pickle as .sav file and will be used it while testing.
   You can find the .sav files under 'saved_model' directory. 

TESTING OUR MODEL
   This is fast but a little tricky
   You have to ensure how many parameters you input for testing out the class.
    
    python test.py tcp_syn -1.5 1.0 2.0 30.0 1.0
    
   This will use the tcp_syn pre-trained model and test the given parameters on it.
   Now each protocol has different parameter length as input. While tcp_syn protocol takes
   a length of 5 float value inputs others may take different inputs.
   
   NOTE:
   
	ICMP takes 7 ARGUMENTS
	
	UDP takes 5 ARGUMENTS
	
	TCP_SYN takes 5 ARGUMENTS

These are few sample attributes of each attack. You can test and compare the result with predicted ones.
        
    python test.py tcp_syn -1.5 1.0 2.0 1.0 1.0
	python test.py tcp_syn -1.5 1.0 2.0 30.0 1.0
	python test.py icmp 0.0 0.0 30.0 0.0 1.0 0.0 0.0
	python test.py udp 45.0 -0.3 45.0 236.0 2.0



























