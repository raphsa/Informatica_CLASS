---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Introduzione al laboratorio

Gli esercizi durante le ore di laboratorio verranno svolti in coppia, al fine di favorire la comprensione. Il lavoro di coppia permette di individuare e correggere tempestivamente gli errori e, inoltre, favorisce il ragionamento su ciò che si sta svolgendo, nell'interazione con il compagno di lavoro.

Di seguito, le slide ufficiali del corso, ad opera del Professore Stefano Pio Zingaro.

<a href="https://virtuale.unibo.it/mod/resource/view.php?id=1836002" target="_blank" style="text-decoration: none;">
  <div style="border: 2px solid #ddd; padding: 16px; border-radius: 10px; background-color: #f0f8ff; text-align: center; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    📎 <strong>Teoria sulle basi del linguaggio: tipo, espressioni, nomi e assegnamento, stato</strong><br>
    <small>slide del professore da Virtuale</small>
  </div>
</a>

<div style="margin-top: 20px;"></div>

<a href="https://virtuale.unibo.it/mod/resource/view.php?id=1836007" target="_blank" style="text-decoration: none;">
  <div style="border: 2px solid #ddd; padding: 16px; border-radius: 10px; background-color: #f0f8ff; text-align: center; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    📎 <strong>Introduzione al laboratorio</strong><br>
    <small>slide del professore da Virtuale</small>
  </div>
</a>

## Esercizi

Di seguito, qualche semplice esercizio di lettura per cominciare a familiarizzare con il linguaggio Python:

###### Esercizio di lettura 1:
```{code-cell}
a = "ciao"
b = "mondo"
aeb = a+b
```

Cosa restituisce il comando `print(aeb)`?

<form onsubmit="checkAnswer(event, 'q1_intro', 'ciaomondo', 'feedback1_intro')">
  <input type="radio" name="q1_intro" value="ciao mondo"> ciao mondo<br>
  <input type="radio" name="q1_intro" value="ciao+mondo"> ciao+mondo<br>
  <input type="radio" name="q1_intro" value="ciaomondo"> ciaomondo<br>
  <input type="radio" name="q1_intro" value="ciao,mondo"> ciao,mondo<br>
  <br>
  <input type="submit" value="Verifica" style="border-radius:5px">
  <button type="button" style="border-radius:5px" onclick="resetQuiz('q1_intro', 'feedback1_intro')">Reset</button>
</form>

<div style="margin-top: 20px;"></div>

<p id="feedback1_intro"></p>

<script>
function checkAnswer(event, groupName, correctValue, feedbackID) {
  event.preventDefault();
  const choices = document.getElementsByName(groupName);
  let selected = null;
  for (const choice of choices) {
    if (choice.checked) {
      selected = choice.value;
      break;
    }
  }

  const feedback = document.getElementById(feedbackID);
  if (selected === correctValue) {
    feedback.innerHTML = "✅ Corretto!";
  } else if (selected) {
    feedback.innerHTML = "❌ Sbagliato. Riprova.";
  } else {
    feedback.innerHTML = "⚠️ Seleziona una risposta prima di verificare.";
  }
}

function resetQuiz(groupName, feedbackID) {
  const choices = document.getElementsByName(groupName);
  for (const choice of choices) {
    choice.checked = false;
  }
  document.getElementById(feedbackID).innerHTML = "";
}
</script>




###### Esercizio di lettura 2:
```{code-cell}
a = "ciao" 
b = 5 
aperb = a*b 
```

Cosa restituisce il comando `print(aperb)`?

<form onsubmit="checkAnswer(event, 'q2_intro', 'ciaociaociaociaociao', 'feedback2_intro')">
  <input type="radio" name="q2_intro" value="5ciao"> 5ciao<br>
  <input type="radio" name="q2_intro" value="ccccciiiiiaaaaaooooo"> ccccciiiiiaaaaaooooo<br>
  <input type="radio" name="q2_intro" value="ciaociaociaociaociao"> ciaociaociaociaociao<br>
  <input type="radio" name="q2_intro" value="cinqueciao"> cinqueciao<br>
  <br>
  <input type="submit" value="Verifica" style="border-radius:5px">
  <button type="button" style="border-radius:5px" onclick="resetQuiz('q2_intro', 'feedback2_intro')">Reset</button>
