# Ejercicios de Bash: ¿Qué pasa si...?

## Ejercicio 1: Estructura de partida

**Estructura inicial:**
```
proyecto/
|---- datos/
|   |---- archivo1.txt
|   |__-- archivo2.txt
|---- informe/
|   |__-- resumen.md
|__-- README.md
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
cd proyecto
mv datos/archivo1.txt informe/
rm datos/archivo2.txt
rmdir datos
```

## Ejercicio 2: Copiar y mover con *

**Estructura inicial:**
```
backup/
|---- enero/
|   |---- dia1.log
|   |---- dia2.log
|   |__-- dia3.log
|__-- febrero/
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
cd backup
cp enero/*.log febrero/
rm enero/dia2.log
```

## Ejercicio 3: Combinando mkdir, mv y rutas relativas

**Estructura inicial:**
```
materiales/
|---- clase1.txt
|__-- clase2.txt
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
cd materiales
mkdir teoria practica
mv clase1.txt teoria/
mv clase2.txt practica/
cd ..
rm -r materiales/practica
```

## Ejercicio 4: touch y errores comunes

**Estructura inicial:**
```
(No hay estructura inicial, solo comandos)
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
mkdir reportes
cd reportes
touch resumen.txt
mv resumen.txt datos/
```

