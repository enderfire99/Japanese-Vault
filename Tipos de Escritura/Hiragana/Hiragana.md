---
tipo: Escritura
descripcion: Letra curva
origen: "[[Kanji]]"
---
```button
name Nuevo Caracter Puro
type note(Default, split) template
action Nueva Letra Hiragana Pura
templater true
color purple
folder Tipos de Escritura/Hiragana/Letras
prompt true
```

```button
name Nuevo Caracter Impuro
type note(Default, split) template
action Nueva Letra Hiragana Impuro
templater true
color purple
folder Tipos de Escritura/Hiragana/Letras
prompt true
```

```button
name Nueva Palabra
type note(Default, split) template
action Nueva Palabra Hiragana
templater true
color blue
folder Tipos de Escritura/Hiragana/Palabras
prompt true
```

## Silabario

![[Hiragana Silabario.gif]]

## Alfabeto puro

```dataview 
TABLE pronunciacion
FROM "Tipos de Escritura"
WHERE alfabeto = [[Hiragana]]
AND sonido = [[Seion]]
```


## Alfabeto impuro

```dataview 
TABLE pronunciacion, derivacion
FROM "Tipos de Escritura"
WHERE alfabeto = [[Hiragana]]
AND sonido = [[Dakuon]]
```

## Palabras
```dataview 
TABLE letras, significados, pronunciacion 
FROM "Tipos de Escritura"
WHERE origen = [[Hiragana]]
AND tipo = "Palabra"
```
