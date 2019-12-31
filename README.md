# Voce 2.0 with Maven

Mirror of Voce Code, with my improvements related to upgrade build process with maven. 

Keywords : Java Speech recognition api java voce speech FreeTTS CMU Sphinx Speech Recognizer Text To Speech voce.sourceforge.net speech recognition using Java and Sphinx Pure Java speech recognition library java SpeechRecognition 

# Upstream 

[http://voce.sourceforge.net](http://voce.sourceforge.net)

# Inspiration

I do this because I love artificial intelligence and I dream about the day when a true artificial intelligence can coexist with humans.

# Improvements

* Usage maven artifact repository [https://mvnrepository.com/](https://mvnrepository.com/) for this libraries : freetts

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

- Java 7 or 8
- [Download Maven](http://maven.apache.org/download.cgi)
- [Install Maven](http://maven.apache.org/install.html)

In order to compile and get your own library of voce jar, install this two offline jars in your local maven :

- install required libraries with: 

```
mvn install:install-file -Dfile=offline-jars/sphinx4-1.0.jar -DgroupId=edu.cmu.sphinx -DartifactId=sphinx4 -Dversion=1.0 -Dpackaging=jar

mvn install:install-file -Dfile=offline-jars/jsapi-1.0.jar -DgroupId=javax.speech -DartifactId=jsapi -Dversion=1.0 -Dpackaging=jar

```

### Compile

- go to cloned folder and execute

```
mvn clean package
```

If no errors, a jar named voce.jar will be inside **target** folder ready to use in your java projects

### Install

If no errors in compilation step, voce jar could be used as maven library.

Just execute this:

```
mvn clean install
```

After that, you can use this dependency in your maven projects:

```xml
<dependency>
	<groupId>voce</groupId>
	<artifactId>voce</artifactId>
	<version>0.9.1</version>
</dependency>
```


## Running the tests

...


## Voice Recognition usage

See this proof of concept [https://github.com/jrichardsz/java-speech-recognition-apis/tree/master/voce](https://github.com/jrichardsz/java-speech-recognition-apis/tree/master/voce)
...


## Deployment

...

## Built With

* [Maven](https://www.apache.org/) - Apache Maven is a software project management and comprehension tool
* [Java](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html) - Java SE Development Kit 7 Downloads

## Contributing

...

## Versioning

Current version is 0.9.1

## Authors

* **Tyler Streeter** - *Initial work* - [http://voce.sourceforge.net/](http://voce.sourceforge.net/) [http://www.tylerstreeter.net/](http://www.tylerstreeter.net/) **streeter@iastate.edu** **tylerstreeter@gmail.com**

* **Richard Osmar Leon Ingaruca** - *Migrate to maven* - [contact me](http://jrichardsz.weebly.com/contact.html)

## License

Voce is licensed under the BSD or LGPL Open Source licenses.  Also, be sure to read the licenses for [FreeTTS](http://freetts.sourceforge.net/docs/index.php) and [CMU Sphinx4](http://cmusphinx.sourceforge.net/wiki/tutorialsphinx4).

