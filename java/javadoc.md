# javadoc

[oracle](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#orderoftags)

```java
/**
 * Luokan, attribuutin tai metodin kuvaus
 *
 * @tag kommentti tagille
 */
```

**[@author [authors name]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@author)** (luokat ja liittymät) [!] Määrittää luokan tekijän nimen. 

**[@version [verison]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@version)** (luokat ja liittymät) Määrittää luokan version, kehittäjä voi päättää versiomerkinnän itse.

**[@see [class name]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@see)** (luokat ja liittymät) (attribuutit) (methods) [!] Määrittää luokat ja metodit dokumentin "katso myös" (see also) -kohtaan. 

**[@since [version]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@version)** (luokat ja liittymät) (attribuutit) (methods) Määrittää, mistä versiosta alkaen luokka on ollut mukana luokkakirjastossa

**[@exception [exeption]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@exception)** (luokat ja liittymät) (methods) Throws [!]

**[@debrecated [description]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@deprecated)** (luokat ja liittymät) (attribuutit) (methods) Määrittelee luokan (tai metodin)  vanhentuneeksi.

**[@param [param name] [description]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@param)** (methods) [!] Metodin jokaista parametria kohden on sitä kuvaava tagi.

**[@return [description]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@return)** (methods) Kuvaa metodin paluu-arvoa.

**[!]** -merkinnällä kuvattuja tageja voi olla useita allekkain.
