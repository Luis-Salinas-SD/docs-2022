+++
title = "Eventos"
chapter = true
weight = 4
pre = "<b>4. </b>"
+++

# Eventos

Los eventos en React son muy similares que en Javascript

En el boton Agregar establecemos el evento onClick

```jsx
import React from "react";

const Eventos = ({ valor }) => {
  const addOne = () => {
    console.log(valor + 1);
  };

  return (
    <>
      <button onClick={addOne}>Agregar!</button>
    </>
  );
};

export default Eventos;
```
