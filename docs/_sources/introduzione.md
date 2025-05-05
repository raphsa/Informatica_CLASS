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
:tags: [thebe-run]

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
  <input type="submit" value="Verifica" style="background-color:#29313D; border-radius:5px">
  <button type="button" style="background-color:#29313D; border-radius:5px" onclick="resetQuiz('q1_intro', 'feedback1_intro')">Reset</button>
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
  <input type="submit" value="Verifica" style="background-color:#29313D; border-radius:5px">
  <button type="button" style="background-color:#29313D; border-radius:5px" onclick="resetQuiz('q2_intro', 'feedback2_intro')">Reset</button>
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
  <input type="submit" value="Verifica" style="background-color:#29313D; border-radius:5px">
  <button type="button" style="background-color:#29313D; border-radius:5px" onclick="resetQuiz('q3_intro', 'feedback3_intro')">Reset</button>
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
  <input type="submit" value="Verifica" style="background-color:#29313D; border-radius:5px">
  <button type="button" style="background-color:#29313D; border-radius:5px" onclick="resetQuiz('q4_intro', 'feedback4_intro')">Reset</button>
</form>

<div style="margin-top: 20px;"></div>

<p id="feedback4_intro"></p>

## Esercizi da svolgere

###### 1° esercizio:

Scrivere un programma che stampa il perimetro di un quadrato avente il lato `l = 3`.

```{code-cell}
l = 0
```

###### 2° esercizio:

Scrivere un programma che stampa `n` volte una stringa `s` a piacere (es. con `n = 4`, `s = "ciao"` stamperà ciaociaociaociao)

```{code-cell}
s = ""
n = 0
```

###### 3° esercizio:

Scrivere un programma che stampa il volume di una sfera avente raggio `r` a piacere. Importare il valore di Pi greco dal modulo `math`.

```{code-cell}
r = 0
```

###### 4° esercizio:

Scrivere un programma che stampa al contrario una stringa lunga 4 caratteri scelta a piacere (es. se `s="lodi"`, il programma stampa idol).

```{code-cell}
s = "lodi"
```

###### 5° esercizio:

Supponete di correre 10 km in 42 min e 42 sec. Scrivere un programma che stampa la vostra velocità media in km/minuto, km/h, miglia/minuto e miglia/h.
- Calcolate quanti secondi ci sono in 42 minuti e 42 secondi.
- A quante miglia corrispondono 10km? (un miglio corrisponde a 1.61 km)
- La vostra velocità media è calcolata come distanza/tempo.

```{code-cell}
secondi = 0
```

###### 6° esercizio:

Scrivere un programma che scambia i valori (scelti a piacere) legati ai due nomi `a` e `b` (deve funzionare per ogni valore iniziale di `a` e `b`). Es. se inizialmente `a = 7` e `b = 20`, alla fine `print(a,b)` stamperà 20 7.

```{code-cell}
a = 0
b = 0
```