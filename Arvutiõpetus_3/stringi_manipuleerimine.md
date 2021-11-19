# .replace()

Meetod tähistusega

```python
.replace()
```
asendab stringis määratud alamstringi uute alamstringidega.
Käsu esimene argument on alamstring mida asendada soovitakse, ning teine argument on alamstring millega see esimene asendatakse. 

Näiteks:

```python
nimi = "Artur"
nimi = nimi.replace("r", "l")
print(nimi)
```
Väljund:

```python
"Altul"
```

# .capitalize() , .upper() ja .lower() käsud

Võib esineda olukordi, kus meil oleks vaja asendada mõnes stringis kõik esinevad ühesugused sümbolid.
Näiteks kui meil oleks string "Hahahahaha", ning me püüaksime asendada kõik "h"-d mõne muu tähega näiteks "k"-ga, siis saaksime:

```python
muutuja = "Hahahahaha"
muutuja = muutuja.replace("h", "k")
print(muutuja)
```
Väljund:

```python
"Hakakakaka"
```
On näha, et esimene "H", meil jäi samaks. Põhjus on selles, et arvuti keel on väga primitiivne ja tundlik ning täidab meie käske nii nagu me talle rangelt ette kirjutasime.
Kuna me palusime asendada kõik väikesed "h"-d, siis suure "H" jättis ta samaks. Võib küll eraldi teha ka asenduse "H" jaoks, kuid mõistlikum oleks teisendada kogu string väikesteks või suurteks tähtedeks. Seda saab teha .lower() või .upper() käsuga.

