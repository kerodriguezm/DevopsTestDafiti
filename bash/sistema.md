1. Escribe un comando para listar el espacio utilizado por cada partición de disco duro:
```shell
```df -h
```

2. Escribe un comando para mostrar la cantidad de núcleos de CPU con los que cuenta tu sistema:
```shell
```nproc --all
```

3. Escribe un comando para mostrar el PID del proceso `cron`, si éste se está ejecutando, junto al PID de su proceso padre:
```shell
```ps -e | grep cron
```

4. Escribe un comando para ver los puertos TCP/UDP abiertos por los procesos ejecutándose en background (podría requerir 
privilegios de root):
```shell
```sudo netstat -tu
```

5. Escribe un comando para ver la salida de `stdout` de un proceso identificado por el PID `1234` (podría requerir privilegios de root):
```shell
```ps -p 1234
```