</form>

<div style="margin-top: 20px;"></div>

<p id="feedback2_intro"></p>

###### Esercizio di lettura 3:
```{code-cell}
a = 2 
b = 3 
area = a*b
perimetro = a*2 + b*2 
```

Cosa restituisce il comando `print(area, perimetro)`?

<form onsubmit="checkAnswer(event, 'q3_intro', '6 10', 'feedback3_intro')">
  <input type="radio" name="q3_intro" value="6, 10"> 6, 10<br>
  <input type="radio" name="q3_intro" value="6 10"> 6 10<br>
  <input type="radio" name="q3_intro" value="23, 14"> 23, 14<br>
  <input type="radio" name="q3_intro" value="ab, a2b2"> ab, a2b2<br>
  <br>
  <input type="submit" value="Verifica" style="border-radius:5px">
  <button type="button" style="border-radius:5px" onclick="resetQuiz('q3_intro', 'feedback3_intro')">Reset</button>
</form>

<div style="margin-top: 20px;"></div>

<p id="feedback3_intro"></p>

###### Esercizio di lettura 4:
```{code-cell}
a = 42 
b = a 
a = 13 
print(a, b)
```

Cosa restituisce il comando `print(a, b)`?

<form onsubmit="checkAnswer(event, 'q4_intro', '13 42', 'feedback4_intro')">
  <input type="radio" name="q4_intro" value="42, 13"> 42, 13<br>
  <input type="radio" name="q4_intro" value="13 42"> 13 42<br>
  <input type="radio" name="q4_intro" value="42 13"> 42 13<br>
  <input type="radio" name="q4_intro" value="13 a"> 13 a<br>
  <br>
  <input type="submit" value="Verifica" style="border-radius:5px">
  <button type="button" style="border-radius:5px" onclick="resetQuiz('q4_intro', 'feedback4_intro')">Reset</button>
</form>

<div style="margin-top: 20px;"></div>

<p id="feedback4_intro"></p>

## Esercizi da svolgere

###### 1° esercizio:

Scrivere un programma che stampa il perimetro di un quadrato avente il lato `l = 3`.

```{code-cell}
l = 3
```
Partendo dal codice sopra, prova a risolvere l'esercizio:
<a href="https://www.programiz.com/python-programming/online-compiler/" target="_blank" style="text-decoration: none;">
  <div>
    <strong>Clicca qui per sviluppare il tuo codice!</strong><br>
  </div>
</a>

<div style="margin-top: 20px;"></div>

<button id="show-intro1" style="border-radius:5px" onclick="document.getElementById('output-intro1').style.display='block'; document.getElementById('show-intro1').style.display='none'; document.getElementById('hide-intro1').style.display='inline';">
  Mostra soluzione
</button>

<button id="hide-intro1" style="display:none; border-radius:5px" onclick="document.getElementById('output-intro1').style.display='none'; document.getElementById('show-intro1').style.display='inline'; document.getElementById('hide-intro1').style.display='none';">
  Nascondi soluzione
</button>

<div style="margin-top: 20px;"></div>

<div id="output-intro1" style="display:none;">

```python
l = 3
perimetro = 4*l
print(perimetro)
```
</div>

###### 2° esercizio:

Scrivere un programma che stampa `n` volte una stringa `s` a piacere (es. con `n = 4`, `s = "ciao"` stamperà `ciaociaociaociao`)

```{code-cell}
s = ""
n = 0
```

Partendo dal codice sopra, prova a risolvere l'esercizio:
<a href="https://www.programiz.com/python-programming/online-compiler/" target="_blank" style="text-decoration: none;">
  <div>
    <strong>Clicca qui per sviluppare il tuo codice!</strong><br>
  </div>
</a>

<div style="margin-top: 20px;"></div>

<button id="show-intro2" style="border-radius:5px" onclick="document.getElementById('output-intro2').style.display='block'; document.getElementById('show-intro2').style.display='none'; document.getElementById('hide-intro2').style.display='inline';">
  Mostra soluzione
