# Aplicación React con Custom Hook useFetch
Este reto se centra en la creación de un custom hook reutilizable en React para realizar solicitudes HTTP. El objetivo principal es consolidar el uso de useState y useEffect para manejar datos asincrónicos, encapsulando la lógica de fetch() en un hook limpio y modular.

# Reto Semana 20
Implementar un hook personalizado llamado useFetch que cumpla con los siguientes requisitos:

### Hook ```useFetch```
- Recibe una URL como parámetro.
- Devuelve un objeto con tres propiedades:
  - data: resultado de la solicitud.
  - loading: booleano que indica si la solicitud está en proceso.
  - error: objeto con información del error si ocurre.

### Componente Principal (App.jsx)
- Utiliza el hook useFetch para obtener datos desde la API: ```https://jsonplaceholder.typicode.com/users```
- Muestra un mensaje de carga mientras se realiza la solicitud.
- Muestra un mensaje de error si la solicitud falla.
- Muestra una lista de nombres de usuarios si la solicitud es exitosa.

# Tecnologías utilizadas
- React
- JavaScript
- Vite
- Hooks
- Fetch API

# Estructura del Proyecto
```
retoSemana20/
├── node_modules/
├── public/
├── src/             
│   ├── components/
│   │   └── useFetch.jsx            ← Custom hook para solicitudes HTTP
│   ├── App.jsx                     ← Componente principal que usa el hook
│   ├── index.css                   ← Estilos globales
│   └── main.jsx                    ← Punto de entrada de la aplicación
├── .gitignore
├── eslint.config.js
├── index.html
├── package-lock.json
├── package.json
└── vite.config.js
```

# Cómo ejecutar
- Instala dependencias (si es un proyecto nuevo):
```npm install```
- Ejecuta el servidor de desarrollo de Vite:
```npm run dev```
- Abre la URL que te proporciona el terminal (generalmente http://localhost:5173/).

# Resultados y Funcionalidades
**Carga inicial**
Mientras se realiza la solicitud, se muestra el mensaje: "Cargando..." (Al ser muy rapida la carga, casi no es visible)

**Error en la solicitud**
Si ocurre un error, se muestra el mensaje: "Error: [mensaje del error]"
<img width="1913" height="160" alt="image" src="https://github.com/user-attachments/assets/725291d9-b795-4d84-9634-c609e66fa3b9" />

**Datos cargados correctamente**
Si la solicitud es exitosa, se muestra una lista con los nombres de los usuarios obtenidos desde la API: "Usuarios" seguido de los nombres.
<img width="1909" height="387" alt="image" src="https://github.com/user-attachments/assets/99ce22e6-2ce8-4470-a464-3c8dfac3c0eb" />
