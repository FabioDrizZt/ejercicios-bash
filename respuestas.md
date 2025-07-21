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

