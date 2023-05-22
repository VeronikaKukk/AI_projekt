# ASL tähtede tuvastamine videost

**Veronika Kukk ja Lauri Lüüsi**

**TÜ arvutiteaduse instituut, kevad 2023**

---

### Töö eesmärk ja tehisintellekti kasutamise vajadus

Meie töö eesmärk oli kasutada masinõpet, et tuvastada veebikaamera videovoost ASL (American Sign Language) tähemärke ning seejärel need kasutajale ette lugeda.

ASL on keel, mis on laialdaselt kasutusel Põhja-Ameerikas, eelkõige inimeste seas, kes on kaotanud kuulmisvõime. Keeles väljendab iga inglise tähte üks unikaalne käemärk, mida viibates on võimalik teistega suhelda ilma kõne, suud ja kõrvu kasutamata. 

Töö käigus on vaja kasutada kahte tehisintellekti komponenti, masinõpet ja kõnesünteesi, millest esimene tunneb ära videovoost käemärgid ja teine sünteesib tuvastatud märkidest kõne, et viibatud sõna kasutajale ette lugeda. Lisaks kasutame ka videosisendi töötlemist ehk muudame videost saadud kaadri suurust ja lisame kaadrile peale tekstikasti, kus on seni viibatud märgid.

---

### Kasutatud ideed (nii kursuse materjalidest kui mujalt) koos viidetega

Kasutatud andmestik (ASL alphabet): https://www.kaggle.com/datasets/grassknoted/asl-alphabet

Mudeli ettevalmistamine ja treenimine: https://www.tensorflow.org/tutorials/images/classification

Ühe närvivõrgu inspiratsioon: https://www.kaggle.com/code/edbertkhovey/uts-asl-2022-deep-learning

Video sisselugemine kaamerast: Tehisintellekt (LTAT.01.003), praktikum 9 (lisamaterjal)

---

### Iga autori enda panuse kirjeldus

**Lauri:** Treenisin erinevaid mudeleid, et tuvastada videovoost käemärke ja lisasin videovoo ülesse riba, kuhu tekivad jooksva sõna tähed.

**Veronika:** Tegin andmete jagamise train ja validationiks. Treenisin kaks mudelit. Tegin kõnesünteesi osa, tegin video sisselugemise ja programmi katkestamise. 

---

### Programmi testimisvõimalused ja vähemalt mõned testimistulemused

<>

---

### Töö käigu kirjeldus
*(millised olid probleemid, mis õnnestus, mis jäi realiseerimata)*

Üheks probleemiks oli see, et tahtsime kõigepealt teha klassifitseerijat, mis otse veebikaamera videovoost käemärgid ära tunneks, aga selle tarbeks oli vaja treeningandmed käsitsi ära märgistada, mis ei tundunud umbes 27 (tähe) * 3000 (pilte tähe kohta) korral mõistlik.

Seejärel otsustasime, et teeme videovoost pildi ja anname selle mõnele "tavalisele" närvivõrgule sisendiks. Kuid ka tavalise närvivõrgu tegemine osutus vägagi probleemseks, sest pilte oli palju ja nad olid (võrreldes tekstiliste andmetega) üsna suured, mistõttu kulus treenimiseks väga palju aega. Erinevad katsed treenimist kiirendada (kasutada treenimisel protsessori asemel videokaarti, muuta kihtide struktuuri lihtsamaks/kiiremaks, jne) kas üldse ei aidanud ega töötanud või andsid hoopis vastupidiseid või mitte etteaimatavavaid tulemusi, mistõttu oli kohati raske leida, mida peaks muutma, et paremaid tulemusi saada.

Kokkuvõtteks võib öelda, et kõik lubatu sai realiseeritud. Kasutaja saab näidata kaamerale ASL tähti, need tehakse tekstiks ning loetakse seejärel talle ette. Probleem on aga selles, et käemärke tuvastav närvivõrk ei ole piisavalt hea, mis on eelkõige tingitud arvutusvõimsuse ja aja puudusest.

Paraku peab tõdema, et töö oli vist liiga suure mahuga ja kujunes liiga ambitsioonikaks, sest praktikumides jm varasemalt realiseeritud närvivõrgud klassifitseerisid palju vähem, väiksemaid ja rohkem teineteisest erinevaid pilte väiksema arvu klasside vahel. Kuid sellegipoolest, kõik muu (sisendi töötlemine, lugemine, ekraanile kuvamine ja kõnesünteesimine jm) töö juures töötab hästi ning kui asendada olemasolev närvivõrk mingi paremaga, oleks tegemist veel paremini töötava ja kasulikuma programmiga.

---
