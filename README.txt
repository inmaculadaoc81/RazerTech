RAZERTECH ONE PAGE

Dominio: https://madridtechsupport.com.es/
Teléfono caja y botones: +34 914 46 85 03

Variables SMTP compartidas en Vercel:
SMTP_HOST=cp7124.webempresa.eu
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=soporte@kelatos.com
SMTP_PASS=[configurada solo en Vercel]
CONTACT_EMAIL=soporte@kelatos.com

El correo no aparece visible en la web; solo se usa en backend.

Google Analytics:
G-JFW2B4QZMG

HISTORIAL: el repositorio era multipágina (18 páginas /modelos/ de
Blade/Blade Stealth/Razer Book y varias páginas /servicios/) y se
convirtió a one-page; esas páginas fueron eliminadas en commits
anteriores. Como ya no existen en el sitemap actual, se ha añadido
middleware.mjs para redirigir (301) cualquier URL antigua a la home,
evitando 404 en enlaces indexados o backlinks antiguos. Excluye
/api/* y cualquier ruta con extensión de archivo. Se añadió
"@vercel/functions": "^2.0.3" a package.json como dependencia de esta
función.

REVISIÓN (fixes aplicados en esta pasada):
- Ya estaba bien: menú móvil, api/contacto.js con SMTP + nodemailer,
  teléfono +34 914 46 85 03 consistente en toda la web (no se ha
  tocado). No se ha modificado ninguno de estos.
- Google Analytics: no existía. Añadido G-JFW2B4QZMG.
- Meta robots: no existía. Añadido.
- Schema.org: no existía. Añadido LocalBusiness (nombre, url,
  teléfono, descripción, dirección, areaServed Madrid, sameAs con
  Google Maps y YouTube).
- Sección SEO: no existía. Añadida sección "Guía" (id="guia", enlazada
  en el menú) con contenido propio sobre averías habituales en
  equipos Razer.
- Banner de cookies: no existía. Añadido (Aceptar / Rechazar /
  Política de privacidad → https://kelatos.com/privacy-policy/), con
  diseño apilado a ancho completo en móvil.
- Borde blanco del botón del chat: faltaba (el chat ya tenía un color
  azul personalizado, se mantuvo, solo se añadió el borde).
- .navcall: el texto largo ("Atención Telefónica 24 horas 365 días")
  deformaba la píldora del menú. Acortado a solo el número (mismo
  número, +34 914 46 85 03) y añadido white-space:nowrap como
  salvaguarda. El botón grande .cta.phone del hero conserva su texto
  completo.
- H1 de portada reescrito, corto, directo y totalmente afirmativo
  (sin interrogación ni condicionales), incluye la marca: "Tu Razer
  no responde. Aquí lo revisamos sin compromiso." Tamaño del H1
  aumentado: clamp(38-58px) → clamp(46-74px) en escritorio, 40px →
  48px en móvil.

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente):
- H1 repetía la estructura "no responde. Aquí lo [verbo] [coletilla]"
  usada en AcerGlobal. Reescrito con estructura de una sola frase,
  imperativa: "Repara tu Razer sin perder tus archivos." (7 palabras).
- BUG REAL — texto decorativo ".data-art:before" ("DATA", 120px) sin
  reducción de tamaño en móvil/tablet, mismo patrón que otros repos
  de la familia. Añadida reducción (80px tablet, 50px móvil).
- BUG REAL — el formulario no tenía ninguna casilla de consentimiento
  de política de privacidad. Añadida, con enlace a
  https://kelatos.com/privacy-policy/ en azul y subrayado.
- Añadida franja de aviso de servicio técnico independiente debajo
  del menú (no existía).
- Añadido "Sábados, domingos y días festivos estamos cerrados" debajo
  del horario.
- Botón "Atención Telefónica..." sin icono, a diferencia del de
  WhatsApp. Añadido.
- Verificado: schema.org ya usaba correctamente el único teléfono que
  tiene este repo (no hay número propio distinto de información); no
  se ha tocado. Formulario verificado: fetch a /api/contacto coincide
  con api/contacto.js; conexión correcta.
