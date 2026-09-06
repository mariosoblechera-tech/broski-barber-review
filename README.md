# Broski Barbería — Reseña

Mini página estática para pedir reseñas de Google, pensada para enlazar desde un código QR en local. Sustituye a un link plano de Google Maps por una página con la identidad de Broski Barbería.

## Qué hace

Muestra el logo, un selector de estrellas, un botón que redirige a la página de reseñas de Google del negocio y un enlace a Instagram. Al tocar una estrella, redirige automáticamente tras una breve animación.

## Desarrollo local

Es HTML estático puro, sin build. Para verlo localmente:

```bash
npx serve .
```

## Deploy en Vercel

1. Sube este repo a GitHub.
2. En [vercel.com/new](https://vercel.com/new), importa el repositorio.
3. Framework preset: **Other** (no requiere build command ni output directory).
4. Deploy.

Cuando tengas el dominio de Vercel (o uno propio conectado), genera un QR que apunte a esa URL y colócalo en el local.

## Actualizar el enlace de reseña

El link de Google está en `index.html`, en el atributo `href` del botón `#reviewBtn`. Usa el CID numérico del negocio: `https://search.google.com/local/writereview?placeid=<CID>`.
