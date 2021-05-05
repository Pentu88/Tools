# javadoc

[oracle](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#orderoftags)

```java
/**
 * Luokan, attribuutin tai metodin kuvaus
 *
 * @tag kommentti tagille
 */
```

## Lista tageista
***huom*** "**[!]**" -merkinnällä kuvattuja tageja voi olla useita allekkain.

**[@author](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@author)** **[!]** Määrittää luokan tekijän nimen. 

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*

**[@version](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@version)** Määrittää luokan version, kehittäjä voi päättää versiomerkinnän itse.

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*

**[@see](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@see)** **[!]** Määrittää luokat ja metodit dokumentin "katso myös" (see also) -kohtaan.

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*, *[attribuutit](#attribuutit)*, *[metodit](#metodit)*

**[@since](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@version)** Määrittää, mistä versiosta alkaen luokka on ollut mukana luokkakirjastossa.

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*, *[attribuutit](#attribuutit)*, *[metodit](#metodit)*

**[@debrecated [description]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@deprecated)** Määrittelee luokan (tai metodin)  vanhentuneeksi.

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*, *[attribuutit](#attribuutit)*, *[metodit](#metodit)*

**[@param](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@param)** **[!]** Metodin jokaista parametria kohden on sitä kuvaava tagi.

Käyttö: *[metodit](#metodit)*

**[@return](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@return)** Kuvaa metodin paluu-arvoa.

Käyttö: *[metodit](#metodit)*

**[@exception [exeption]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@exception)** **[!]** (Throws)

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*, *[metodit](#metodit)*

## Luokat ja liittymät
Luokkien ja liittymien dokumentoinnissa voi käyttää seuraavia tageja: `@author`, `@version`, `@see`, `@since` sekä `@deprecated`. 
```java
/**
 * [Luokan kuvaus]
 *
 * @author [1st author's name]
 * @author [2nd author's name]
 * @version [verison]
 * @see [class name]
 * @see #[method name]([param])
 * @see #[field name]
 * @since [version]
 */
 public class Luokka{
    public Luokka() {
        // Do things
    }
}
```

## Attribuutit
Attribuuttien dokumentoinnissa voi käyttää seuraavia tageja: `@see`, `@since` sekä `@deprecated`.
```java
 public class Luokka{
   /**
    * [Attribuutin kuvaus]
    *
    * @author [1st author's name]
    * @since [version]
    */
   private String name;
}
```

## Metodit
Metodien dokumentoinnissa voi käyttää seuraavia tageja: `@see`, `@since`, `@deprecated`, `@param`, `@return` sekä `@exception`.
```java
 public class Luokka{
   /**
    * [Metodin kuvaus]
    *
    * @author [1st author's name]
    * @param [param name] [param description]
    * @return [return description]
    * @since [version]
    */
    public String foo(int bar) {
        // Do things
        return "number: " + bar;
    }
}
```

