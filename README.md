# CSS course

## Curso 4. Efectos visuales y Movimientos en CSS

### Sombras

- box-shadow
- text-shadow
- filter: drop-shadow(valor valor valor color);

### Degradados

#### Lineal

```css
background-image: linear-gradient(red, green);
background-image: linear-gradient(90deg, red, green, blue);
background-image: linear-gradient(to top right, red, green, blue);
```

#### Radial

```css
background-image: radial-gradient(
  circle 100px,
  cyan 30%,
  magenta 60%,
  yellow 90%
);
background-image: radial-gradient(
  circle 100px at bottom,
  cyan 30%,
  magenta 60%,
  yellow 90%
);
background-image: radial-gradient(circle 100px, red 50%, white 50%);
```

#### Conic

```css
background-image: conic-gradient(
  from 90deg,
  red 0deg 120deg,
  white 120deg 240deg,
  blue 240deg
);
```

#### Patrones con degradados

```css
background-image: repeating-conic-gradient(
  red 0 8%,
  yellow 8% 16%,
  black 16% 24%
);
background-image: repeating-radial-gradient(
  circle 4rem,
  cyan 0 10px,
  magenta 10px 20px,
  yellow 20px 30px
);
```

#### Gráficas con degradados

```css
.donut-gradient {
  background-image: radial-gradient(white 30%, black 31%, transparent 33%),
    conic-gradient(cyan 0 50%, magenta 50% 80%, yellow 80%);
  border-radius: 50%;
}
```

### Filtros

```css
.card img {
  filter: blur(0.5rem);
  filter: brightness(0.5);
  filter: contrast(0.2);
  filter: grayscale(0.75); /* 0-1 */
  filter: sepia(1); /* 0-1 */
  filter: hue-rotate(50deg); /* deg=degree */
  filter: invert(1); /* 0-1 */
  filter: opacity(0.5); /* 0-1 */
  filter: saturate(4);
}
```

#### Filtros degradados

```css
.filters-multiple {
  filter: blur(0.2rem) hue-rotate(270deg) opacity(0.57) invert(1);
}
```

#### Modos de mezcla

- Para imagenes superpuestas (preferente)
- Se aplica sobre los elemento hijos

```css
.blend-modes img {
  mix-blend-mode: normal;
  mix-blend-mode: color;
  mix-blend-mode: color-dodge;
  mix-blend-mode: color-burn;
  mix-blend-mode: screen;
  mix-blend-mode: multiply;
  mix-blend-mode: saturation;
  mix-blend-mode: luminosity;
  mix-blend-mode: hue;
  mix-blend-mode: exclusion;
  mix-blend-mode: difference;
  mix-blend-mode: hard-light;
  mix-blend-mode: soft-light;
  mix-blend-mode: lighten;
  mix-blend-mode: overlay;
  mix-blend-mode: darken;
}
```

#### Modos de mezcla a imagenes de fondo

```css
.bg-blend-mode {
  background-image: url("../assets/Cat03.jpg"), url("../assets/paisaje.jpg");
  background-size: cover;
  /*
  background-blend-mode: normal;
  background-blend-mode: color;
  background-blend-mode: color-dodge;
  background-blend-mode: color-burn;
  background-blend-mode: screen;
  background-blend-mode: multiply;
  background-blend-mode: saturation;
  background-blend-mode: luminosity;
  background-blend-mode: hue;
  background-blend-mode: exclusion;
  background-blend-mode: difference;
  background-blend-mode: hard-light;
  background-blend-mode: soft-light;
  background-blend-mode: lighten;
  background-blend-mode: darken;
  background-blend-mode: overlay;
  */
  background-blend-mode: multiply;
}
```

### Máscaras (clip-path)

[CSS clip-path maker](https://bennettfeely.com/clippy/)

```css
.clip-path {
  clip-path: circle();
  clip-path: circle(100px at auto);
  clip-path: circle(100px at left);
  clip-path: circle(100px at 30% 60%);
  clip-path: ellipse();
  clip-path: ellipse(100px 50px at right);
  clip-path: inset(4rem);
  clip-path: inset(1rem round 1rem 6rem 6rem 6rem);
  clip-path: polygon(0 0, 100% 0, 50% 100%);
  clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
}
```

### Formas (shape-outside)
