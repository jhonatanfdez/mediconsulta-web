# mediconsulta-web

Sitio público de **MediConsulta**. Cuatro páginas de HTML estático, servidas
por GitHub Pages.

## Para qué existe

Tres de las cuatro páginas no son marketing: **Google Play las exige** para
poder publicar la app.

| Página | Para qué |
|---|---|
| `index.html` | Qué hace el producto, para quién y cuánto cuesta. |
| `privacidad.html` | **Exigida por Play.** URL pública que revisa una persona. |
| `terminos.html` | Términos de servicio. |
| `soporte.html` | **Exigida por Play** como URL de soporte. Incluye cómo pedir la eliminación de la cuenta sin entrar a la app, que Play exige desde 2023. |

## Por qué HTML a mano

Son cuatro páginas de texto. Meter un framework o un generador de sitios
sería cargar un camión para llevar una caja: más piezas que mantener, más
cosas que se rompen con el tiempo, y nada que ganar. Así carga instantáneo y
dentro de un año se sigue editando con cualquier editor.

Todo el estilo vive en `estilo.css`. No hay JavaScript.

## Cómo editar

Se edita el `.html` y se sube. GitHub Pages republica solo, en un minuto.

Si se cambia algo de la política o los términos, **hay que actualizar la
fecha** de «Última actualización» que está arriba de cada una.

## Lo que no puede romperse

- **La URL de la política no puede dejar de funcionar nunca.** Está declarada
  en la ficha de Google Play, y si devuelve 404 pueden bajar la app.
- Si algún día se compra un dominio propio, se apunta a este mismo sitio y se
  actualiza la ficha de Play. Las direcciones viejas deben seguir
  respondiendo.

## Pendiente

- Que un abogado revise la política y los términos. Los redactó Claude, que
  no es abogado, y el punto más delicado es la limitación de responsabilidad
  (sección 7 de los términos) para un producto que maneja datos de salud.
- Decidir el límite económico de responsabilidad en esa misma sección.
- Capturas de pantalla reales en la portada.

## Relación con el repo de la app

Este repositorio es independiente y **público** (GitHub Pages gratis lo
exige). El repo de la app es privado y se monta este como submódulo en la
carpeta `web/`.

Para traerlo al clonar el proyecto:

```
git submodule update --init --recursive
```
