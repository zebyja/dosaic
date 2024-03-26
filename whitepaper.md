# DOSAIC
DOSAIC is a shortcut for Decentralized Open Source Artifical Inteligence Cloud.

## Claims
It is the most optimal solution for running AI models and its training.

DOSAIC is:
* CHEAP
* RESPECTING PRIVACY
* FULLY ANNONYMOUS
* NO CENSORSHIP
* NO REGULATIONS
* NO DATA MINING

How?

1. Thanks to decentralisation, competition is maximised and thus the minimum price available on the market is achieved.
2. Thanks to open source, anyone can provide their hardware on terms known in advance.
3. Fully homomorphic encryption makes it possible to execute requests over models without the execution provider knowing the contents of the request.
4. The user of the model is motivated to give feedback by recovering part of the cost and model provider can thus train the model and improve its features without knowing the content of the request and the result.

DOSAIC offers the benefits of large models at a lower price than a local run of small models.

## Form of solution
A minimum of three parts are needed:
1. Provider administration microservice
2. Model runner microservice
3. Client API microservice
4. Optional WebClient for Client API microservice. It is not necessary part of decentralized solution but should be made for making adoption possible.

### Provider administration microservice
Provider administration microservice is a microservice with configuration on startup input and a running api that provides model results based on requests.

Configuration contains a list of all provided models and prices of all their queues. Similar to blockchain, each model needs to have dynamic queues so that the user can choose either a cheaper option to wait for the result or a more expensive and faster one. The queue is defined by price and average waiting time, each additional level of the queue has a longer waiting time.

### Model runner microservice
Model runner microservice is a microservice that provides results for a single model. Its input is a configuration that specifies the hardware, its limits and defines the behavior of the model runner in situations where, for example, it is underutilized or overloaded.

### Client API microservice
The main reason for having an official decentralized open source client api microservice is to share information about providers. Sharing this information is in the interest of the client and not in the interest of the provider, and so must be enabled by the user. But this does not matter, because it only requires an internet connection and minimal hardware requirements. And should be part of the client for user freindly usage. Client API additionaly allow list available model and prices, requests models and sending feedback.

Zero knowledge verification in the blockchain can be used to verify that this shared database is genuine and not planted by the provider.