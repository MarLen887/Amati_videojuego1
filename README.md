# Amati vuela

Videojuego sencillo para la feria de ciencias del proyecto **Amati**. El jugador ayuda al colibrí Amati a mantener el foco durante una ronda de 60 segundos: esquiva distracciones (íconos genéricos de redes sociales) y atrapa técnicas de estudio y herramientas reales de la aplicación para sumar puntos.

## Cómo se juega

- **Dificultad única:** el juego usa un solo ritmo (rápido, con distracciones ondulantes y en parejas). La mejor puntuación se guarda en el dispositivo.
- **Tienes 3 vidas y 60 segundos.** La partida termina cuando se acaban las vidas o el tiempo, lo que ocurra primero.
- **Esquiva** las distracciones: si Amati toca una, **pierde una vida y puntos** (175 puntos; nunca baja de cero), se rompe la racha, se le caen plumas y la barra de enfoque vuelve a cero.
- **Atrapa** las tarjetas de técnicas (insignia lima) y herramientas (insignia magenta): 50 puntos cada una por el multiplicador. Cada 4 atrapadas seguidas sube el multiplicador, hasta x5.
- **Barra de enfoque = recuperación.** Se llena solo al atrapar tarjetas (12 tarjetas llenan la barra). Al llegar al 100 % recuperas una vida y la barra se reinicia. Si ya tienes las 3 vidas, Amati te saluda aleteando con un mensaje motivador y la barra se queda llena.
- **Sable, la mascota de la UVP, te anima.** Cada vez que Amati pierde una vida aparece Sable, te llama «Pantera» y te dice una frase motivadora de máximo 7 palabras.
- **Bono final:** 300 puntos por cada vida restante si llegas al final del minuto.
- **Poderes** (aparecen poco): Pomodoro (escudo contra distracciones), Respiración (todo va más lento) y Feynman (puntos dobles), +125 puntos al tomarlos.
- La tarjeta dorada **¡Eureka!** es rara y da 250 puntos.
- Cada 15 a 20 segundos llega una **lluvia de ideas** (una ola de técnicas).
- **Hora dorada:** en los últimos 10 segundos todos los puntos valen doble.
- **Gancho inmediato:** en la pantalla de inicio Amati juega sola como demostración y la primera tarjeta llega a los 2 segundos.
- Al terminar se muestran el puntaje, el rango (calculado con los puntos ganados jugando, sin el bono), la mejor racha y las técnicas atrapadas. La mejor puntuación se guarda solo en ese dispositivo.

## Controles

| Dispositivo | Cómo se mueve Amati |
|---|---|
| Celular o tableta | Arrastrar el dedo en cualquier parte de la pantalla (movimiento relativo, para no tapar al colibrí) |
| Computadora | Flechas o WASD. `Enter` o `Espacio` para empezar, `Esc` o `P` para pausar |
| Control de videojuegos | Stick izquierdo o cruceta. Botón `A` para empezar o seguir, `Start` para pausar |

El control se detecta al conectarlo (USB o Bluetooth) y presionar cualquier botón. Funciona con los controles que el navegador reconoce como estándar (Xbox, PlayStation y similares).

En horizontal, las distracciones y tarjetas vienen de derecha a izquierda. En vertical caen de arriba hacia abajo; Amati se mantiene siempre de perfil y mira hacia el lado al que se mueve.

El colibrí aletea de verdad: el ala está separada del cuerpo en el sprite y gira sobre el hombro, con estela de movimiento. Aletea más rápido al subir o al recibir un golpe, y suelta plumas que caen con vaivén.

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
assets/amati.png         Colibrí completo con fondo transparente
assets/amati-ala.png     Capa del ala (se anima en el juego)
assets/amati-cuerpo.png  Capa del cuerpo
assets/sable.png         Sable, la mascota de la universidad
README.md         Este archivo
```

## Notas

- Las distracciones son personajes genéricos con cara enojada y ojos que siguen al colibrí (mensaje, corazón, campana, video, teléfono, carita); al chocar salen despedidas girando y la pantalla vibra. No se usan logotipos ni marcas de terceros.
- Estilo visual «pop urbano»: cielo azul saturado, contornos gruesos y colores planos de alto contraste, pensado para verse a pleno sol. No se usan logotipos ni marcas de terceros.
- El juego no recopila datos personales ni se conecta a ningún servidor.
