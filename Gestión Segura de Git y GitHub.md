# Actividad Complementaria: Gestión Segura de Evidencias con Git y GitHub

## Objetivo

Aplicar mecanismos de protección de la información mediante el uso de control de versiones, autenticación y repositorios privados para almacenar evidencias de las prácticas realizadas en Linux.

---

# Parte 1: Creación de Cuenta GitHub

Cada estudiante deberá:

1. Crear una cuenta en GitHub.
2. Configurar autenticación segura.
3. Activar la autenticación de dos factores (2FA).

## Evidencia

Captura de:

- Cuenta creada.

<p align='center'>
<img width="200" height="250" alt="imagen" src="https://github.com/user-attachments/assets/f924550a-4e43-4057-9287-23dc190c1eab" />
</p>

- Activación de 2FA.
- Perfil configurado.

<p align='center'>
  <img width="400" height="390" alt="imagen" src="https://github.com/user-attachments/assets/9e726b9f-51a3-472b-b222-a0426fc170b6" />
</p>

---

# Parte 2: Instalación y Configuración de Git en Linux

## Instalación

### Ubuntu/Debian

```bash
sudo apt update
sudo apt install git
```

<img width="950" height="450" alt="imagen" src="https://github.com/user-attachments/assets/824c25c4-e94c-4345-a223-89eabaed48b4" />


### Verificación

```bash
git --version
```

<img width="1065" height="220" alt="imagen" src="https://github.com/user-attachments/assets/16e5335e-e616-4926-b1e5-f4e057d426dc" />


## Configuración inicial

```bash
git config --global user.name "Nombre Apellido"
git config --global user.email "correo@ejemplo.com"
```

### Verificar configuración

```bash
git config --list
```

## Evidencia

Captura mostrando la configuración realizada.

<img width="500" height="450" alt="imagen" src="https://github.com/user-attachments/assets/14098243-c190-4555-b83e-0d3efa522c55" />

---

# Parte 3: Creación de Repositorio Privado

Cada estudiante deberá crear un repositorio denominado:

```text
SO-Seguridad-2026
```

## Configuración

- Privado
- Sin acceso público
- Descripción del curso

## Evidencia

Captura del repositorio creado.

---

# Parte 4: Organización Segura de Evidencias

Crear la siguiente estructura:

```text
SO-Seguridad-2026/
│
├── Capitulo1/
├── Capitulo2/
├── Capitulo3/
├── Capitulo4/
├── Capitulo5/
├── Capitulo6/
└── Informe_Final/
```

Cada carpeta contendrá:

- Capturas
- Comandos ejecutados
- Resultados obtenidos
- Análisis

---

# Parte 5: Protección de Datos Sensibles

Crear archivo:

```bash
touch .gitignore
```

## Contenido

```gitignore
*.log
*.key
*.pem
*.crt
passwords.txt
credenciales.txt
```

## Objetivo

Evitar la publicación accidental de:

- Contraseñas
- Claves SSH
- Certificados
- Archivos sensibles

## Evidencia

Captura del archivo `.gitignore`.

---

# Parte 6: Generación de Claves SSH

Generar clave SSH:

```bash
ssh-keygen -t ed25519 -C "correo@ejemplo.com"
```

Ver clave pública:

```bash
cat ~/.ssh/id_ed25519.pub
```

Registrar la clave en GitHub.

## Evidencia

Captura de la clave agregada en GitHub.

---

# Parte 7: Subida de Evidencias

## Inicializar repositorio

```bash
git init
```

## Agregar archivos

```bash
git add .
```

## Primer commit

```bash
git commit -m "Primera entrega de evidencias"
```

## Asociar repositorio remoto

```bash
git remote add origin https://github.com/usuario/SO-Seguridad-2026.git
```

## Enviar evidencias

```bash
git push -u origin main
```

---

# Parte 8: Control de Integridad

Generar hash SHA-256 de evidencias importantes:

```bash
sha256sum informe_final.pdf
```

Guardar resultado en:

```text
hashes.txt
```

Subir el archivo al repositorio.

## Objetivo

Garantizar que las evidencias no han sido modificadas.
