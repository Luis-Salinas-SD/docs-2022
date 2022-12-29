+++
title = "Componentes"
chapter = true
weight = 2
pre = "<b>2. </b>"
+++

# Componentes

No es obligatorio, pero por buenas practicas el archivo en el cual vamos a crear nuestro componente se debe llamar igual que el componente, por ejemplo vamos a crear uno con el siguiente nombre **AppComponent**.

{{< tabs >}}
{{% tab name="AppComponent.jsx" %}}

```jsx
const AppComponent = () => {
  return (
    <div>
      <span>El Componente se llama AppComponent</span>
      <span>bloque 2</span>
      <span>bloque 3</span>
    </div>
  );
};
```

{{% /tab %}}
{{% tab name="main.jsx" %}}

```jsx
import React from "react";
import ReactDOM from "react-dom/client";
//Importación del componente funcional AppComponent
import AppComponent from "./AppComponent";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    // Componente
    <AppComponent />
  </React.StrictMode>
);
```

{{% /tab %}}
{{< /tabs >}}

##### Puntos a tener en cuenta para crear nustro componente.

- Que el componente se llame igual que el archivo .jsx
- Que nuestro componente de función sea PascalCase
- El componente solo puede retornar un solo bloque, en el ejemplo anterior el div es quien retorna los demas bloques de codigo HTML.

##### Exportar el componente

Para exportar el componente lo hacemos de la siguiente manera:

> export default **< NombreDelComponente >**;

```jsx
export default AppComponent;
```

##### Mostrar Componente en la vista

Para mostrar el componente es necesario realizar una importación en el archivo principal, en este caso nuestro archivo se llama **main.jsx**

> Una vez realizada la importación debemos mandarlo a llamara en el docuemtno para que este se muestre en pantalla de la siguiente manera

```jsx
import React from "react";
import ReactDOM from "react-dom/client";
//Importación del componente funcional AppComponent
import AppComponent from "./AppComponent";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    //Componente
    <AppComponent />
  </React.StrictMode>
);
```
