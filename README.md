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

## Ejercicio 5: Uso de rutas relativas y absolutas

**Estructura inicial:**
```
mi_proyecto/
|---- notas/
|   |__-- tarea.txt
|__-- entregas/
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
cd mi_proyecto/notas
mv tarea.txt ../entregas/
cd ..
rmdir notas
```

## Ejercicio 6: Eliminar archivos y carpetas con comodines

**Estructura inicial:**
```
documentos/
|---- vieja/
|   |---- carta1.txt
|   |__-- carta2.txt
|__-- nueva/
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
cd documentos/vieja
rm carta*.txt
cd ..
rmdir vieja
```

## Ejercicio 7: Creación masiva de archivos

**Estructura inicial:**
```
(No hay estructura inicial)
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
mkdir logs
cd logs
touch log_{01..05}.txt
rm log_03.txt
```

## Ejercicio 8: Mover archivos y renombrar carpetas

**Estructura inicial:**
```
descargas/
|__-- imagen.jpg
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
mkdir fotos
mv descargas/imagen.jpg fotos/
mv fotos galeria
```

## Ejercicio 9: Reorganización de carpetas con múltiples comandos

**Estructura inicial:**
```
proyecto/
|---- drafts/
|   |---- nota1.md
|   |__-- nota2.md
|__-- final/
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
cd proyecto
mkdir backup
cp drafts/nota1.md backup/
mv drafts/nota2.md final/
rm -r drafts
```

## Ejercicio 10: Renombrado y reubicación de múltiples archivos

**Estructura inicial:**
```
trabajo/
|---- img1.png
|---- img2.png
|__-- otros/
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
cd trabajo
mkdir imagenes
mv img*.png imagenes/
cd imagenes
for f in *.png; do mv "$f" "nuevo_$f"; done
```

## Ejercicio 11: Estructura anidada con múltiples niveles

**Estructura inicial:**
```
materias/
|__-- 2024/
    |---- quimica/
    |   |__-- tp1.txt
    |__-- fisica/
        |__-- tp2.txt
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
cd materias/2024
mv quimica/tp1.txt ../
rm -r quimica
cd fisica
mv tp2.txt ../../
cd ..
rmdir fisica
```

## Ejercicio 12: Creación de carpetas y archivos en lote

**Estructura inicial:**
```
(No hay estructura inicial)
```

**¿Qué ocurre después de ejecutar los siguientes comandos?**
```bash
mkdir proyecto
cd proyecto
for mes in enero febrero marzo; do mkdir $mes; touch $mes/informe.txt; done
rm febrero/informe.txt
rmdir febrero
```



