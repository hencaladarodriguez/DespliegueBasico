# Mi Proyecto Web

> Práctica evaluable — Documentación y Control de Versiones  
> 2DAW · UT6 · Curso 2025-2026

---

## Descripción

Proyecto web estático desplegado mediante **Docker Compose** y servido por **Nginx**.  
Desarrollado como práctica de la unidad de Documentación y Control de Versiones, demuestra el uso de Git para gestionar el historial de cambios y Docker para garantizar un entorno de despliegue reproducible.

---

## Tecnologías Utilizadas

| Tecnología      | Versión   | Uso                              |
|-----------------|-----------|----------------------------------|
| HTML5 / CSS3    | —         | Estructura y estilos de la web   |
| Docker          | 24+       | Contenedorización                |
| Docker Compose  | v2        | Orquestación del servicio        |
| Nginx           | alpine    | Servidor web estático            |
| Git             | 2+        | Control de versiones             |
| GitHub          | —         | Alojamiento del repositorio      |

---

## Requisitos Previos

Antes de comenzar, asegúrate de tener instalado:

- [Git](https://git-scm.com/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (incluye Docker Compose)

---

## Instrucciones de Instalación

```bash
# 1. Clonar el repositorio
git clone https://github.com/usuario/mi-proyecto-web.git

# 2. Acceder al directorio del proyecto
cd mi-proyecto-web
```

---

## Instrucciones de Despliegue

```bash
# Levantar el contenedor en segundo plano
docker compose up -d

# Verificar que el contenedor está en ejecución
docker compose ps
```

Abrir el navegador y acceder a:

```
http://localhost:8080
```

### Detener el servicio

```bash
docker compose down
```

### Ver los logs del servidor

```bash
docker compose logs -f
```

---

## Estructura del Proyecto

```
mi-proyecto-web/
├── docker-compose.yml     # Configuración del servicio Docker
├── README.md              # Documentación del proyecto
└── src/
    └── index.html         # Página web principal
```

---

## Configuración de Docker Compose

El archivo `docker-compose.yml` define un único servicio:

- **Imagen:** `nginx:alpine` (ligera y oficial)
- **Puerto:** mapea el `8080` del host al `80` del contenedor
- **Volumen:** monta la carpeta `./src` como contenido web (solo lectura)
- **Restart:** `unless-stopped` para reinicio automático

---

## Flujo de Trabajo con Git

```bash
# Ver el estado de los archivos
git status

# Añadir cambios al área de preparación
git add .

# Crear un commit con mensaje descriptivo
git commit -m "descripción del cambio realizado"

# Subir los cambios al repositorio remoto
git push origin main
```

---

## Autor

**Nombre del alumno**  
2DAW · Curso 2025-2026

---

## Licencia

Este proyecto se desarrolla con fines educativos.