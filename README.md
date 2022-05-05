# Rankings
## Información:
Primero se define la variable "Ranking" con una lista vacía para que posteriormente podamos añadirle los elementos que vayan siendo rankeados.
  Luego usamos un for para el valor y el link saliente del diccionario anteriormente definido, donde salen los links, así va a iterar por todo el diccionario, dividiéndolo por valor y clave.
  Luego definimos "s" como saliente, y contamos cuántas veces existe el texto "https", se le suma uno porque al momento de dividir, se divide por cero y nos saldría un error.
  ```ranking = []

for valor, saliente in web.items():
    s = saliente.count("https")+1
    e = 0
 ```
  
  Dentro del for del inicio, usamos otro for para que este pueda iterar entre los links entrantes con una variable auxiliar la cual es "a" y le asigne un número a la variable "e" que posteriormente lo definimos con un valor de 0, cada vez que termine de contar los links, la variable "a" cambiará su valor nuevamente y podrá tomar nuevos valores y pueda iterar entre los links entrantes restantes:
  
    
```bash
for x in web.items():
     a = x.count(valor)
     e += a 
```

  A continuación, ejecutamoos el comando print tal que así:
  ```
  print(f"entrantes = {e}")
    print(f"salientes = {s}")
  ```
    
   Antes al empezar paréntesis se usa "f" para indicar un format, por eso luego definimos entrantes como {e} y salientes como {s}, así para que luego podamos operar:
   
  ``` rank = e/s```
   
   Luego de hacer la división, añadimos el resultado a la lista vacía que creamos en un inicio, añadiendo el rank (los números que indican la posición) y el valor (los links)
   
  ```ranking.append([rank, valor])```
   
   Luego, para ordenar los ranks de mayor a menor, se usa el comando "sorted" para ordenar las claves con sus valores y luego [::-1] para ordenarlo de mayor ranking a menor y se asigna todo eso a la variable "n"
   Finalmente, uso el comando "print" para imprimir con un string, "n", indicando cuál es el top 1 hasta el top 6, indicando sus respectivos valores y claves:
 ```  
 n = sorted(ranking)[::-1]
print("Top 1: ", str((n[0])))
print("Top 2: ", str((n[1])))
print("Top 3: ", str((n[2])))
print("Top 4: ", str((n[3])))
print("Top 5: ", str((n[4])))
print("Top 6: ", str((n[5])))
   
```
