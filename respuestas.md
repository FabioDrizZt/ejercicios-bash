# Ejercicios de Bash: ¿Qué pasa si...? (con respuestas)

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

**Comandos ejecutados:**
```bash
cd proyecto
mv datos/archivo1.txt informe/
rm datos/archivo2.txt
rmdir datos
```

**Respuesta esperada:**
- `archivo1.txt` se mueve a `informe/`
- `archivo2.txt` se borra
- `datos/` queda vacío y se elimina

**Estructura final:**
```
proyecto/
├── informe/
│   ├── resumen.md
│   └── archivo1.txt
└── README.md
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

**Comandos ejecutados:**
```bash
cd backup
cp enero/*.log febrero/
rm enero/dia2.log
```

**Respuesta esperada:**
- Todos los `.log` de `enero/` se copian a `febrero/`
- Luego, `dia2.log` se elimina solo de `enero/`

**Estructura final:**
```
backup/
├── enero/
│   ├── dia1.log
│   └── dia3.log
└── febrero/
    ├── dia1.log
    ├── dia2.log
    └── dia3.log
```

## Ejercicio 3: Combinando mkdir, mv y rutas relativas

**Estructura inicial:**
```
materiales/
|---- clase1.txt
|__-- clase2.txt
```

**Comandos ejecutados:**
```bash
cd materiales
mkdir teoria practica
mv clase1.txt teoria/
mv clase2.txt practica/
cd ..
rm -r materiales/practica
```

**Respuesta esperada:**
- Se crean las carpetas `teoria` y `practica`
- `clase1.txt` se mueve a `teoria/`, `clase2.txt` a `practica/`
- Luego se borra `practica/` con su archivo

**Estructura final:**
```
materiales/
└── teoria/
    └── clase1.txt
```

## Ejercicio 4: touch y errores comunes

**Estructura inicial:**
```
(No hay estructura inicial, solo comandos)
```

**Comandos ejecutados:**
```bash
mkdir reportes
cd reportes
touch resumen.txt
mv resumen.txt datos/
```

**Respuesta esperada:**
- El comando `mv` falla porque `datos/` no existe
- Se muestra un error: `mv: cannot move 'resumen.txt' to 'datos/': No such file or directory`
- El archivo `resumen.txt` queda en la carpeta `reportes/`

## Ejercicio 1: Uso de rutas relativas y absolutas

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

## Ejercicio 2: Eliminar archivos y carpetas con comodines

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

## Ejercicio 3: Creación masiva de archivos

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

## Ejercicio 4: Mover archivos y renombrar carpetas

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
