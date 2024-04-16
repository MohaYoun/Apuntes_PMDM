# Apuntes_PMDM
Cosas interesantes y fallos cometidos.
### Ejercicio 1 de pract junio
1. En esta parte del codigo lo hemos generado dentro de un click listener,
hemos generado un Array de numeros y se lo hemos pasado a la otra actividad.
```
    int tamArry = Integer.parseInt(etNumero.getText().toString());
    ArrayList<String> nums = new ArrayList<>();
    for (int i = 0; i < tamArry; i++) {
        num_random = (int) (Math.random() * NUM_MAX);
        nums.add(String.valueOf(num_random));
    }
    Intent intent = new Intent(this, ej1Recep.class);
    intent.putExtra(NUMS_ARRAY, nums);
```
Recogida del array.
```
lista = (ArrayList<String>)getIntent().getSerializableExtra(ej1Main09042024.NUMS_ARRAY);
```
Fallos cometidos:
 - **Crear los public static final String, y darles el mismo valor.**
