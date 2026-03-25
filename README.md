# 📝 Todo List — CSS Responsivo

Proyecto de lista de tareas con estilos en CSS, al que se le agregó soporte responsivo para dispositivos móviles.

---

## 📁 Estructura del proyecto

```
todo-list/
├── index.html
├── style.css
└── README.md
```

---

## 🎨 ¿Qué contiene el CSS?

El archivo `style.css` define la apariencia visual de la aplicación. A continuación se describen los bloques principales:

| Selector | Descripción |
|---|---|
| `body` | Centra el contenido con flexbox y aplica padding general |
| `.todo-container` | Tarjeta blanca con sombra y bordes redondeados |
| `h2` | Título centrado con línea inferior azul |
| `.input-group` | Contenedor del input y el botón en fila |
| `input` | Campo de texto con borde y sin outline |
| `#add-btn` | Botón azul para agregar tareas |
| `ul` | Lista sin estilos por defecto |
| `li` | Cada tarea con separador inferior y layout flex |
| `.delete-btn` | Botón rojo sin fondo para eliminar tareas |

---

## 📱 Responsividad agregada

Se añadió un bloque `@media` al final del CSS **sin modificar el código original**, que aplica ajustes cuando el ancho de pantalla es de **480px o menos**:

```css
@media (max-width: 480px) {
  body { padding: 20px; }
  .todo-container { padding: 20px; }
  .input-group { flex-direction: column; }
  input { border-radius: 4px; margin-bottom: 8px; }
  #add-btn { border-radius: 4px; width: 100%; }
}
```

### Cambios que aplica el media query

- **`body`** — Reduce el padding de `50px` a `20px` para aprovechar mejor el espacio en móvil.
- **`.todo-container`** — Reduce el padding interno de `30px` a `20px`.
- **`.input-group`** — Cambia la dirección de fila (`row`) a columna (`column`) para que el input y el botón no queden comprimidos.
- **`input`** — Recupera las 4 esquinas redondeadas, ya que al estar en columna no necesita el lado derecho plano.
- **`#add-btn`** — Recupera sus 4 esquinas redondeadas y ocupa el ancho completo (`width: 100%`) para verse bien debajo del input.

---

## 🚀 ¿Cómo usarlo?

1. Clona o descarga el proyecto.
2. Abre `index.html` en tu navegador.
3. Escribe una tarea en el input y presiona el botón para agregarla.
4. Presiona el botón de eliminar para quitar una tarea de la lista.

---

## 🛠️ Tecnologías utilizadas

- HTML5
- CSS3 (Flexbox + Media Queries)

---

## 👤 Autor

Santiago Vidal Sánchez Martínez