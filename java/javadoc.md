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

Käyttö: *[luokat ja liittymät](#luokat-ja-liittymät)*, *[attribuutit](#attribuutit)*, *[metodit]()*

**[@since](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@version)** (luokat ja liittymät) (attribuutit) (methods) Määrittää, mistä versiosta alkaen luokka on ollut mukana luokkakirjastossa

**[@exception [exeption]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@exception)** (luokat ja liittymät) (methods) Throws **[!]**

**[@debrecated [description]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@deprecated)** (luokat ja liittymät) (attribuutit) (methods) Määrittelee luokan (tai metodin)  vanhentuneeksi.

**[@param [param name] [description]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@param)** (methods) **[!]** Metodin jokaista parametria kohden on sitä kuvaava tagi.

**[@return [description]](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html#@return)** (methods) Kuvaa metodin paluu-arvoa.

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

## Atribuutit
Attribuuttien dokumentoinnissa voi käyttää seuraavia tageja: `@author`, `@since` sekä `@deprecated`. 

## Metodit
Metodien dokumentoinnissa voi käyttää seuraavia tageja: `@author`, `@since`, `@deprecated`, `@param`, `@return` sekä `@exception`. 