</button>

<button id="hide-intro2" style="display:none; border-radius:5px" onclick="document.getElementById('output-intro2').style.display='none'; document.getElementById('show-intro2').style.display='inline'; document.getElementById('hide-intro2').style.display='none';">
  Nascondi soluzione
</button>

<div style="margin-top: 20px;"></div>

<div id="output-intro2" style="display:none;">

```python
s = "ciao"
n = 4
output = s*n
print(output)
```

*Nel caso non si fosse interessati a conservare l'output in una variabile e si volesse effettuare un passaggio in meno:*

```python
s = "ciao"
n = 4
print(s*n)
```
</div>

###### 3° esercizio:

Scrivere un programma che stampa il volume di una sfera avente raggio `r` a piacere. Importare il valore di Pi greco dal modulo `math`.

```{code-cell}
r = 0
```
```{tip}
Per utilizzare il modulo `math` è necessario importarlo. Consulta la [documentazione](https://docs.python.org/3/library/math.html) per trovare il comando Pi greco.
```

Partendo dal codice sopra, prova a risolvere l'esercizio:
<a href="https://www.programiz.com/python-programming/online-compiler/" target="_blank" style="text-decoration: none;">
  <div>
    <strong>Clicca qui per sviluppare il tuo codice!</strong><br>
  </div>
</a>

<div style="margin-top: 20px;"></div>

<button id="show-intro3" style="border-radius:5px" onclick="document.getElementById('output-intro3').style.display='block'; document.getElementById('show-intro3').style.display='none'; document.getElementById('hide-intro3').style.display='inline';">
  Mostra soluzione
</button>

<button id="hide-intro3" style="display:none; border-radius:5px" onclick="document.getElementById('output-intro3').style.display='none'; document.getElementById('show-intro3').style.display='inline'; document.getElementById('hide-intro3').style.display='none';">
  Nascondi soluzione
</button>

<div style="margin-top: 20px;"></div>

<div id="output-intro3" style="display:none;">

```python
import math
r = 10 #qualsiasi valore di r va bene
volume = 4/3 * math.pi * r**3
print(r)
```

*In alternativa, l'importazione diretta del comando `pi` può essere una soluzione, se non si ha necessità di usare altri comandi del modulo `math`:*

```python
from math import pi
r = 10 #qualsiasi valore di r va bene
volume = 4/3 * pi * r**3
print(r)
```
</div>

###### 4° esercizio:

Scrivere un programma che stampa al contrario una stringa lunga 4 caratteri scelta a piacere (es. se `s="lodi"`, il programma stampa `idol`).

```{code-cell}
s = "lodi"
```

Partendo dal codice sopra, prova a risolvere l'esercizio:
<a href="https://www.programiz.com/python-programming/online-compiler/" target="_blank" style="text-decoration: none;">
  <div>
    <strong>Clicca qui per sviluppare il tuo codice!</strong><br>
  </div>
</a>

<div style="margin-top: 20px;"></div>

<button id="show-intro4" style="border-radius:5px" onclick="document.getElementById('output-intro4').style.display='block'; document.getElementById('show-intro4').style.display='none'; document.getElementById('hide-intro4').style.display='inline';">
  Mostra soluzione
</button>

<button id="hide-intro4" style="display:none; border-radius:5px" onclick="document.getElementById('output-intro4').style.display='none'; document.getElementById('show-intro4').style.display='inline'; document.getElementById('hide-intro4').style.display='none';">
  Nascondi soluzione
</button>

<div style="margin-top: 20px;"></div>

<div id="output-intro4" style="display:none;">

```python
s = "lodi"
print(s[::-1])
```

</div>

###### 5° esercizio:

Supponete di correre 10 km in 42 min e 42 sec. Scrivere un programma che stampa la vostra velocità media in km/minuto, km/h, miglia/minuto e miglia/h.
- Calcolate quanti secondi ci sono in 42 minuti e 42 secondi.
- A quante miglia corrispondono 10km? (un miglio corrisponde a 1.61 km)
- La vostra velocità media è calcolata come distanza/tempo.

```{code-cell}
secondi = 0
```

