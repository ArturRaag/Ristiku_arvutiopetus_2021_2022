# Põhilised andmetüübid
Põhilised andmetüübid on:
1) str - "string", ehk vaikimisi jutumärkides olev sõna/tekst.
2) int - "integer", ehk täisarv. NB! Teisendab väiksemaiks täisarvuks. Ehk nt arvu 5.9 ümbardaks int käsk arvuks 5.
3) float - "float", ehk komaarv. Otstarbekad erinevate arvutuste jaoks.

Andmetüüpe on veelgi, kuid nendega tutvume veidi hiljem.

Etteruttavalt mainime, et käsk
```python
print()
```
trükkib ekraanile sulgude vahel oleva sisu (stringi kujul)!

# Muutujate deklareerimine
Selleks, et andmeid koguaeg ümber mitte kirjutada (näiteks mingeid pikkaid valemeid või tekste), võime need andmed salvestada mõne muutuja sisse, kasutades võrdusmärki.
 ```python
 tekst = "Tere Maailm!"
 suvaline_arv = 3
 ```
 Ehk praegusel juhul me deklareerisime endale muutuja "tekst" mis sisaldab antud sisu: "Tere Maailm!".
 Samuti deklareerisime muutuja "suvaline_arv", mis sisaldab arvu 3.
 
 Kindlasti võiks tekkida küsimus, et milleks deklareerida muutujat arvude jaoks ( trükkida "suvaline_arv" võtaks rohkem aega kui lihtsalt "3").
 Hoolimata sellest, et "3"-e trükkimine võtaks vähem aega, kui "suvaline_arv", on sellel muutujal siiski üks eelis olemas.
 Nimelt kui meil oleks koostatud programm, mis sisaldab 100+ rida koodi, ning oleks järsku vaja teha programmi siseselt mõni muudatus.
 Siis selle asemel, et igalpool (igal real) neid arve muuta ja ümber trükkida, saaksime vaid programmi alguses muuta muutuja "suvaline_arv" väärtust.
 
 Lihtne näide: Kolmnurga pindala arvutamise programm.
 
```python
alus=15
kõrgus=20
S=(alus*kõrgus)/2
print(S)
```
Säärane programm väljastaks meile arvu 150 (see ongi kolmnurga pindala).

Kuid eeldame, et meie kolmnurga kõrgus on muutunud. Uus kolmnurga kõrgus on 100.

Selle asemel, et kogu programmi uuesti ümber kirjutada, piisab sellest, kui muudame muutuja "kõrgus" omistatud väärtust.
Ehk:
```python
alus=15
kõrgus=100
S=(alus*kõrgus)/2
print(S)
```
Programm väljastab, et kolmnurga pindala on: 750.

Hetkel oli küll tore vaid ühe valemiga/funktsiooniga töötada, sisuliselt ei oleks olnud häda midagi ka uut programmi selle jaoks kirjutada.
Kuid jällegi, tasub silmas pidada, et tõsisemad programmid sisaldavad sadu kui mitte tuhandeid ridu koodi, ning iga rea pealt seda kolmnurga
kõrgust arvuna otsida, oleks väga ajakulukas tegevus. Palju lihtsam oleks luua selle jaoks programmi alguses muutuja, ning seda vastavalt oma soovidele
muuta.

# String andmetüüp

Stringid on jutumärkides olev tekst, kusjuures tekst võib sisaldada ka numbreid ja muid sümboleid.
Stringidega saab teostada järgmisi "tehteid":
```python
sõna_1 = "Tere Maailm!"
sõna_2 = " Minu nimi on Artur!"

print(sõna_1+sõna_2)
print(sõna_1 * 5)
print(sõna_1 * "5")
```
Väljund:
```python
"Tere Maailm! Minu nimi on Artur!"
"Tere Maailm!Tere Maailm!Tere Maailm!Tere Maailm!Tere Maailm!"
TypeError
```

Ehk nagu näha, esimene väljund "sõna_1" + "sõna_2" annab meile mõlema muutuja kokku liimitud stringid kujul: "Tere Maailm! Minu nimi on Artur!". 
Siit saame teha esimese järelduse: kahe stringi liitmisel, "kleebitakse" stringid kokku üheks uueks stringiks.

Teine väljund annab meile viiekordse "Tere Maailm!"-a. Ehk kui stringi mõne täisarvuga läbi korrutada, siis see string kleebitakse iseendale järgi määratud arv kordi.

Kolmas väljund annab Errori, sest me korrutame stringi teise stringiga, mis sest, et teine string on number (pane tähele arvul 5 on jutumärkid ümber!).

Samuti soovitan kodus proovida ja katsetada igasuguseid muid aritmeetilisi tehted stringidega. Näiteks, mis juhtuks, kui korrutaksite stringi mõne koma arvuga, ehk floatiga?

