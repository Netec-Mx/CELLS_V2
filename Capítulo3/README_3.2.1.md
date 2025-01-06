# Práctica 3.2.1 Estilos en Lit

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:
-

 
## Duración aproximada:
- 125 minutos.


## Instrucciones 

### **Tarea 1. Estilos en Lit**

#### Paso 1. **Estructuración del Proyecto Lit**

1. **Crear la carpeta principal del proyecto:**
   Ejecuta el siguiente comando para crear una carpeta llamada `practica3_2_1` que contendrá tu proyecto.  
   ```cmd
   mkdir practica3_2_1
   ```

2. **Inicializar el proyecto con Node.js:**
   Navega a la carpeta recién creada y prepara el entorno de trabajo inicializando un proyecto con Node.js.  
   ```cmd
   cd practica3_2_1
   npm init -y
   ```

3. **Crear la estructura de carpetas y archivos:**

   - Crea una subcarpeta llamada `src` para organizar los archivos fuente.  
    
     ```cmd
     mkdir src
     ```
   - Dentro de la carpeta raíz, crea un archivo llamado `index.html`, que será el punto de entrada de tu proyecto.  
    
     ```cmd
     touch index.html
     ```
   - Dentro de la carpeta `src`, crea un archivo llamado `bb-estilos.js`, donde escribirás los estilos de tu componente Lit.  
    
     ```cmd
     cd src
     touch bb-estilos.js
     ```  

Con estos pasos, tendrás listo el proyecto base para comenzar a trabajar con estilos en Lit.


#### Paso 2. **Uso de Estilos en Lit**

1. **Agregar contenido al archivo `bb-estilos.js`:**  
   Este archivo define un componente Lit con estilos aplicados.

   ```javascript
   import { LitElement, html, css } from 'lit';

   class BbEstilos extends LitElement {
     // Definición de estilos
     static styles = css`
       :host {
         display: block;
         font-family: Arial, sans-serif;
         text-align: center;
         color: #333;
       }
       .container {
         padding: 20px;
         border: 1px solid #ddd;
         border-radius: 8px;
         background-color: #f9f9f9;
       }
       h1 {
         color: #007acc;
       }
       p {
         font-size: 14px;
       }
     `;

     // Renderizado del componente
     render() {
       return html`
         <div class="container">
           <h1>Estilos en Lit</h1>
           <p>Este es un ejemplo de un componente estilizado con Lit.</p>
         </div>
       `;
     }
   }

   customElements.define('bb-estilos', BbEstilos);
   ```

2. **Actualizar el archivo `index.html`:**  
   Este archivo carga el componente y muestra su contenido.

   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
     <meta charset="UTF-8" />
     <meta name="viewport" content="width=device-width, initial-scale=1.0" />
     <title>Estilos en Lit</title>
   </head>
   <body>
     <h1>Bienvenido a la práctica de Lit</h1>
    
     <!-- Componente personalizado -->
     <bb-estilos></bb-estilos>

     <!-- Cargar el módulo de JavaScript -->
     <script type="module" src="./src/bb-estilos.js"></script>
   </body>
   </html>
   ```

3. **Iniciar un servidor local para visualizar el proyecto:**  
   Puedes usar un servidor local como el de `live-server` o el integrado en Visual Studio Code para ejecutar el proyecto.

   ```cmd
   npm start
   ```

4. **Verificar el resultado:**  
   Abre tu navegador web y observa cómo el componente `bb-estilos` se carga con los estilos definidos. Asegúrate de que los estilos se apliquen correctamente y que el diseño sea coherente.

<br/><br/>

#### Tarea 2. 



