# Gladiadores de las Ventas — Prototipo Frontend

Prototipo interactivo de frontend para una academia de ventas gamificada con narrativa de gladiadores romanos. Diseñado para presentar la experiencia completa del producto antes del desarrollo.

## Vista previa

El prototipo incluye 5 pantallas navegables con interacciones, animaciones y un sistema de personalización completo.

## Pantallas

| Pantalla | Archivo | Descripcion |
|----------|---------|-------------|
| Dashboard | `index.html` | Ludus Magnus — mapa de progreso, proxima batalla, clase en vivo |
| Perfil | `player.html` | Perfil del gladiador — arquetipo, estadisticas, arsenal de armas |
| Modulos | `modulos.html` | Las 8 Batallas — sidebar de progreso, clase del lanista, recursos |
| Armeria | `armeria.html` | Entrenamientos adicionales — busqueda, filtros, grid de cursos |
| Coliseo | `coliseo.html` | Comunidad — Discord, leaderboard, eventos |

## Stack

- **HTML5** — paginas estaticas multi-page
- **Tailwind CSS v3** — via CDN
- **Vanilla JavaScript** (ES6+) — sin dependencias
- **CSS custom properties** — design tokens y tematizacion dinamica
- **Lenis** — smooth scroll (via CDN)
- **Web Audio API** — efectos de sonido metalicos

Sin framework, sin build tools, sin npm. Abrir cualquier HTML directamente en el navegador.

## Sistema de personalizacion

El prototipo incluye un **selector flotante** (boton en esquina inferior derecha) que permite cambiar en tiempo real:

- **Arquetipo** (4): Dominus (verde), Structor (dorado), Invictus (naranja), Nexus (azul)
- **Personaje** (6): Servus, Ventas, Veteranus, Orator, Lanista, Imperator
- **Modulo activo** (1-8): cambia el estado de progreso en toda la app

Todos los colores, glows, bordes, iconos y contenido se adaptan dinamicamente.

## Sistema de gamificacion

- **4 arquetipos** con colores, fortalezas y retos unicos
- **8 batallas** secuenciales con progresion y XP
- **6 personajes** seleccionables con avatares de cuerpo completo
- **Sistema de rareza** en armas: Comun, Raro, Epico, Legendario
- **Leaderboard** comunitario
- **Barra de XP** dinamica segun modulo

## Interacciones

- Marcos RPG ornamentados con diamantes, esquinas decorativas y glows
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
- **Tablet** (769-1024px): tab bar centrada, columnas adaptadas
- **Mobile** (<=768px): tab bar inferior, header minimo, cards full-width, journey map en grid

## Estructura

```
index.html          Pagina principal (Dashboard)
player.html         Perfil del gladiador
modulos.html        Modulos / batallas
armeria.html        Armeria de entrenamientos
coliseo.html        Comunidad y leaderboard

css/styles.css      Estilos globales, tokens, animaciones, responsive
js/main.js          Interacciones, particulas, sonidos, parallax
js/onboarding.js    Tour guiado de 17 pasos
js/module-selector.js  Selector de arquetipos, personajes y modulos

img/                Assets (SVG, WebP, PNG, JPG)
fonts/              Heroes Legend (tipografia custom)
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

## Como usar

1. Clonar el repositorio
2. Abrir `index.html` en el navegador
3. Usar el boton flotante (esquina inferior derecha) para cambiar arquetipos, personajes y modulos
4. Navegar entre las 5 pantallas

No requiere servidor, build ni instalacion.

## Notas

- Es un prototipo visual, no hay logica de negocio real
- Los datos son estaticos (no hay backend)
- Las imagenes de personajes son assets de alta resolucion (algunos >3MB)
- El tour de onboarding se muestra automaticamente la primera vez; se puede reiniciar desde el footer
