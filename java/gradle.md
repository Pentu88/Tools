# Gradle
[Gradle](https://gradle.org/) on tietokoneohjelmistojen kääntämiseen ja siihen liittyvien toimintojen automatisointiin tarkoitettu työkaluohjelma.

## Sisältö
* [Konfigurointi](#konfigurointi)
* [Taskien suorittaminen](#gradle-taskien-suorittaminen)
  * [Gradle](#tasks-gradle)
  * [java-blugin](#tasks-java)
  * [application-plugin](#tasks-application)
  * [jacoco-plugin](#tasks-jacoco)
* [Liitännäiset](#gradle-liit%C3%A4nn%C3%A4iset-plugins)
* [Riippuvuudet](#riippuvuudet-dependencies)
* [Lähdekoodi](#l%C3%A4hdekoodin-lis%C3%A4%C3%A4minen-projektiin)

## Gradle taskien suorittaminen
*Gradle*-taskit (gradlen komennot) suoritetaan projektin juuressa komentoriviltä muodossa `gradle [task]`. Komennolla `gradle -v` voi tarkastaa *Gradle*n version. Mikäli *Gradle*a ei ole asennettu, voit kopioida (Linux)`gradlew`- ja (Windows)`gradlew.bat`- tiedostot toisesta projektista. Tiedostot tulee sijoittaa projektin juureen, jolloin komennot suoritetaan muodossa (Linux)`./gradlew [task]` tai (Windows)`gradlew.bat [task]`. Voit myös kopioida molemmat tiedostot sisältävän *Gradle*-projektipohjan [tästä]() hakemistosta.
  
<a id="tasks-gradle">**Taskit - gradle**</a>

`tasks` listaa käytettävissä olevat taskit (komennot).

`init` alustaa gradle projektin.

## Konfigurointi
Gradle-projekti määritellään projektihakemiston juureen sijoitettavan *build.gradle*-tiedoston avulla, joka luodaan projektia alustaessa (ks. gradle init, [tältä listalta](https://github.com/Pentu88/Toolbox/blob/master/java/gradle.md#taskit---perus)). Gradle luo valmiiksi projektille sopivan .gitignore -tieodston, missä määritellään *.gradle*- ja *build*-hakemistot jätettäväksi pois versionhallinnan piiristä.

## Gradle liitännäiset (plugins)
Tiedosto *build.gradle* tulee alkaa *plugin*-määrittelyllä

Gradle *plugin*it otetaan käyttöön lisäämällä *build.gradle*-tiedostoon rivit:
```groovy
plugins {
    id '[plugin]'
}
```
*Plugin*ien käyttö saattaa lisätä projektille uusia taskeja.

**[`java-plugin`](https://docs.gradle.org/current/userguide/java_plugin.html)** otetaan käyttöön lisäämällä *build.gradle*-tiedostoon, *plugins*-osioon rivi `id 'java'`. Se tuo mukanaan joitakin Javan kääntämiseen liittyviä taskeja. Oletusarvoisesti *Gradle* ei tiedä *java*sta mitään.

<a id="tasks-java">**Taskit - java-plugin**</a>

[Doc-tasks](https://docs.gradle.org/current/userguide/java_plugin.html#sec:java_tasks)

`build` suorittaa koodin kääntämisen, paketoinnin jar -tiedostoksi ja projektiin liittyvät testit.
```
gradle build
``` 
##

`clean` poistaa *build*-hakemiston sisältöineen.
```
gradle clean
``` 
##

`test` suorittaa sovellukseen liittyvät testit.
```
gradle test
gradle test jacocoTestReport
```

`jar` paketoi koodista *jar*-tiedoston.
```
gradle jar
```

Taskia `jar` varten *build.gradle*-tiedostoon määritellään *pääohjelman sijainti* lisäämällä rivit:
```groovy
jar {
    manifest {
        attributes 'Main-Class': 'Main'
    }
}
```

Luotu *jar*-tiedosto suoritetaan `java -jar [file name].jar`-komennolla, hakemistossa, jossa ko. tiedosto on.

**[application-plugin](https://docs.gradle.org/current/userguide/application_plugin.html)**  otetaan käyttöön lisäämällä *build.gradle*-tiedostoon, *plugins*-osioon rivi `id 'application'`.\
Lisäksi *build.gradle*-tiedostoon tulee määritellä pääohjelman sisältävä luokka (*main class*) lisäämällä rivit:
```groovy
application {
    mainClass = 'Main'
}
```

<a id="tasks-application">**Taskit - application-plugin**</a>

[Doc - tasks](https://docs.gradle.org/current/userguide/application_plugin.html#sec:application_tasks)
Se sisältää myös *java-plugin*in [taskit](#tasks-java).

`run` kääntää ja suorittaa sovelluksen. Optiolla *-q* gradle jättää omat tulostukset pois.
```
gradle run
$ gradle run -q
```

Määritellään *run*-taskille komentorivi liitettäväksi syötevirtaan *System.in* lisäämällä *build.gradle*-tiedostoon rivit:
```groovy
run {
    standardInput = System.in
}
```
##

**[jaCoCo-plugin](https://docs.gradle.org/current/userguide/jacoco_plugin.html#gsc.tab=0)** otetaan käyttöön lisäämällä *build.gradle*-tiedostoon, *plugins*-osioon rivi `id 'jacoco'`.

<a id="tasks-jacoco">**Taskit - jacoco-plugin**</a>
[Doc - tasks](https://docs.gradle.org/current/userguide/jacoco_plugin.html#sec:jacoco_tasks)\
**HUOM** tehtävässä käytettävä jacoco-plugin edellyttää toimiakseen gradlen versiota 5.6.

`jacocoTestReport` kerää projektista testien rivikattavuusraportin.
```
$ gradle test jacocoTestReport
```
Testikattavuus-raportti on generoitu *index.html*-tiedostoon, hakemistossa *build/reports/jacoco/test/html/*

## Riippuvuudet (dependencies)
Käytännössä riippuvuudet ovat jar-paketteja, jotka sisältävät käytettävien apukirjastojen koodin. 
Projektin riippuvuudet määritellään *gradle.build*-tiedostossa lisäämällä rivit:
```groovy
repositories {
    jcenter()
}

dependencies {
    implementation group: '[group]', name: '[name]', version: '[version]'
    testImplementation group: '[group]', name: '[name]', version: 'version'
}
```

Missä:
* *repositories*-osa määrittelee mistä *Gradle*n tulee hakea riippuvuudet. 
* *dependencies*-osa määrittelee käytettävät riippuvuudet.\
Molempiin osiin voidaan määritellä useita rivejä. 

vaihtoehtoinen syntaksi, missä riippuvuus, ja sen versio kerrotaan yhtenä merkkijonona:
```
implementation '[group]:[name]:[version]'
testImplementation '[group]:[name]:[version]'
```

## Lähdekoodin lisääminen projektiin
Gradle projektissa ohjelman lähdekoodi sijoitetaan hakemisto-polkuun *src/main/java* ja ohjelman testit hakemisto-polkuun *src/test/java*.
```
* [project's root]
├── src
│   ├── main
│   │   └── java
│   │       └── [app-files]
│   ├── test
│   │   └── java
│   │       └── [test-files]
...
```

## Lähteet
* [Gradle -dokumentaatio](https://docs.gradle.org/current/userguide/userguide.html) - Virallinen dokumentaatio, mm. [simple index](https://docs.gradle.org/current/samples/index.html), [Gradle plugins](https://docs.gradle.org/current/userguide/plugin_reference.html#header)
* [OhTu -materiaali](https://ohjelmistotuotanto-hy-avoin.github.io/) - Helsingin yliopiston *DEFA*-kurssi materiaali, mm. [Gradle-sivu](https://ohjelmistotuotanto-hy-avoin.github.io/gradle/)
