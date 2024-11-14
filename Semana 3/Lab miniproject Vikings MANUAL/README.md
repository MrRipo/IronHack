![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Mini Project | Vikingos (Vikings)

## Introducción

Los Vikingos y los Sajones están en guerra. Ambos son Soldados, pero tienen sus propios métodos para luchar. ¡Los Vikingos han sido transportados a Python. YAY!!

En este laboratorio trabajarás con el concepto de herencia en Python.

### Empezando

Encontrarás los siguientes archivos en la carpeta de este laboratorio:

- `vikingsClasses.py`
- `1-testSoldier.py`
- `2-testVikings.py`
- `3-testSaxons.py`
- `4-testWar.py`

Eres libre de usar cualquiera de los editores de código que tengas para abrir estos archivos.

### Pregunta del desafío

Modifica el archivo `vikingsClasses.py` para que todas las pruebas sean correctas.

## Entrega

- Modifica `vikingsClasses.py` y guarda tus cambios.

## Pruebas

La mejor manera de saber cómo va nuestro código es trabajar con pruebas. Probarás el archivo `vikingsClases.py` paso a paso.

**Solo** estarás **editando** el archivo `vikingsClasses.py`. Los archivos que **ejecutarás** para probar tu código son los siguientes: 1-testsSoldier.py, 2-testsVikings.py, 3-testsSaxons.py y 4-testsWar.py, dependiendo de cuánto hayas avanzado en tu código.

Entonces, digamos que ya has creado la clase para los Soldados.

1. Escribes tu código.
2. Asegúrate de guardar los cambios en tu editor.
3. En tu terminal, ejecuta el archivo de prueba para esa clase.

```bash
$ python3 1-testSoldier.py --v
```

### Prueba correcta

Cuando todas las pruebas sean correctas, recibirás el siguiente mensaje en la terminal.

```
$ python3 1-testSoldier.py --v

testAttackHasNoParams (__main__.TestSoldier) ... ok
testAttackRetunsStrength (__main__.TestSoldier) ... ok
testAttackShouldBeFunction (__main__.TestSoldier) ... ok
testCanReceiveDamage (__main__.TestSoldier) ... ok
testConstructorSignature (__main__.TestSoldier) ... ok
testHealth (__main__.TestSoldier) ... ok
testReceiveDamageReturnNone (__main__.TestSoldier) ... ok
testReceivesDamage (__main__.TestSoldier) ... ok
testReceivesDamageHasParams (__main__.TestSoldier) ... ok
testStrength (__main__.TestSoldier) ... ok

----------------------------------------------------------------------
Ran 10 tests in 0.001s

OK
```

### Prueba fallida

Cuando alguna prueba sea incorrecta, recibirás el siguiente mensaje en la terminal. Significa que debes seguir haciendo cambios en el archivo `vikingsClasses.py`.

```
$ python3 1-testSoldier.py --v

testAttackHasNoParams (__main__.TestSoldier) ... ok
testAttackRetunsStrength (__main__.TestSoldier) ... ok
testAttackShouldBeFunction (__main__.TestSoldier) ... ok
testCanReceiveDamage (__main__.TestSoldier) ... FAIL
testConstructorSignature (__main__.TestSoldier) ... ok
testHealth (__main__.TestSoldier) ... ok
testReceiveDamageReturnNone (__main__.TestSoldier) ... ok
testReceivesDamage (__main__.TestSoldier) ... ok
testReceivesDamageHasParams (__main__.TestSoldier) ... ok
testStrength (__main__.TestSoldier) ... ok

======================================================================
FAIL: testCanReceiveDamage (__main__.TestSoldier)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "1-testsSoldier.py", line 44, in testCanReceiveDamage
    self.assertEqual(self.soldier.health, self.health + 50)
AssertionError: 250 != 350

----------------------------------------------------------------------
Ran 10 tests in 0.001s
```

## Ejercicio

![](https://i.imgur.com/5TPElt8.jpg)

---

**Escribe el código**

Ahora tenemos que escribir el código correcto en el archivo `vikingsClasses.py` para hacer que la prueba pase. El código inicial que encontrarás en el archivo es el siguiente:

```
# Soldier
class Soldier:

# Viking
class Viking:

# Saxon
class Saxon:

# War
class War:
```

En este caso, la prueba dice que la función constructora de Soldier debe recibir 2 argumentos (salud y fuerza), por lo que tenemos que escribir el código correcto que pase esta prueba. Hagamos que la función constructora de `Soldier` reciba dos argumentos:

```
# Soldier
class Soldier:
    def __init__(self, health, strength):
        # add code here

# Viking
class Viking:

# Saxon
class Saxon:

# War
class War:

```

### Soldier

Modifica la función constructora de `Soldado` y añade 2 métodos a su prototipo: `attack()`, y `receiveDamage()`.

#### constructor function


- Debe recibir **2 argumentos** (salud y fuerza).
- Debe recibir la propiedad **`salud`** como su **primer argumento**.
- Debe recibir la propiedad **`fuerza`** como su **segundo argumento**.

#### `attack()` method

- Debe ser una función.
- Debe recibir **0 argumentos**.
- Debe devolver **la propiedad `fuerza` del `Soldado`**.

#### `receiveDamage()` method

- Debe ser una función.
- Debe recibir **1 argumento** (el daño).
- Debe restar el daño recibido de la propiedad `salud`.
- **No debe devolver** nada.

---

### Viking

Un `Viking` es un `Soldier` con una propiedad adicional, su `name`. Tienen un método `receiveDamage()` diferente y un nuevo método, `battleCry()`.

#### inheritance

- `Viking` debe heredar de`Soldier`

#### constructor function

- Debe recibir **3 argumentos** (name, health y strength).
- Debe recibir la propiedad **`name`** como su **primer argumento**.

#### `attack()` method

- Debe ser una función.
- Debe recibir **0 argumentos**.
- Debe devolver **"Odin Owns You All!"**.

#### `receiveDamage()` method

(Este método necesita ser **reimplementado** para `Vikingo` porque la versión de `Vikingo` necesita tener valores de retorno diferentes.)

- debe ser una función
- debe recibir **1 argumento** (el daño)
- debe restar el daño recibido de la propiedad `health`
- **si el `Viking` sigue vivo**, debe devolver **"NOMBRE ha recibido PUNTOS DE DAÑO puntos de daño"**
- **si el `Viking` muere**, debe devolver **"NOMBRE ha muerto en acto de combate"**

#### `battleCry()` method

[Aprende más sobre los gritos de batalla](http://www.artofmanliness.com/2015/06/08/battle-cries/).

- debe ser una función
- debe recibir **0 argumentos**
- debe devolver **"¡Odin os posee a todos!"**

---

### Saxon

Un `Saxon` es un tipo de `Soldier` más débil. A diferencia de un `Viking`, un `Saxon` no tiene nombre. Su método `receiveDamage()` también será diferente al de la versión original de `Soldier`.

Modifica la función constructora de `Saxon`, haz que herede de `Soldier` y reimplementa el método `receiveDamage()` para `Saxon`.

#### inheritance

- `Saxon` hereda de `Soldier`

#### constructor function
- debe recibir **2 argumentos** (health y strength)
- debe recibir la propiedad **`health`** como su **primer argumento**
- debe recibir la propiedad **`strength`** como su **segundo argumento**


#### Método `attack()`

(Este método debe ser **heredado** de `'Soldier'`, no es necesario reimplementarlo.)

- debe ser una función
- debe recibir **0 argumentos**
- debe devolver **la propiedad `'strength'` del `'Saxon'`**

#### Método `receiveDamage()`

(Este método necesita ser **reimplementado** para `'Saxon'` porque la versión de `'Saxon'` necesita tener valores de retorno diferentes.)

- debe ser una función
- debe recibir **1 argumento** (el daño)
- debe restar el daño recibido de la propiedad `'health'`
- **si el 'Saxon' sigue vivo**, debe devolver _**"Un 'Saxon' ha recibido PUNTOS DE DAÑO puntos de daño"**_
- **si el 'Saxon' muere**, debe devolver _**"Un 'Saxon' ha muerto en combate"**_

---

### Guerra

¡Ahora llegamos a lo bueno: GUERRA! Nuestra función constructora `'War'` nos permitirá tener un ejército de `'Viking'` y un ejército de `'Saxon'` que luchan entre sí.

Modifica el constructor de `'War'` y añade 5 métodos a su prototipo:

- `'addViking()'`
- `'addSaxon()'`
- `'vikingAttack()'`
- `'saxonAttack()'`
- `'showStatus()'`

#### Función constructora

Cuando creamos una `'War'` por primera vez, los ejércitos deben estar vacíos. Añadiremos soldados a los ejércitos más tarde.

- debe recibir **0 argumentos**
- debe asignar un array vacío a la propiedad `'vikingArmy'`
- debe asignar un array vacío a la propiedad `'saxonArmy'`

#### Método `'addViking()'`

Añade 1 `'Viking'` al `'vikingArmy'`. Si quieres un ejército de 10 `'Viking'`, necesitas llamar a esto 10 veces.

- debe ser una función
- debe recibir **1 argumento** (un objeto `'Viking'`)
- debe añadir el `'Viking'` recibido al ejército
- **no debe devolver** nada

#### Método `'addSaxon()'`

La versión `'Saxon'` de `'addViking()'`.

- debe ser una función
- debe recibir **1 argumento** (un objeto `'Saxon'`)
- debe añadir el `'Saxon'` recibido al ejército
- **no debe devolver** nada

#### Método `'vikingAttack()'`

Un `'Saxon'` (elegido al azar) tiene su método `'receiveDamage()'` llamado con el daño igual a la `'strength'` de un `'Viking'` (también elegido al azar). Esto debería realizar solo un ataque y el `'Saxon'` no tiene oportunidad de contraatacar.

- debe ser una función
- debe recibir **0 argumentos**
- debe hacer que un `'Saxon'` `'receiveDamage()'` igual a la `'strength'` de un `'Viking'`
- debe eliminar a los sajones muertos del ejército
- debe devolver **el resultado de llamar a `'receiveDamage()'` de un `'Saxon'`** con la `'strength'` de un `'Viking'`

#### Método `'saxonAttack()'`

La versión `'Saxon'` de `'vikingAttack()'`. Un `'Viking'` recibe el daño igual a la `'strength'` de un `'Saxon'`.

- debe ser una función
- debe recibir **0 argumentos**
- debe hacer que un `'Viking'` `'receiveDamage()'` igual a la `'strength'` de un `'Saxon'`
- debe eliminar a los vikingos muertos del ejército
- debe devolver **el resultado de llamar a `'receiveDamage()'` de un `'Viking'`** con la `'strength'` de un `'Saxon'`

#### Método `'showStatus()'`

Devuelve el estado actual de la `'War'` basado en el tamaño de los ejércitos.

- debe ser una función
- debe recibir **0 argumentos**
- **si el array de `'Saxon'` está vacío**, debe devolver _**"¡Los Vikingos han ganado la guerra del siglo!"**_
- **si el array de `'Viking'` está vacío**, debe devolver _**"Los Sajones han luchado por sus vidas y sobreviven otro día..."**_
- **si hay al menos 1 `'Viking'` y 1 `'Saxon'`**, debe devolver _**"Los Vikingos y los Sajones todavía están en plena batalla."**_

## BONUS

Crea un juego utilizando las clases que definiste. Para esto, necesitarás:
- Crear un nuevo `file.py`
- Importar las clases que definiste anteriormente
- Definir funciones para crear el flujo de trabajo del juego: por ejemplo, funciones para crear equipos (quizás puedas crear equipos aleatorios con los nombres de tus compañeros de clase), ejecutar el juego, etc.

## Entregables

- REQUERIDO: `vikingsClases.py` modificado con tu solución a la pregunta del desafío.

## Recursos

- https://docs.python.org/3/library/unittest.html
- https://www.python-course.eu/python3_inheritance.php

## Desafío Adicional para los Nerds

Puedes intentar hacer tus propias pruebas para tu código creando otro archivo de prueba.