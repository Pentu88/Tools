# javadoc

[oracle](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#orderoftags)

```java
/**
 * Luokan, attribuutin tai metodin kuvaus
 *
 * @tag kommentti tagille
 */
```

**[@author](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@author)** **[!]** Määrittää luokan tekijän nimen. 

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*

**[@version](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@version)** Määrittää luokan version, kehittäjä voi päättää versiomerkinnän itse.

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*

**[@see](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@see)** (luokat ja liittymät) (attribuutit) (methods) **[!]** Määrittää luokat ja metodit dokumentin "katso myös" (see also) -kohtaan.

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*, *[attribuutit](#attribuutit)*, *[metodit](#metodit)*

**[@since](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@version)** Määrittää, mistä versiosta alkaen luokka on ollut mukana luokkakirjastossa.

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*, *[attribuutit](#attribuutit)*, *[metodit](#metodit)*

**[@exception [exeption]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@exception)** **[!]** (Throws)

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*, *[metodit](#metodit)*

**[@debrecated [description]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@deprecated)** Määrittelee luokan (tai metodin)  vanhentuneeksi.

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*, *[attribuutit](#attribuutit)*, *[metodit](#metodit)*

**[@param [param name] [description]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@param)** **[!]** Metodin jokaista parametria kohden on sitä kuvaava tagi.

Käyttö: *[metodit](#metodit)*

**[@return [description]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@return)** Kuvaa metodin paluu-arvoa.
Käyttö: *[metodit](#metodit)*

**[!]** -merkinnällä kuvattuja tageja voi olla useita allekkain.

## Luokat ja liittymät
Luokkien ja liittymien dokumentoinnissa voi käyttää seuraavia tageja: `@author`, `@version`, `@see`, `@since` sekä `@deprecated`. 
```java
/**
 * [Luokan, attribuutin tai metodin kuvaus]
 *
 * @author [1st author's name]
 * @author [2nd author's name]
 * @version [verison]
 * @see [class name]
 * @see #[method name]
 * @see [class name]
 * @since [version]
 */
 public class Luokka{
    public Luokka() {
        // Do something
    }
}
```

## Attribuutit
Attribuuttien dokumentoinnissa voi käyttää seuraavia tageja: `@author`, `@since` sekä `@deprecated`. 

## Metodit
Metodien dokumentoinnissa voi käyttää seuraavia tageja: `@author`, `@since`, `@deprecated`, `@param`, `@return` sekä `@exception`. 

