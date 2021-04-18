![alt](https://camo.githubusercontent.com/581046b90092b4de08416fe5ea162525a4600ee82d229653b9a94b15873415c5/68747470733a2f2f7777772e7a656c6a6b6f6f6272656e6f7669632e636f6d2f746f6f6c732f746563682f696d616765732f65636c697073655f646565706c6561726e696e67346a2e706e67) </br>
Auteur : Silahi Ali Houssene

# DataVec [1]: Chargement des données

1. **Charger le contenu d'un répertoire de façon récursive ou non**
2. **Utilisation des filtres**
3. **Chargement aléatoire**
4. **Chargement d'un seul fichier**

## Dépendence maven

```xml
<dependency>
    <groupId>org.datavec</groupId>
    <artifactId>datavec-api</artifactId>
    <version>1.0.0-beta7</version>
</dependency>
```  

## Code sample

  
  

```java
   // chargement de tous le fichiers de façon récursive
        FileSplit split = new FileSplit(new File("data/images"));

        // chargement de tous le fichiers de façon non récursive
        FileSplit split1 = new FileSplit(new File("data/images"), null, false);

        // chargement de fichiers jpg
        FileSplit split2 = new FileSplit(new File("data/images"), new String[] { ".jpg" });

        // chargement des images des chats de façon aléatoire
        FileSplit split3 = new FileSplit(new File("data/images/cats"), new Random(1000));

        // chargement d'un fichier spécifique
        FileSplit split4 = new FileSplit(new File("data/csv/iris.data"));

        split4.locationsIterator().forEachRemaining(System.out::println);
```