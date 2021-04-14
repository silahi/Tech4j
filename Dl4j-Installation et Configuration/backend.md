# Deeplearning4j Backends

![alt](https://camo.githubusercontent.com/581046b90092b4de08416fe5ea162525a4600ee82d229653b9a94b15873415c5/68747470733a2f2f7777772e7a656c6a6b6f6f6272656e6f7669632e636f6d2f746f6f6c732f746563682f696d616765732f65636c697073655f646565706c6561726e696e67346a2e706e67) </br>
Auteur : Silahi Ali Houssene

## Configuration et Installation  (Maven)  

### 1. Backends GPUs

* **CUDA Version 9.2 +** et **NVIDIA**

```xml
 <dependency>
    <groupId>org.nd4j</groupId>
    <artifactId>nd4j-cuda-9.2</artifactId>
    <version>1.0.0-beta7</version>
</dependency>
```  

* Exemple : CUDA 10.2

```xml
 <dependency>
    <groupId>org.nd4j</groupId>
    <artifactId>nd4j-cuda-10.2</artifactId>
    <version>1.0.0-beta7</version>
</dependency>
```

### 2. Backends CPUs

 ```xml
<dependency>
    <groupId>org.nd4j</groupId>
    <artifactId>nd4j-native</artifactId>
    <version>1.0.0-beta7</version>
</dependency>
 ```

### 3. Backends sur plusieurs architectures

 ```xml
<dependency>
    <groupId>org.nd4j</groupId>
    <artifactId>nd4j-native-platform</artifactId>
    <version>1.0.0-beta7</version>
</dependency>
 ```

### 4. Backends pour les CPU et AVX (Advanced Vector Extensions)

* AVX512 sous Windows

 ```xml
 <dependency>
    <groupId>org.nd4j</groupId>
    <artifactId>nd4j-native</artifactId>
    <version>1.0.0-beta7</version>
</dependency>

<dependency>
    <groupId>org.nd4j</groupId>
    <artifactId>nd4j-native</artifactId>
    <version>1.0.0-beta7</version>
    <classifier>windows-x86_64-avx2</classifier>
</dependency>
 ```

* AVX512 sous Linux

```xml
<dependency>
    <groupId>org.nd4j</groupId>
    <artifactId>nd4j-native</artifactId>
    <version>${nd4j.version}</version>
</dependency>

<dependency>
    <groupId>org.nd4j</groupId>
    <artifactId>nd4j-native</artifactId>
    <version>${nd4j.version}</version>
    <classifier>linux-x86_64-avx512</classifier>
</dependency>
  ```

### 5. Dl4j core

 ```xml
<dependency>
      <groupId>org.deeplearning4j</groupId>
      <artifactId>deeplearning4j-core</artifactId>
      <version>1.0.0-beta7</version>
</dependency>
 ```

### 5. DataVec

 ```xml
<dependency>
      <groupId>org.datavec</groupId>
      <artifactId>datavec-api</artifactId>
      <version>1.0.0-beta7</version>
</dependency>
 ```

* Local

 ```xml
 <dependency>
      <groupId>org.datavec</groupId>
      <artifactId>datavec-local</artifactId>
      <version>1.0.0-beta7</version>
</dependency>
 ```

* Spark

 ```xml
<dependency>
    <groupId>org.datavec</groupId>
    <artifactId>datavec-spark_2.12</artifactId>
    <version>1.0.0-beta7</version>
</dependency>

 ```
