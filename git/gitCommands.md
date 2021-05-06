# Lyhyt git muistio
[git documentaatio](https://git-scm.com/docs/)


## Hyödyllisiä komentoja

**[`git init`](https://git-scm.com/docs/git-init)** muuttaa tietokoneen normaalin hakemiston tyhjäksi git-repositorioksi. Tämä on ensimmäinen vaihe repon luonnissa, vasta tämän komennon jälkeen toiset git-komennot toimivat oikein.

```
git init
```
##

**[`git clone`](https://git-scm.com/docs/git-clone)** luo paikallisen kopion olemassa olevasta etärepositoriosta, voit käyttää tätä komentoa kopioidaksesi tai lataamalla repon tietokoneellesi.

```
git clone [remote URL]
```

##
**[`git add`](https://git-scm.com/docs/git-add)** lisää muutokset "*staging*"-alueelle. Tiedostot tulee siirtää "staging"-aleuelle, jotta ne voi lisätä repoon.
  
**Käyttö:**
```
git add .
git add file(or folder)-name
git add -p
```
**

**[`git status`](https://git-scm.com/docs/git-status)** esittää "repon" nykyisen tilan. Mikäli muutoksia on lisätty "staging"-alueelle, mutta niitä ei ole vielä "commit"oitu, muutokset näkyvät status-komennolla. 

```
git status
```

Kehitystyö tapahtuu käytännössä viemällä muutoksia versionhallintaan 
***

**[`git commit`](https://git-scm.com/docs/git-commit)** vie "staging"-alueella (ks. `git add`) olevat muutokset versionhallintaan ja luo repositorion tallennuspisteen, "commitin", mikä on eräänlainen kuvaus repositorioon tehdyistä muutoksista. Näihin tallennuspisteisiin, "commit"teihin voi palata tarpeenvaatiessa myöhemmin yksillöllisen ID:n avulla. Hyvä käytäntö on sisällyttää jokaiseen committiin viesti, missä selitetään tehdyt muutokset. [[Ohje]](https://github.com/erlang/otp/wiki/writing-good-commit-messages) hyvän commit-viestin kirjoittamiseksi.

**Käyttö:**
```
git commit -m "[commit msg]"
```
***

**[`git branch`](https://git-scm.com/docs/git-branch)** luo uuden versio-haaran nykyiseen haaraan. Uuteen haaraan voi tehdä muutoksia, mitkä eivät näy toisiin versiohaaroihin. Komennolla voi myös poistaa minkä tahansa olemassa olevan haaran tai tarkistella haaroja paikallisesta repositoriosta.

* `-d [branch name]` poistaa `<branch name>`-haaran.

**Käyttö:**
```
git branch
git branch [branch name]
git branch -d [branch name]
```
***

**[`git checkout`](https://git-scm.com/docs/git-checkout)** siirtyy toiseen kehityshaaraan.

* `-b [new branch name]` luo uuden `<new branch name>`-haaran ja siirtyy siihen.

**Käyttö:**
```
git checkout [branch name]
git checkout -b [new branch name]
```

## TODO Lisättäviä komentoja:
- [git pull](https://git-scm.com/docs/git-pull)
- [git push](https://git-scm.com/docs/git-push)
- [git tag]()
- [git stash]() 

## Lähteitä
- [git documentaatio](https://git-scm.com/docs/)
- [Tietokone työvälineenä - Lapio](https://tkt-lapio.github.io/git/) (kurssin git osuus)

<link https://dzone.com/articles/top-20-git-commands-with-examples>
<link https://vm.utu.fi/document/fi_pieni-git-opas.pdf>

 **[`git `]()**
