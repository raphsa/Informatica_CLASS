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

# Funzioni

In Python, la definizione di una funzione parte da 5 semplici componenti. Nella riga iniziale devono essere indicati:
- sigla che caratterizza la funzione (`def`), 
- nome che si decide di assegnare alla funzione,
- parametri che caratterizzano una funzione, dentro una parentesi tonda e separati da virgola,
- i `:` alla fine della riga, per poter procedere con il corpo della funzione, costituito da uno o più comandi
Nella riga conclusiva, indendata rispetto alla riga iniziale (quindi applicando un rientro verso destra), deve essere indicato:
- il comando `return`, seguito dall'espressione o risultato che si vuole venga restituita quando si chiama la funzione.

Un esempio di sintassi di una funzione con due parametri, senza alcun comando al suo interno, è il seguente:

```python
def <nome funzione>(<parametro1>,<parametro2>):
    return <espressione>
```

L'utilità di una funzione sta nel potere applicare una serie di comandi a tanti diversi oggetti (ad esempio, potremmo volere trovare il quadruplo di diversi numeri). Il ruolo dei parametri è proprio questo: comportarsi come una variabile, a cui ogni volta si assegna un valore a nostra discrezione.

Di seguito, un esempio su come si potrebbe sviluppare la funzione, che chiameremo quadr, per generare il quadruplo di un numero:

```python
def quadr(x):
    q = 4*x
    return q
```

In questo modo, per ogni valore che decidiamo di verificare, la funzione ci restituirà il valore di `q`, che altro non è che il quadruplo del nostro numero.

Di seguito, prova tu stesso giocando con diversi numeri! (Premi il tasto **run**) 

```{code-cell}
:tags: [thebe-run]

# NON MODIFICARE LA FUNZIONE, MA SOLO IL NUMERO ALL'INTERNO DI print()
def quadr(x):
    q = 4*x
    return q

print(quadr(5))
```

## Link utili

Slide di teoria sulle funzioni:

<a href="https://virtuale.unibo.it/mod/resource/view.php?id=1836009" target="_blank" style="text-decoration: none;">
  <div style="border: 2px solid #ddd; padding: 16px; border-radius: 10px; background-color: #f0f8ff; text-align: center; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    📎 <strong>Teoria sulle funzioni</strong><br>
    <small>slide del professore da Virtuale</small>
  </div>
</a>

<div style="margin-top: 20px;"></div>

Esercizi sulle funzioni:

<a href="https://virtuale.unibo.it/mod/resource/view.php?id=1836012" target="_blank" style="text-decoration: none;">
  <div style="border: 2px solid #ddd; padding: 16px; border-radius: 10px; background-color: #f0f8ff; text-align: center; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    📎 <strong>Esercizi senza soluzioni</strong><br>
    <small>slide del professore da Virtuale</small>
  </div>
</a>

## Esercizi

Di seguito, qualche semplice esercizio di lettura per cominciare a familiarizzare con l'utilizzo delle funzioni nel linguaggio Python:

###### Esercizio di lettura 1:
```{code-cell}
:tags: [thebe-run]

def moltiplic_stringa(stringa):
  risultato = stringa*4
  return risultato
```

Cosa restituisce il comando `print(moltiplic_stringa("prova"))`?

<form onsubmit="checkAnswer(event, 'q1_funz', 'provaprovaprovaprova', 'feedback1_funz')">
  <input type="radio" name="q1_funz" value="Errore"> Errore<br>
  <input type="radio" name="q1_funz" value="prova4"> prova4<br>
  <input type="radio" name="q1_funz" value="provaprovaprovaprova"> provaprovaprovaprova<br>
  <input type="radio" name="q1_funz" value="risultato"> risultato<br>
  <br>
  <input type="submit" value="Verifica" style="background-color:#29313D; border-radius:5px">
  <button type="button" style="background-color:#29313D; border-radius:5px" onclick="resetQuiz('q1_funz', 'feedback1_funz')">Reset</button>
