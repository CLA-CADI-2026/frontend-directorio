# Directorio Frontend: Instrucciones para reproducir el proyecto

## Autores (Equipo 6):
* Aram Baruch González Pérez
* Pedro Hernández Oregel
* Roberto Martínez Román

## Video con demostración del funcionamiento
[Demo Equipo 6](https://youtu.be/-whUfUK38-s)


Este repositorio contiene un frontend en HTML, CSS y JavaScript puro para gestionar materias y docentes mediante una API REST.

## 1. Requisitos

- Python 3 instalado (solo para levantar un servidor local).
- Un backend activo con los endpoints de materias y docentes.
- Navegador web moderno.

## 2. Clonar el repositorio

```bash
git clone https://github.com/CLA-CADI-2026/frontend-directorio.git
cd frontend-directorio
```

## 3. Configurar la URL del backend

Edita la constante `API_BASE` en el archivo `index.html` y coloca la URL de tu backend:

```javascript
const API_BASE = "http://TU_BACKEND/api/v1";
```

Ejemplos:

- Local: `http://localhost:3000/api/v1`
- Codespaces: `https://xxxx-3000.app.github.dev/api/v1`

## 4. Levantar el frontend
En la terminal ejecuta:

```bash
python3 -m http.server 8080
```



Luego abre en el navegador:

`http://localhost:8080`

## 5. Probar que funciona

Al abrir la aplicación debes ver dos pestañas:

- Materias
- Docentes

Valida el flujo CRUD en ambas:

1. Crear un registro.
2. Ver la lista actualizada.
3. Editar un registro.
4. Eliminar un registro.

Si hay problemas de conexión, revisa:

- Que `API_BASE` sea correcto.
- Que el backend esté encendido y con CORS habilitado para el origen del frontend.
- Que la URL incluya el prefijo `/api/v1`.

## 6. Endpoints esperados del backend

El frontend consume estos recursos:

- `GET /materias`
- `GET /materias/:id`
- `POST /materias`
- `PUT /materias/:id`
- `DELETE /materias/:id`
- `GET /docentes`
- `GET /docentes/:id`
- `POST /docentes`
- `PUT /docentes/:id`
- `DELETE /docentes/:id`

## 7. Estructura actual del proyecto

```text
frontend-directorio/
|- index.html
|- README.md
```

Todo el frontend (estilos, interfaz y lógica JavaScript) está concentrado en `index.html`.
