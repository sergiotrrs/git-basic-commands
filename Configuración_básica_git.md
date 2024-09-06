# Configuraciones Básicas de Git con `git config --global`

Cuando trabajamos con Git, es importante establecer algunas configuraciones básicas que identificarán al autor de los commits y definirán el comportamiento de Git a nivel global en tu sistema. El comando `git config --global` permite establecer configuraciones que aplican a todos los repositorios de Git en tu sistema.

## ¿Por qué usar `git config --global`?

Configurar tus credenciales y preferencias globalmente asegura que cada vez que realices un commit, la información de autoría esté correctamente asignada. Además, otras configuraciones, como el editor por defecto, pueden mejorar tu flujo de trabajo.

## Comandos Esenciales

### 1. Configurar tu Nombre de Usuario
Este comando establece el nombre que aparecerá en los commits como autor:

```bash
git config --global user.name "Tu Nombre"
```

### 2. Configurar tu corre eléctrónico
Este comando establece el nombre que aparecerá en los commits como autor:

```bash
git config --global user.email "tu.correo@ejemplo.com"
```

### 3. Configurar el marco de colores
Este comando habilita la visualización de colores en la terminal para los comandos de Git. Esto mejora la legibilidad y facilita la identificación de diferentes tipos de información, como diferencias (`git diff`), estado (`git status`), o ramas (`git branch`), al usar colores específicos:

```bash
git config --global color.ui true
```

### 4. Configurar el Editor por Defecto
Es recomendable configurar el editor de texto por defecto para Git. Esto será útil cuando Git requiera abrir un archivo para que añadas mensajes de commit o resuelvas conflictos:

```bash
git config --global core.editor "nano"
```

### 5. Verificar tus Configuraciones 
Para confirmar que tus configuraciones se han aplicado correctamente, puedes ejecutar:

```bash
git config --global --list
```

## ¿Cuándo Usar Estas Configuraciones?

- Nombre y correo electrónico: Debes configurarlos antes de empezar a trabajar con Git para que tu identidad quede asociada a cada cambio que realices.
- Editor por defecto: Útil cuando Git necesite abrir un editor para mensajes de commit o para resolver conflictos.

Notas adicionales:
- Si deseas configurar parámetros específicos solo para un proyecto, puedes omitir la bandera --global y Git aplicará las configuraciones solo al repositorio actual.


## ¿Cómo eliminar una configuración global?

Si deseas eliminar una configuración que previamente has establecido con `git config --global`, el comando a usar es el siguiente:

```bash
git config --global --unset <nombre.de.configuracion>
```