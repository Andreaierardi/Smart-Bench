# Relazione di progetto - Reti2 Sperimentazioni ![logo](/img/logo.png)

![main](/img/firstpage.png)

# Smart-Bench


## Introduction
The aim of the project is to show the development and realization of a smart bench press that monitors the state, performance and health of the atlete during a session training with sensors.
In particular, the SmartBench reads and elaborates the data that come from three different sensors:
- gym weights: monitor variation of weights.
- barbell: monitor repetition (barbell lifted up and down) and if the barbell is placed in the initial position. 
- bracelet: monitor heartbeat and heart rate.

## Technologies
The architecture used is message broker in this way it is ensured modularity. Also, it used MQTT protocol for communication between brokers and modules.
There are two Mosquitto Broker: 
- Cloud broker: guarantees communication between controller, client and database.
- Local Beaglebone broker: guarantees communication between sensor and controller.
The traffic is minimum because each device used the Publish/subscribe pattern since the IoT devices have low memory and computation.

## Architecture
![resume](/img/structure.JPG)


## Class diagram
![diagram](/img/diagram.png)
