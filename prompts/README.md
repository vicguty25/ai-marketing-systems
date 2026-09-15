# Prompts operativos

Cuatro prompts, no cuarenta. Cada uno resuelve un cuello de botella concreto del
[sistema](../sistema) y viene con **la forma en que falla**, porque saber dónde
falla un prompt es lo que lo hace usable.

Regla común a todos: **la IA interroga y genera volumen; la persona decide.**
Ningún prompt aquí produce una entrega final.

---

## 1. Interrogar un brief

Cuando el brief está lleno pero vago. El modelo no lo completa: lo ataca.

```
Eres un director de marketing escéptico. Te paso un brief de campaña.

No lo mejores. No escribas copy. Tu único trabajo es encontrar dónde es tan
vago que dos personas podrían ejecutarlo de forma distinta.

Para cada respuesta vaga:
1. Cita la frase exacta.
2. Explica qué dos cosas distintas podría significar.
3. Haz UNA pregunta concreta que lo resolvería.

Si la métrica declarada no mide el objetivo declarado, dilo primero.

BRIEF:
[pegar]
```

**Cómo falla:** tiende a pedir más detalle en todo, incluido lo que ya está
claro. Si señala más de cinco cosas, está rellenando — quédate con las tres
primeras.

---

## 2. Generar ángulos incompatibles

```
Producto: [qué es, en una frase]
Usuario: [la persona concreta del brief]
Creencia actual: [lo que hoy piensa y hay que mover]

Dame 5 ángulos de campaña. Cada uno tiene que atacar una creencia DISTINTA.

Restricción: los 5 deben ser mutuamente excluyentes. Si dos pudieran usarse a
la vez como mensaje principal sin contradecirse, no cuentan como dos.

Por cada ángulo, una línea: qué creencia ataca y qué habría que renunciar a
decir si se elige.
```

**Cómo falla:** el fallo predecible es devolver cinco formas de decir lo mismo.
Prueba de control: intenta usar dos a la vez. Si puedes, vuelve a pedirlos.

---

## 3. Variantes de copy con la restricción del canal

```
Ángulo elegido: [uno solo]
Canal: [feed | story | landing | email | whatsapp]
Restricción física del canal: [ver sistema/03-copy.md]
Voz: [dos o tres adjetivos + un ejemplo de algo que esta persona SÍ diría]

Dame 10 variantes. Rango completo: de muy sobrio a muy directo.
No expliques las variantes.
```

**Cómo falla:** sale correcto y sin voz. Se usa como borrador para reescribir,
nunca como entrega — si se publica tal cual, el canal se vuelve genérico en unas
tres semanas y deja de distinguirse de cualquier otro.

---

## 4. Agrupar respuestas abiertas en temas

Solo con volumen. Con decenas de comentarios al mes, unas reglas de palabras
clave rinden más y son corregibles — está implementado así, y explicado, en
[Voz](https://github.com/vicguty25/voz-cliente-nps/blob/main/src/lib/temas.ts).

```
Te paso comentarios de clientes.

Agrúpalos en máximo 6 temas. Por cada tema: nombre corto, cuántos comentarios y
DOS citas textuales sin editar.

No resumas los comentarios. No suavices las quejas.
Al final, lista aparte los que no encajaron en ningún tema.

COMENTARIOS:
[pegar]
```

**Cómo falla:** suaviza. Una queja dura se convierte en «oportunidad de mejora»
y deja de doler, que es justo lo que la hacía útil. Los comentarios que no
encajan son la parte más valiosa de la respuesta: ahí está lo que no sabías que
estabas buscando.
