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

Kolmas väljund annab Errori, sest me korrutame stringi teise stringiga, mis sest, et teine string on number (pane tähele arvul 5 on jutumärkid ümber!). Teisisõnu, sõna ei saa teise sõnaga läbi korrutada. See ei ole meie jaoks loogiline, rääkimata siis ka arvutist.

Samuti soovitan kodus proovida ja katsetada igasuguseid muid aritmeetilisi tehted stringidega. Näiteks, mis juhtuks, kui korrutaksite stringi mõne koma arvuga, ehk floatiga?

# input(), type(), str(), int() ja float() käsud

Tihti osutub kasulikuks küsida kasutajalt sisendit.
Seda saab teha järgmise käsuga:
```python
input()
```
Sulgude sisse, võib ka midagi kirjutada, mida kasutajale enne sisendi küsimist väljastada. Ehk näiteks:
```python
nimi = input("Mis on sinu nimi?: ")
```
NB! See käsk salvestab sisendi STRING kujul, isegi kui sisestakse mõni number.
Andmetüüpe saab kontrollida käsuga:
```python
type()
```
Kontrollimegi, et kui me sisestame input käsku enda nime asemel mõne numbri (näiteks 35), et kas ta salvestub stringina või mõne muu andmetüübina:

```python
nimi = input("Mis on sinu nimi?: ")
print(type(nimi))
```
Väljundiks saame:
```python
"Mis on sinu nimi?: "35
<class 'str'>
```
Ja ütlebki, et tegemist on string (str) andmetüübiga.
Tulevikus tasub siis seda kindlasti meeles pidada, et kui näiteks soovime kasutajalt arvude kujul andmeid küsida ning nendega mingisuguseid arvutusi teha, siis tuleb need "input" andmed teisendada arvulisele kujule.

Andmetüüpe saab teisendada järgmiste käskudega:

```python
str()
float()
int()
```
Kus "str()" teisendab sulgude vahel oleva sisu stringiks, "float()" teisendab sulgude vahel oleva sisu komaarvuks ning "int()" teisendab sulgude vahel oleva sisu väikseimaks täisarvuks.

Järgida tuleb aga ka loomuliku loogikat! Näiteks ei oleks ju loogiline teisendada sõna "Tere" ei täisarvuks ega ka komaarvuks. Pigem on see kasulik siis, kui meil on arvud salvestatud stringideks ja oleks vaja need nö "lahti pakkida" numbriteks.

Ehk veel üks näide:
Laseme kasutajal sisestada kolmnurga kõrgust ja kolmnurga alust. Seejärel teisendame mõõdud komaarvudeks ja arvutame kolmnurga pindala.

**VALE LAHENDUS:**
```python
a = input("Sisesta kolmnurga alus: ")
h = input("Sisesta kolmnurga kõrgus: ")
S = (a*h)/2
print(S)
```
Väljund:
```python
"Sisesta kolmnurga alus": 5
"Sisesta kolmnurga kõrgus": 10 
TypeError: can't multiply sequence by non-int of type 'str'
```
Ehk kuna "input" jäi stringi kujule, siis loomulikult ei saa me sõnadega pindala arvutada.

**ÕIGE LAHENDUS:**
```python
a = float(input("Sisesta kolmnurga alus: "))
h = float(input("Sisesta kolmnurga kõrgus: "))
S = (a*h)/2
print(S)
```
Väljund:
```python
"Sisesta kolmnurga alus": 5
"Sisesta kolmnurga kõrgus": 10 
25.0
```
Ehk kolmnurga pindala tuli 25.0.

# Mõned skriptid, mida võite läbi proovida ja katsetada
Skript 1:
```python
tekst="Tere maailm!"
print(tekst)
```
Skript 2:
```python
nimi=input("Mis on sinu nimi? : ")
print("Tere "+ nimi)
```
Skript 3:
```python
nimi=input("Mis on sinu nimi? : ")
vanus=input("Mis on sinu vanus? : ")
print("Tere "+nimi + ". Sina oled "+vanus+" aastat vana.")
```
Skript 4:
```python
vanus_int=int(input("Sisesta uuesti enda vanus: "))
vanus_sõber_int=int(input("Sisesta enda sõbra vanus: "))
print("Sa oled oma sõbrast "+str(vanus_int-vanus_sõber_int)+" aastat vanem.")
```

Skript 5:
```python
tekst="Tere maailm!"
nimi=input("Mis on sinu nimi? : ")
vanus=input("Mis on sinu vanus? : ")
vanus_int=int(input("Sisesta uuesti enda vanus: "))
vanus_sõber_int=int(input("Sisesta enda sõbra vanus: "))

print("Meie andmetüübid on järgmised:")
print("'tekst' andmetüüp on: " + str(type(tekst)))
print("'nimi' andmetüüp on: "+str(type(nimi)))
print("'vanus' andmetüüp on: "+str(type(vanus)))
print("'vanus_int' andmetüüp on: "+str(type(vanus_int)))
print("'vanus_sõber_int' andmetüüp on: "+str(type(vanus_sõber_int)))

arv_pi=3.14
print("'arv_pi' andmetüüp on: "+str(type(arv_pi)))
```
