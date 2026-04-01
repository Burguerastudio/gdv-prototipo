# Gladiadores de las Ventas — Prototipo Frontend

Prototipo interactivo de frontend para una academia de ventas gamificada con narrativa de gladiadores romanos. Diseñado para presentar la experiencia completa del producto antes del desarrollo.

## Demo en vivo

**https://gdv-sepia.vercel.app**

El prototipo incluye 5 pantallas navegables con interacciones, animaciones y un sistema de personalizacion completo.

## Pantallas

| Pantalla | Archivo | Descripcion |
|----------|---------|-------------|
| Dashboard | `index.html` | Ludus Magnus — mapa de progreso, proxima batalla, clase en vivo |
| Perfil | `player.html` | Perfil del gladiador — arquetipo, estadisticas, arsenal de armas |
| Modulos | `modulos.html` | Las 8 Batallas — sidebar de progreso, clase del lanista, recursos |
| Armeria | `armeria.html` | Entrenamientos adicionales — busqueda, filtros, grid de cursos |
| Coliseo | `coliseo.html` | Comunidad — Discord, leaderboard, eventos |

## Stack

- **HTML5** — paginas estaticas multi-page, minificadas
- **Tailwind CSS v3** — pre-built (15KB), no CDN
- **Vanilla JavaScript** (ES6+) — minificado con terser
- **CSS custom properties** — design tokens y tematizacion dinamica por arquetipo
- **Lenis** — smooth scroll (via CDN)
- **Web Audio API** — efectos de sonido metalicos sintetizados

Sin framework. Abrir cualquier HTML directamente en el navegador.

## Sistema de personalizacion

El prototipo incluye un **selector flotante** (boton en esquina inferior derecha) que permite configurar:

- **Arquetipo** (4): Dominus (verde), Structor (dorado), Invictus (naranja), Nexus (azul)
- **Personaje** (6): Servus, Ventas, Veteranus, Orator, Lanista, Imperator
- **Modulo activo** (1-8): cambia el estado de progreso en toda la app

Selecciona las opciones y pulsa **"Aplicar Cambios"** para recargar con la nueva configuracion.

## Sistema de gamificacion

- **4 arquetipos** con colores, fortalezas y retos unicos
- **8 batallas** secuenciales con progresion y barra de XP
- **6 personajes** seleccionables con avatares y figuras de cuerpo completo
- **Sistema de rareza** en armas: Comun (gris), Raro (verde), Epico (purpura), Legendario (dorado)
- **Leaderboard** comunitario con avatares unicos
- **Marcos RPG** ornamentados con diamantes, esquinas y filigranas

## Interacciones

- Marcos de carta RPG con ornamentos, diamantes y patron de grabado
- Particulas flotantes (cenizas/brasas) con color del arquetipo
- Parallax en heroes al mover el raton
- Bandera interactiva con animacion de ondeo
- Gladiador interactivo con chispas al click
- Sonidos metalicos via Web Audio API (click, swoosh, hover, select)
- Transiciones de pagina (fade en desktop, slide en mobile)
- Smooth scroll con Lenis
- Barra de scroll progress en el header
- Tour de onboarding guiado de 17 pasos multi-pagina

## Responsive

- **Desktop** (>1280px): diseno completo con sidebar, flag banner, ornamentos
- **Laptop** (1025-1280px): paddings reducidos
- **Tablet** (769-1024px): tab bar centrada, columnas adaptadas, sidebar oculta
- **Mobile** (<=768px): tab bar inferior, header minimo, cards full-width, journey map en grid

## Estructura

```
index.html              Pagina principal (Dashboard)
player.html             Perfil del gladiador
modulos.html            Modulos / batallas
armeria.html            Armeria de entrenamientos
coliseo.html            Comunidad y leaderboard

css/styles.css          Estilos minificados
css/tailwind.min.css    Tailwind pre-built (solo clases usadas)
js/main.js              Interacciones, particulas, sonidos, parallax (minificado)
js/module-selector.js   Selector de arquetipos, personajes y modulos (minificado)
js/onboarding.js        Tour guiado de 17 pasos (minificado)

img/                    Assets optimizados (WebP, SVG)
fonts/                  Heroes Legend (WOFF2 + TTF)
```

## Paleta de colores

| Elemento | Color |
|----------|-------|
| Fondo | `#111`, `#1a1a1a` |
| Texto | `#f0f0e8` (claro), `#999` (muted) |
| Dominus | `#75e21c` (verde) |
| Structor | `#ffc42e` (dorado) |
| Invictus | `#f97316` (naranja) |
| Nexus | `#60a5fa` (azul) |
| Raro | `#75e21c` (verde) |
| Epico | `#9e58f5` (purpura) |
| Legendario | `#ffc42e` (dorado) |

## Como usar

1. Clonar el repositorio
2. Abrir `index.html` en el navegador
3. Usar el boton flotante (esquina inferior derecha) para cambiar arquetipos, personajes y modulos
4. Pulsar "Aplicar Cambios" para ver la nueva configuracion
5. Navegar entre las 5 pantallas

No requiere servidor, build ni instalacion.

## Notas

- Es un prototipo visual, no hay logica de negocio real
- Los datos son estaticos (no hay backend)
- El tour de onboarding se muestra automaticamente la primera vez; se puede reiniciar desde el footer
- Los archivos fuente (*.src.js, styles.src.css) no se incluyen en el deploy
