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

Esercizi sulle funzioni:

<a href="https://virtuale.unibo.it/mod/resource/view.php?id=1836012" target="_blank" style="text-decoration: none;">
  <div style="border: 2px solid #ddd; padding: 16px; border-radius: 10px; background-color: #f0f8ff; text-align: center; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    📎 <strong>Esercizi senza soluzioni</strong><br>
    <small>slide del professore da Virtuale</small>
  </div>
</a>

## Esercizi svolti in aula

## Esercizi aggiuntivi

## Trova l'errore
