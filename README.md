# Amati vuela

Videojuego sencillo para la feria de ciencias del proyecto **Amati**. El jugador ayuda al colibrí Amati a mantener el foco durante una ronda de 60 segundos: esquiva distracciones (íconos genéricos de redes sociales) y atrapa técnicas de estudio y herramientas reales de la aplicación para sumar puntos.

## Cómo se juega

- **Esquiva** las distracciones: restan enfoque y rompen la racha. Si el enfoque llega a cero, Amati se despista unos segundos, pero la partida no termina.
- **Atrapa** las tarjetas de técnicas (borde verde azulado) y herramientas (borde coral). Cada 4 atrapadas seguidas sube el multiplicador, hasta x5.
- **Poderes** (aparecen poco): Pomodoro (escudo contra distracciones), Respiración (todo va más lento) y Feynman (puntos dobles).
- Cada 15 a 20 segundos aparece una **racha de técnicas** en forma de ola.
- Al terminar se muestran el puntaje, el rango, la mejor racha y las técnicas atrapadas. La mejor puntuación se guarda solo en ese dispositivo.

## Controles

| Dispositivo | Cómo se mueve Amati |
|---|---|
| Celular o tableta | Arrastrar el dedo en cualquier parte de la pantalla (movimiento relativo, para no tapar al colibrí) |
| Computadora | Flechas o WASD. `Enter` o `Espacio` para empezar, `Esc` o `P` para pausar |
| Control de videojuegos | Stick izquierdo o cruceta. Botón `A` para empezar o seguir, `Start` para pausar |

El control se detecta al conectarlo (USB o Bluetooth) y presionar cualquier botón. Funciona con los controles que el navegador reconoce como estándar (Xbox, PlayStation y similares).

En vertical, el juego gira el campo: las distracciones y tarjetas caen de arriba hacia abajo y Amati vuela hacia arriba. En horizontal vienen de derecha a izquierda.

## Cómo abrirlo

1. **Sin internet, en la computadora:** descarga la carpeta y abre `index.html` con Chrome, Edge o Firefox. No necesita instalar nada. Conecta el control y juega.
2. **En celular o tableta:** abre la dirección donde lo publiques (por ejemplo, GitHub Pages) y usa «Agregar a pantalla de inicio» si quieres un ícono.
3. **Sin conexión, la tipografía** cae a una fuente del sistema. El juego funciona igual.

### Publicar con GitHub Pages

En el repositorio: *Settings → Pages → Deploy from a branch → `main` / carpeta `/ (root)`*. La dirección será `https://<usuario>.github.io/<repositorio>/`.

## Personalización

- `APP_URL` (inicio del `<script>` en `index.html`): si escribes la dirección de Amati, aparece en la pantalla final.
- `?r=20` al final de la dirección acorta la ronda a 20 segundos. Útil para pruebas.
- Las técnicas y herramientas están en las listas `TECH` y `TOOLS`. Los nombres se tomaron del repositorio de Amati.

## Estructura

```
index.html        Juego completo en un solo archivo (HTML + CSS + JavaScript, sin dependencias)
assets/amati.png  Colibrí con fondo transparente
README.md         Este archivo
```

## Notas

- Las distracciones son íconos genéricos (burbuja de mensaje, corazón, campana, reproductor, teléfono, arroba). No se usan logotipos ni marcas de terceros.
- El juego no recopila datos personales ni se conecta a ningún servidor.