Partendo dal codice sopra, prova a risolvere l'esercizio:
<a href="https://www.programiz.com/python-programming/online-compiler/" target="_blank" style="text-decoration: none;">
  <div>
    <strong>Clicca qui per sviluppare il tuo codice!</strong><br>
  </div>
</a>

<div style="margin-top: 20px;"></div>

<button id="show-intro5" style="border-radius:5px" onclick="document.getElementById('output-intro5').style.display='block'; document.getElementById('show-intro5').style.display='none'; document.getElementById('hide-intro5').style.display='inline';">
  Mostra soluzione
</button>

<button id="hide-intro5" style="display:none; border-radius:5px" onclick="document.getElementById('output-intro5').style.display='none'; document.getElementById('show-intro5').style.display='inline'; document.getElementById('hide-intro5').style.display='none';">
  Nascondi soluzione
</button>

<div style="margin-top: 20px;"></div>

<div id="output-intro5" style="display:none;">

```python
km = 10
miglia = 10/1.61
# calcolo quanti secondi corrispondono 42min e 42sec
tempo_sec = 42*60 + 42
tempo_min = tempo_sec/60
tempo_hour = tempo_min/60
vel_km_min = km/tempo_min
vel_km_hour = km/tempo_hour
vel_miglia_min = miglia/tempo_min
vel_miglia_hour = miglia/tempo_hour
print(vel_km_min, vel_km_hour, vel_miglia_min, vel_miglia_hour)
```

```{tip}
Il risultato che si ottiene dal `print` è poco comprensibile. Per avere un `print` più chiaro, si provi a sostituire con i seguenti `print`.
```

```python
print(f"La velocità media in km/min è: {vel_km_min} km/min")
print(f"La velocità media in km/h è: {vel_km_hour} km/h")
print(f"La velocità media in miglia/min è: {vel_miglia_min} miglia/min")
print(f"La velocità media in miglia/h è: {vel_miglia_hour} miglia/h")
```

```{note}
La lettera `f` subito dopo la prima `(` permette di inserire dinamicamente variabili all'interno di una stringa per la stampa, a patto che le variabili siano inserite dentro `{}`.
```

</div>

###### 6° esercizio:

Scrivere un programma che scambia i valori (scelti a piacere) legati ai due nomi `a` e `b` (deve funzionare per ogni valore iniziale di `a` e `b`). Es. se inizialmente `a = 7` e `b = 20`, alla fine `print(a,b)` stamperà 20 7.

```{code-cell}
a = 0
b = 0
```

Partendo dal codice sopra, prova a risolvere l'esercizio:
<a href="https://www.programiz.com/python-programming/online-compiler/" target="_blank" style="text-decoration: none;">
  <div>
    <strong>Clicca qui per sviluppare il tuo codice!</strong><br>
  </div>
</a>

<div style="margin-top: 20px;"></div>

<button id="show-intro6" style="border-radius:5px" onclick="document.getElementById('output-intro6').style.display='block'; document.getElementById('show-intro6').style.display='none'; document.getElementById('hide-intro6').style.display='inline';">
  Mostra soluzione
</button>

<button id="hide-intro6" style="display:none; border-radius:5px" onclick="document.getElementById('output-intro6').style.display='none'; document.getElementById('show-intro6').style.display='inline'; document.getElementById('hide-intro6').style.display='none';">
  Nascondi soluzione
</button>

<div style="margin-top: 20px;"></div>

<div id="output-intro6" style="display:none;">

```python
a = 7 #qualsiasi valore di a va bene
b = 20 #qualsiasi valore di b va bene
a, b = b, a
print(a, b)
```

*In alternativa, si potrebbe anche creare una terza variabile temporanea su cui appoggiare il valore di una delle due variabili durante il cambiamento. Il metodo precedente, però, è più veloce e non porta alla creazione di nessuna variabile futile.*

```python
a = 7 #qualsiasi valore di a va bene
b = 20 #qualsiasi valore di b va bene
c = a #si parcheggia il valore di a in c, così quando a diventa b possiamo ancora prendere il valore di a, che non si trova più in a ma solo in c
a = b
b = c
print(a, b)
```
</div>