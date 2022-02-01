---
layout: default
title: Research
permalink: /research/
---

# Current Research 
At Meta I am currently working on privacy-preserving ML and on-device Machine learning. 


# Past Research Samsung AI

At Samsung AI I was working on the intersection of systems, networks and AI. I was particularly interested in distributed machine learning both for inference (offloading to the edge/cloud) and training (federated learning and on-device personalization)


#### Federated Learning
Federated Learning is quickly gaining traction in privacy-centric distributed deployments of ML models.
The aim of this research is to explore how we can train different model architectures in a massively scalable Federated Learning setup, where heterogeneous clients, both in terms of data (non-iid) and compute capabilities exist. Furthermore, we are looking how biases in the data affect the resulting models.

#### On-Device personalization 
Machine learning models are typically over-provisioned to support a wide variety of input distributions. For example, an ASR system has to support people with various demographics,  accents, different microphone configurations, a large number of possible noisy environments, etc. These wide distributions result in rather large models that can only be compressed that much.
However, once installed, these systems are typically used by a single individual that has some specific input distributions. For example, in the ASR example specific age, accent, environment etc. 
On-device learning can help us personalize these models to remove any biases, improve accuracy and even reduce computational complexity.  We use state-of-the-art teqniques such as self-supervision and  Meta-Learning techniques to support efficient on-device personalization.



#### AI offloading
State-of-the-art models are increasing in complexity exponentially. 
While on-device model execution is the ultimate goal, some of these models cannot be possibly be supported by embedded devices. 
At the same time, the advent of 5G will enable low-latency communication with the edge and the cloud. 
In this work we conduct research on offloading AI computation to the edge and the cloud. We look into the system challenges on where to place computation, how to optimize the communication between the phone and the edge/cloud and on how to scale offloading in order to support million of clients. 


#### AI scheduling
Mobile devices might have a wide range of available computation capabilities that can support AI tasks (e..g, CPUs, GPUs, DSPs, NPUs, FPGAs). At the same time more and more models are being deployed and many of them have to be concurrently executed. In this work we look how we can schedule this computation on a heterogeneous computation platform in order to maximize the overall throughput, minimize energy consumption  while satisfying the application QoE requirements.

#### AI backend optimizations
Embedded AI is supported by great tools such as Tensorflow Lite and Caffe2. However, mobile execution is still in its infancy. Frequently operators are not supported or they are not optimized for mobile execution. Furthermore, AI libraries are not always included or supported by the vendors. Furthermore, memory and energy restrictions might require us to make compromises in terms of the complexity of the models. In this project our goal is to research novel tools that will help us compile, compress, quantise, distill and execute models on mobile and embedded devices. 


#### Cellular networks and AI
Machine learning has a big impact on cellular networks. We are looking into the research areas of network automation, zero configuration, monitoring and anomaly detection, self-healing and RAN optimization with the help of deep-learning.


# Past Research Telefonica
At Telefonica Research, I was also using AI on big-data to support the cellular and fixed network of millions of customers. Some of the projects that I have worked on include:

#### Anomaly detection 
In Telefonica I was leading a project on using deep-learning to detect anomalies and outliers in large-scale cellular networks.  The main idea is to identify anomalies, correlate them together and identify the root cause. Furthermore, we were using SDN/NVFs to automatically intervene and auto-heal the network. 

#### Forecasting cellular-network issues
Similarly to the previous project, we use deep-learning to predict the demand and forecast bottlenecks in cellular networks. Furthermore, we were able to make predictions about individual Key-Performance Indicators (KPIs) and provide early warnings to the radio teams. Finally, we worked towards predicting in advance failures that might need human intervention. 


#### Model customer satisfaction
The idea is to combine all the data that are gathered (weblogs, mobility, CRM, network singling, call-center calls to complain, network measurements, etc) in order to estimate each customer’s satisfaction and understand the main reasons of dissatisfaction. We use a spark cluster to crunch terabytes of data that are daily collected into customer features. Then we used machine learning to model satisfaction, churn, up-sell, etc. 


#### Encrypted Traffic classificaEon and QoE estimation
By analysing web-logs and DPIs of encrypted traffic, we designed a system to perform real-time mobile traffic classificaIon and idenIfy poor QoE. We collected the groundtruth with a combinaIon reverse-engineering and by instrumenting android devices to crowdsource telemetry. 



#### Crowd-source assisted android testing with deep-learning
We designed a platform to allow crowdsourcing human inputs for mobile phone testing. The idea is to stream fully-usable mobile applications to a browser in order to be used by crouwdsourcing platforms such as crowdflower, mechanical turk, etc. 
 My work was primarily around automated tesIng. I designed an architecture that combines RNN and CNN to learn from the crowdsourced input and replicate user input (taps, text, dragging, etc). The idea is to learn from real users to speed-up automated testing to increase code coverage in a more efficient way than automated “monkeys”.


#### Mobile instrumentation
I wrote an SDK to collect measurements from Android devices (location, network, accelerometer, light, etc). Furthermore, we also conduct on-device experience sampling (quesIonnaire). This was used to collect the groundtruth and to provide telemetry to the operator. 


#### Mobile network measurements 
As part of Telefonica I was responsible to collect, analyze and model network measurements that come from various part of the network (RAN, backbone, MME, client devices, etc)


#### Smart notifications 
We use the data coming from mobile phones to predict when is the best time to send out noIficaIons. I have been working on the effort to use RNNs to perform continuous  predicIons. 


#### Location modeling 
We designed and currently implemenIng a model in order to model the mobility of cellular network users. We used a combination of network events, mapping information and deep-learning in order to model large-scale mobility patterns. 


#### Network capacity planning
I studied the factors that impact the success of cellular capacity upgrades and build an algorithm to make recommendaIons on where to upgrade capacity.


#### Insurance telematics
Used mobility traces to esImate the driving behaviour of individuals and estimate the risk.

####  Privacy & Mobile networks
In collaboraIon with UCL and NICTA, we looked into how unique are our cellular-network clients in terms of i) mobility, ii) web/app usage. Furthermore, we looked into privacy leak from  smartphone applications. Finally, we built a model to detect malicious behavior in our cellular network (crypto-miners, etc).