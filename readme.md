DeKa: https://github.com/DeKa3331/notesforJS

### Dodanie do klasy 'string' nowej metody:
```JS
String.prototype.mirror = function () {
  return this.split('').reverse().join('');
};

// Przykład użycia:
console.log("Ala ma kota".mirror()); // "atok am alA"

```
