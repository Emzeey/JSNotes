DeKa: https://github.com/DeKa3331/notesforJS

## Dodanie do klasy 'string' nowej metody:
```JS
String.prototype.mirror = function () {
  return this.split('').reverse().join('');
};

// Przykład użycia:
console.log("Ala ma kota".mirror()); // "atok am alA"

```
To samo ale inaczej:
```JS
String.prototype.mirror = function () {
  let new_str = ""
  for(let i=this.length-1; i >= 0; i--) {
  	new_str += this[i]
  }
  return new_str;
};

console.log("Ala ma kota".mirror());
```

## Metoda klasy wykorzystująca mechanizm 'clousers':
```JS
function createCounter() {
  let count = 0; // prywatna zmienna dostępna tylko wewnątrz closure

  return function() {
    count++;
    return count;
  };
}

// Przykład użycia:
const counter1 = createCounter();
console.log(counter1()); // 1
console.log(counter1()); // 2

const counter2 = createCounter();
console.log(counter2()); // 1 (niezależny licznik)
```
Clousers (domknięcia) - to sytuacja, gdy funkcja „zapamiętuje” zmienne ze swojego otoczenia (z zakresu, w którym została stworzona), nawet jeśli zostanie wywołana później, poza tym zakresem.
