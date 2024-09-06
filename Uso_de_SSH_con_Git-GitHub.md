# Uso de SSH con Git y GitHub

Cuando trabajas con GitHub, existen dos formas principales de autenticarte al clonar, hacer push o pull en repositorios: **HTTPS** y **SSH**.

Con el protocolo SSH, puedes conectarte y autenticarte a servidores y servicios remotos. Con las claves SSH, puedes conectarte a GitHub sin tener que proporcionar tu nombre de usuario y token de acceso personal en cada visita. 

A continuación se detallan las ventajas y desventajas de cada método para ayudarte a decidir cuál usar según tu caso.

## Ventajas y Desventajas de usar HTTPS vs SSH en GitHub

| Característica     | HTTPS                                   | SSH                                   |
|--------------------|-----------------------------------------|---------------------------------------|
| **Facilidad de uso**   | Alta, sin configuración inicial         | Media, requiere configuración inicial |
| **Seguridad**      | Media (segura con tokens)               | Alta (autenticación por clave)        |
| **Autenticación**  | Contraseña/token por cada operación     | Automática con la llave SSH           |
| **Acceso desde múltiples máquinas** | Fácil (solo contraseña o token) | Requiere configuración en cada máquina |
| **Restricciones de red** | Menos probable que esté bloqueado   | Puede ser bloqueado por firewalls     |

### ¿Cuál elegir?

- **Elige HTTPS** si prefieres una configuración rápida, trabajas en múltiples máquinas o entornos donde es más fácil administrar contraseñas o tokens.
- **Elige SSH** si buscas mayor seguridad y comodidad a largo plazo, especialmente si trabajas en una sola máquina o tienes facilidad para configurar SSH en varias máquinas.

## Generar una nueva llave SSH y registrarla en GitHub

### 1. Generar una nueva llave SSH
Si no tienes una llave SSH o prefieres generar una nueva, usa el siguiente comando:

```bash
ssh-keygen -t ed25519 -C "tu.correo@ejemplo.com"
```

- -t ed25519: Especifica el tipo de encriptación. ed25519 es más moderna y segura. Si tu sistema no lo soporta, puedes usar rsa con -t rsa.
- -C: Es un comentario que suele ser tu correo electrónico para identificar la llave.

Nota: Si está utilizando un sistema que no admite el algoritmo Ed25519, utilice:

```bash
 ssh-keygen -t rsa -b 4096 -C "tu.correo@ejemplo.com"
```

### 2. Copiar tu clave pública
Para usar la autenticación SSH en GitHub, necesitas copiar la clave pública y añadirla a tu cuenta de GitHub. Usa el siguiente comando para copiarla al portapapeles:

```bash
cat ~/.ssh/id_ed25519.pub
```

Copia el contenido que aparece en pantalla.

### 3. Añadir tu clave SSH en GitHub

1. Accede a GitHub y ve a Ajustes de SSH.
2. Haz clic en "New SSH Key".
2. Pega tu clave pública copiada en el campo "Key".
4. Da un nombre a la llave en el campo Title (puedes usar el nombre de tu máquina para identificarla).
5. Haz clic en "Add SSH Key".

### 4. Verificar la conexión SSH con GitHub
Para asegurarte de que la llave SSH está correctamente configurada y funciona, prueba la conexión con el siguiente comando:

```bash
ssh -T git@github.com
```

Si todo está correcto, recibirás un mensaje similar a:

"Hi username! You've successfully authenticated, but GitHub does not provide shell access."