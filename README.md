# Gentleman_Javascript_Tournament
```javascript

// 1-Dado un array de números, escribir una función que encuentre el número más grande.
const mayor = [1, 2, 3].reduce((acc, element) =>
  element > acc ? element : acc
);

// 2-Dado un array de números, escribir una función que encuentre el número más pequeño.
const minor = [1, 2, 3].reduce((acc, element) =>
  element < acc ? element : acc
);

// 3-Dado un array de números, escribir una función que calcule la suma de todos los elementos.
const sum = [1, 2, 3].reduce((acc, element) => acc + element);

// 4-Dado un array de números, escribir una función que calcule el promedio de todos los elementos.
const prom = sum / [1, 2, 3].length;

// 5-Dado un string, escribir una función que invierta el orden de las palabras en el string.
const resultString = "hola".split("").reverse().join("");

// 6-Dado un string, escribir una función que encuentre la palabra más larga en el string.
const resultLonger = "hola mundo"
  .split(" ")
  .reduce((acc, element) => (element.length > acc.length ? element : acc));
  
// 7-Dado un string y un número n, escribir una función que trunque el string a n caracteres y agregue "..." al final.
const n = 5;
const truncatedResult =  "hola gentleman programming".slice(0, n);
const truncatedText = truncatedResult.length < n ? truncatedResult : `${truncatedResult}...`;

// 8-Dado un array de números, escribir una función que elimine todos los números duplicados y devuelva el array resultante sin duplicados.
const setOfArray = new Set();
[1, 1, 1, 1, 2].forEach((n) => setOfArray.add(n));

// 9-Dado un array de números y un número objetivo, escribir una función que encuentre dos números en el array que sumen el número objetivo.
const checkNumbers = (arrayOfNumbers, n) => {
  let secondNumber = null;
  const result = arrayOfNumbers.find((e, index) =>
    arrayOfNumbers.slice(index).find((element2) => {
      const isTrue = element2 + e === n;
      if (isTrue) secondNumber = element2;
      return isTrue;
    })
  );
  return {result, secondNumber};
};
const test = checkNumbers([1, 2, 3], 3);
```
