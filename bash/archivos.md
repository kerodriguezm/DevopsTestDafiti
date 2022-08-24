1. Escribe un comando para ver las últimas dos líneas del archivo `lorem-ipsum.txt`, ubicado en el directorio `bash/`:
```shell
```tail -n2 ../bash/lorem-ipsum.txt
```

2. Escribe un comando para mostrar la cantidad de palabras que contiene cada línea del archivo `lorem-ipsum.txt`, ubicado en el directorio `bash/`:
```shell
```awk '{c++} {print "line",c ":", NF}' ../bash/lorem-ipsum.txt
```

1. Escribe un comando para ver el contenido del archivo `lorem-ipsum.txt`, ubicado en el directorio `bash`, sin los caracteres ***punto*** `.` y ***coma*** `,`:
```shell
```cat ../bash/lorem-ipsum.txt | tr -d '.,'
```

4. Escribe un comando para listar todos los directorios dentro de este repositorio (no recursivo):
```shell
```find /$HOME/prueba-tecnica/ -maxdepth 1 

```

5. Esribe un comando para ordenar los directorios listados, por tamaño:
```shell
```ls -ltr
```
 
