# Secure File Manager

Este proyecto ofrece un gestor de archivos cifrados desde la terminal, con usuarios, permisos y cifrado implementado con la librería estándar de Python, sin dependencias externas.

<img width="837" height="601" alt="image" src="https://github.com/user-attachments/assets/e139ec66-5665-4de6-93d0-d0a390a9ca65" />
<img width="751" height="612" alt="image" src="https://github.com/user-attachments/assets/ab41132c-d46c-4dd9-a1fb-48c9768b579b" />
<img width="697" height="692" alt="image" src="https://github.com/user-attachments/assets/6b6c0855-ac40-4868-b24c-f584716ba7e8" />


## Requisitos

- Python 3.9 o superior

## Instalación automática

### Windows

Ejecuta desde la carpeta del proyecto:

```bat
install_windows.bat
```

Esto hará lo siguiente automáticamente:
- crea un entorno virtual en `.venv`
- instala `pip` y las dependencias del archivo `requirements.txt`
- deja listo el launcher para iniciar el programa

### Linux / macOS

Ejecuta:

```bash
chmod +x install_linux.sh
./install_linux.sh
```

Esto hará lo siguiente automáticamente:
- crea un entorno virtual en `.venv`
- instala `pip` y las dependencias del archivo `requirements.txt`
- deja listo el launcher para iniciar el programa

## Inicio rápido

### Windows

```bat
start_windows.bat --help
```

### Linux / macOS

```bash
./start_linux.sh --help
```

## Uso básico

### 1) Inicializar el espacio seguro

```bat
start_windows.bat init --admin admin
```

```bash
./start_linux.sh init --admin admin
```

El programa pedirá la contraseña del administrador y creará el almacenamiento en `secure_store` por defecto.

### 2) Añadir un usuario

```bat
start_windows.bat add-user --admin admin --username pepe --password MiPassword123
```

```bash
./start_linux.sh add-user --admin admin --username pepe --password MiPassword123
```

### 3) Cifrar un archivo

```bat
start_windows.bat encrypt --admin admin --file archivo.txt --allowed pepe
```

```bash
./start_linux.sh encrypt --admin admin --file archivo.txt --allowed pepe
```

### 4) Descifrar un archivo

```bat
start_windows.bat decrypt --file archivo.txt --username pepe
```

```bash
./start_linux.sh decrypt --file archivo.txt --username pepe
```

## Comandos útiles

- `--help`: muestra la ayuda general
- `list-users`: muestra usuarios registrados
- `list-files`: muestra archivos cifrados
- `status`: muestra el estado del espacio seguro

## Personalización

Puedes cambiar la carpeta de almacenamiento con:

```bat
start_windows.bat --storage otra_carpeta init --admin admin
```

```bash
./start_linux.sh --storage otra_carpeta init --admin admin
```
