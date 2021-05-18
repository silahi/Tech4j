# Deeplearning4j
 
![alt](https://camo.githubusercontent.com/581046b90092b4de08416fe5ea162525a4600ee82d229653b9a94b15873415c5/68747470733a2f2f7777772e7a656c6a6b6f6f6272656e6f7669632e636f6d2f746f6f6c732f746563682f696d616765732f65636c697073655f646565706c6561726e696e67346a2e706e67) </br>
Auteur : Silahi Ali Houssene

Pour plus de détails : [Tech4j on Youtube](https://www.youtube.com/channel/UC3ZKhGziYa1Tg6HS7SoFCzw)

## 1. DL4j

C'est un framwork de **deeplearning** :

- Open Source
- Distribué
![alt](https://github.com/silahi/deeplearningalgos/blob/images/distributed.jpg?raw=true)
- JVM / C++ / Python
![alt](https://github.com/silahi/deeplearningalgos/blob/images/dl4j-jvm-lang-comp.jpg?raw=true)

## 2. Concepts de base

### 2.1. DataVec  

* **Préparation des données pour l'apprentissage et la prédiction**
 ![alt](https://github.com/silahi/deeplearningalgos/blob/images/dl4j-types.png?raw=true) 
* **Normalisation des données**

### 2.2. Nd4j

* DataSets
![* ](https://miro.medium.com/max/3880/1*GDM8ogtF6004Q5J8kOgIIA.png)
* INDArrays
![alt](https://res.cloudinary.com/practicaldev/image/fetch/s--hi96gU9b--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/pj0q0bgh3g0jx88gmooo.png)
* Mini-Batches

## 3. Model de Réseau de Neurones

* **Configuration** </br>

~~~

MultiLayerConfiguration conf = new NeuralNetConfiguration.Builder()
        .optimizationAlgo(OptimizationAlgorithm.STOCHASTIC_GRADIENT_DESCENT)
        .updater(new Nesterovs(learningRate, 0.9))
        .list(
            new DenseLayer.Builder().nIn(numInputs).nOut(numHiddenNodes)
            .activation("relu").build(),
            new OutputLayer.Builder(LossFunction.NEGATIVELOGLIKELIHOOD)
            .activation("softmax").nIn(numHiddenNodes).nOut(numOutputs)
            .build())
    .backprop(true).build();
    MultiLayerNetwork model = new MultiLayerNetwork(conf);
~~~

* **Entrainement**
~~~
model.fit(trainSet);// single epoch
~~~   
ou bien 
~~~
for (int i=0; i< numberOfEpoc; i++){ 
    model.fit(trainSet);
}
~~~ 
* **Evaluation des performences** </br>

![alt](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT4GcUasGArCPUfiPCbi-0wyro3emFBspJjnA&usqp=CAU)

* **Monotoring / Troubleshooting**

> **ScoreIterationListener** </br>
> **HistogramIterationListener** </br>

![alt](https://user-images.githubusercontent.com/517415/41141894-608bcb14-6b11-11e8-8e3e-e1937af722f7.png)
