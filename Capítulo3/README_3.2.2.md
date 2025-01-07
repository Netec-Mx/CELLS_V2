# Práctica 3.2.2 Eventos & Reactividad

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:
- Crear un componente interactivo que gestione eventos del usuario.

## Duración aproximada:
- 95 minutos.

 
## Instrucciones 
 
### **Tarea 1: Manejo de Eventos en Lit**

En esta tarea, aprenderás a manejar eventos en un componente Lit. Comenzarás con la configuración del proyecto y crearás un componente que capture y gestione eventos, modificando su comportamiento en respuesta a las interacciones del usuario.

#### Paso 1. **Crear la carpeta del proyecto:**  
   Ejecuta el siguiente comando para crear una carpeta llamada `practica3_2_2` que contendrá tu proyecto.

   ```cmd
   mkdir practica3_2_2
   ```

#### Paso 2. **Navegar a la carpeta recién creada:**  
   ```cmd
   cd practica3_2_2
   ```

#### Paso 3. **Inicializar un proyecto Node.js:**  
   ```cmd
   npm init -y
   ```

#### Paso 4. **Instalar dependencias necesarias:**  
   Instala `lit` y `es-dev-server` para trabajar con componentes y ejecutar un servidor local.
   ```cmd
   npm install lit
   npm install --save-dev es-dev-server
   ```
#### Paso 5. **Crear una subcarpeta `src`:**  
   ```cmd
   mkdir src
   ```

#### Paso 6. **Crear el archivo `index.html` en la carpeta raíz:**  
   Este será el punto de entrada de tu proyecto.
   ```cmd
   touch index.html
   ```

#### Paso 7. **Crear el archivo del componente en la carpeta `src`:**  
   ```cmd
   cd src
   touch bb-eventos.js
   ```

#### Paso 8. **Abre el archivo `bb-eventos.js` y agrega el siguiente contenido:**

   - **Define un contador que incrementa al hacer clic en un botón.**
   - **Muestra un mensaje dinámico basado en la interacción del usuario.**

   ```javascript
   import { LitElement, html, css } from 'lit';

class BbEventos extends LitElement {
  static styles = css`
    :host {
      display: block;
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 20px;
    }
    .button {
      padding: 10px 20px;
      font-size: 16px;
      color: white;
      background-color: #007acc;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .button:hover {
      background-color: #005fa3;
    }
    .message {
      margin-top: 20px;
      font-size: 18px;
      color: #333;
    }
  `;

  static properties = {
    message: { type: String },
  };

  constructor() {
    super();
    this.message = 'Presiona el botón para interactuar';
  }

  handleClick() {
    this.message = '¡El evento se ejecutó correctamente!';
  }

  render() {
    return html`
      <h2>Manejo de Eventos en Lit</h2>
      <button class="button" @click="${this.handleClick}">Haz clic aquí</button>
      <div class="message">${this.message}</div>
    `;
  }
}

customElements.define('bb-eventos', BbEventos);

   ```

#### Paso 9. **Actualizar el archivo `index.html`**

    - Abre el archivo `index.html` y define la estructura básica para cargar y mostrar el componente `bb-eventos`.

    ```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Manejo de Eventos en Lit</title>
</head>
<body>
  <h1>Práctica: Manejo de Eventos</h1>
  <!-- Componente personalizado -->
  <bb-eventos></bb-eventos>
  <!-- Cargar el módulo de JavaScript -->
  <script type="module" src="./src/bb-eventos.js"></script>
</body>
</html>

    ```

#### Paso 10. **Iniciar un servidor local para visualizar el proyecto**

- **Configurar el servidor en `package.json`:**  
   Agrega el siguiente script al archivo `package.json` para iniciar un servidor local:  
   ```json
   "scripts": {
     "start": "es-dev-server --app-index index.html --node-resolve --open"
   }
   ```

- **Inicia el servidor local:**  
   Ejecuta el siguiente comando para cargar la aplicación en tu navegador:  
   ```cmd
   npm start
   ```

#### Paso 11. **Verificar el resultado**

   - Abre tu navegador y observa el componente `bb-eventos`.
   - Interactúa con el botón y verifica que el contador se actualice correctamente.
   - Asegúrate de que los eventos se manejen de forma fluida y que el diseño sea coherente. 



### Tarea 2. Manejo de Eventos Reactivos

### Tarea 3. Gestión de estado reactivo con propiedades observables

### Tarea 4. Actualizaciones eficientes del DOM con reuestUpdate.

### Resultado esperado


![imagen resultado](../images/img3.png)
