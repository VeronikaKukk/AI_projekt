# ASL tähtede tuvastamine videost

### Töö eesmärk ja tehisintellekti kasutamise vajadus

<>

---

### Kasutatud ideed (nii kursuse materjalidest kui mujalt) koos viidetega

Kasutatud andmestik (ASL alphabet): https://www.kaggle.com/datasets/grassknoted/asl-alphabet

Mudeli ettevalmistamine ja treenimine: https://www.tensorflow.org/tutorials/images/classification

---

### Iga autori enda panuse kirjeldus

<>

---

### Programmi testimisvõimalused ja vähemalt mõned testimistulemused

<>

---

### Töö käigu kirjeldus
*(millised olid probleemid, mis õnnestus, mis jäi realiseerimata)*

Üheks probleemiks oli see, et tahtsime teha klassifitseerijat, mis otse veebikaamera videovoost käemärgid ära tunneks, aga selle tarbeks oleksime pidanud treeningandmeid käsitsi ära märgendama, mis ei tundunud umbes 26 (tähe) * 3000 (pilte tähe kohta) korral mõistlik.

Ka tavalise närvivõrgu tegemine ei olnud lihtne, sest pilte oli palju ja nad olid (võrreldes tekstiliste andmetega) üsna suured, mistõttu kulus treenimiseks väga palju aega.

---