</form>

<div style="margin-top: 20px;"></div>

<p id="feedback1_funz"></p>

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
def funz_decina(numero):
  risultato = numero + 10
  return "risultato"
```

Cosa restituisce il comando `print(funz_decina(5))`?

<form onsubmit="checkAnswer(event, 'q2_funz', 'risultato', 'feedback2_funz')">
  <input type="radio" name="q2_funz" value="50"> 50<br>
  <input type="radio" name="q2_funz" value="15"> 15<br>
  <input type="radio" name="q2_funz" value="510"> 510<br>
  <input type="radio" name="q2_funz" value="risultato"> risultato<br>
  <br>
  <input type="submit" value="Verifica" style="background-color:#29313D; border-radius:5px">
  <button type="button" style="background-color:#29313D; border-radius:5px" onclick="resetQuiz('q2_funz', 'feedback2_funz')">Reset</button>
</form>

<div style="margin-top: 20px;"></div>

<p id="feedback2_funz"></p>

###### Esercizio di lettura 3:
```{code-cell}
def somma_elem(elemento1, elemento2):
  risultato = elemento1+elemento2
  return risultato
```

Cosa restituisce il comando `print(somma_elem("elemento2", "3"))`?

<form onsubmit="checkAnswer(event, 'q3_funz', 'elemento23', 'feedback3_funz')">
  <input type="radio" name="q3_funz" value="elemento23"> elemento23<br>
  <input type="radio" name="q3_funz" value="elemento2elemento2elemento2"> elemento2elemento2elemento2<br>
  <input type="radio" name="q3_funz" value="elemento2+3"> elemento2+3<br>
  <input type="radio" name="q3_funz" value="3elemento2"> 3elemento2<br>
  <br>
  <input type="submit" value="Verifica" style="background-color:#29313D; border-radius:5px">
  <button type="button" style="background-color:#29313D; border-radius:5px" onclick="resetQuiz('q3_funz', 'feedback3_funz')">Reset</button>
</form>

<div style="margin-top: 20px;"></div>

<p id="feedback3_funz"></p>

###### Esercizio di lettura 4:
```{code-cell}
def divisione(x, y):
  zero = x/y
  return 0
```

Cosa restituisce il comando `print(divisione(8, 4))`?

<form onsubmit="checkAnswer(event, 'q4_funz', '0', 'feedback4_funz')">
  <input type="radio" name="q4_funz" value="2"> 2<br>
  <input type="radio" name="q4_funz" value="due"> due<br>
  <input type="radio" name="q4_funz" value="0"> 0<br>
  <input type="radio" name="q4_funz" value="zero"> zero<br>
  <br>
  <input type="submit" value="Verifica" style="background-color:#29313D; border-radius:5px">
  <button type="button" style="background-color:#29313D; border-radius:5px" onclick="resetQuiz('q4_funz', 'feedback4_funz')">Reset</button>
</form>

<div style="margin-top: 20px;"></div>

<p id="feedback4_funz"></p>



## Esercizi svolti in aula

## Esercizi aggiuntivi

## Trova l'errore

<button id="show-btn" style="background-color:#29313D; border-radius:5px" onclick="document.getElementById('output-container').style.display='block'; document.getElementById('show-btn').style.display='none'; document.getElementById('hide-btn').style.display='inline';">
  Mostra soluzione
</button>

<button id="hide-btn" style="display:none; background-color:#29313D; border-radius:5px" onclick="document.getElementById('output-container').style.display='none'; document.getElementById('show-btn').style.display='inline'; document.getElementById('hide-btn').style.display='none';">
  Nascondi soluzione
</button>

<div style="margin-top: 20px;"></div>

<div id="output-container" style="display:none;">

```{code-cell}
:tags: [thebe-run, remove-input]

print("Ciao, questo è l'output")
```
</div>
