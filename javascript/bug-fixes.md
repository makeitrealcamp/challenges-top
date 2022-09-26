# Bug Fixes

## Fix Error: manipulación de arreglos
¡Ayuda a corregir todos los errores en la función `incrementItems`! ¡Está destinado a agregar 1 a cada elemento en el arreglo!

```js
function incrementItems(arr) {
  for (let i = 0; i < array.length; i++) {
    arr[i] === arr[i] + 1
  }

  return array
}
```
| Test Case                        | Expected        |
|----------------------------------|-----------------|
| incrementItems([0, 1, 2, 3])     | [1, 2, 3, 4]    |
| incrementItems([2, 4, 6, 8])     |  [3, 5, 7, 9]   |
| incrementItems([-1, -2, -3, -4]) | [0, -1, -2, -3] |

## Fix Error: Valor vs. Referencia de Tipos
Cree una función que devuelva `true` si dos arreglos contienen valores idénticos y `false` en caso contrario.

Para resolver esta pregunta, tu amigo escribe el siguiente código:

```js
function checkEquals(arr1, arr2) {
if (arr1 === arr2) {
  return true
 } else {
  return false
 }
}
```

Pero probando el código, ves que algo no está del todo bien. Ejecutar el código arroja los siguientes resultados:

```js
checkEquals([1, 2], [1, 3]) ➞ false
// Good so far...

checkEquals([1, 2], [1, 2]) ➞ false
// Yikes! What happened?
```

Reescribe el código de tu amigo para que verifique correctamente si dos arreglos son iguales. Para ser iguales, los arreglos deben tener los mismos elementos en el mismo orden.

Las siguientes pruebas deben pasar:

| Test Case                          | Expected |
|------------------------------------|----------|
| checkEquals([1, 2], [1, 3])        | `false`  |
| checkEquals([1, 2], [1, 2])        | `true`   |
| checkEquals([4, 5, 6], [4, 5, 6])  | `true`   |
| checkEquals([4, 7, 6], [4, 5, 6])  | `false`  |
| checkEquals([4, 7, 6], [4, 6, 7])  | `false`  |

## Fix error: Aplanando un arreglo

Estoy tratando de escribir una función para aplanar una matriz de subarreglos en un arreglo. (Supongamos que no sé que hay un método .flat() en el prototipo de Array).

En otras palabras, quiero transformar esto: `[[1, 2], [3, 4]]` en `[1, 2, 3, 4]`.

Aquí está mi código:

```js
function flatten(arr) {
  const result = []
  for (let i = 0; i < arr.length; i++) {
    result.concat(arr[i])
  }
  return result
}
```
Pero... ¡no parece estar funcionando! Arregle mi código para que aplane correctamente la matriz.

| Test Case                                | Expected                      |
|------------------------------------------|-------------------------------|
| flatten([[1, 2], [3, 4]])                | `[1, 2, 3, 4]`                |
| flatten([[1], [2], [3], [4]])            | `[1, 2, 3, 4]`                |
| flatten([["a", "b"], ["c", "d"]])        | `["a", "b", "c", "d"]`        |
| flatten([[true, false], [false, false]]) | `[true, false, false, false]` |

## Fix error: Clonar un arreglo

El siguiente código intenta agregar un clon de una arreglo a sí mismo. No hay ningún mensaje de error, pero los resultados no son los esperados. ¿Puedes arreglar el código?

```js
function clone(arr) {
  arr.push(arr)
  return arr
}
```

| Test Case                  | Expected                                   |
|----------------------------|--------------------------------------------|
| clone([1, 1])              | `[1, 1, [1, 1]]`                           |
| clone([1, 2, 3])           | `[1, 2, 3, [1, 2, 3]]`                     |
| clone(["x", "y"])          | `["x", "y", ["x", "y"]]`                   |
| clone([true, false, true]) | `[true, false, true, [true, false, true]]` |


## Fix error: Devolución de precios válidos
Ha habido un problema de datos maestros que afectó los precios de los productos. Compruebe si cada producto tiene un precio válido (entero o flotante, y mayor o igual a cero). Los productos con un precio de 0 son gratuitos y cuentan como un precio válido.

```js
function hasValidPrice(product) {
  return (product && product.price && product.price >= 0)
}
```

El valor de retorno debe ser un booleano.

| Test Case                                             | Expected |
|-------------------------------------------------------|----------|
| hasValidPrice({ "product": "Milk", price: 1.50 })     | `true`   |
| hasValidPrice({ "product": "Cheese", price: -1 })     | `false`   |
| hasValidPrice({ "product": "Eggs", price: 0 })        | `true`   |
| hasValidPrice({ "product": "Cereals", price: "3.0" }) | `false`   |
| hasValidPrice()                                       | `false`   |

Ejecute los `test case` primero para ver los resultados antes de realizar cambios y comprenda por qué los huevos devuelven 0 y la harina devuelve `undefined`.

## Hints 🇺🇸🤔

#### ¿Por qué los huevos son 0?
.denruter si 0 erofereht os ,`ecirp.tcudorp` ta eulav yslaf a si 0 .noitidnoc tsal eht ro noitidnoc yslaf tsal eht fo tluser eht si eulav denruter eht ,&& hguorht snoitidnoc gnigrem nehW (https://www.textreverse.com)

#### ¿Por qué la harina es `undefined`?
.denruter si denifednu erofereht os ,denifednu si `ecirp.tcudorp` .noitidnoc tsal eht ro noitidnoc yslaf tsal eht fo tluser eht si eulav denruter eht ,&& hguorht snoitidnoc gnigrem nehw ,ereh emaS (https://www.textreverse.com)
