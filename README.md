<div align="center">

# itla-profile-modal-remover

**Elimina el molesto modal obligatorio de foto de perfil del Aula Virtual del ITLA — automáticamente y sin interrupciones.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Stylus](https://img.shields.io/badge/Stylus-CSS-orange)](https://add0n.com/stylus.html)
[![ITLA](https://img.shields.io/badge/Para-ITLA-green)](https://aulavirtual.itla.edu.do)
[![Stars](https://img.shields.io/github/stars/anthonygzm/itla-profile-modal-remover?style=social)](#)

---

### ⭐ ¡Apoya el proyecto!

Si este userscript te fue útil, considera darle una **estrella al repositorio** para apoyar el proyecto <3.

</div>

---

## ¿Qué problema resuelve?

Cada vez que inicias sesión en `aulavirtual.itla.edu.do`, aparece este modal:

<img width="506" height="547" alt="Image" src="https://github.com/user-attachments/assets/938da6ca-e6f9-4660-9043-ff9e9ba68a79" />

Bloquea toda la página y no te deja hacer nada. Este estilo lo oculta permanentemente con CSS puro.

---

## Instalación

### Instala Stylus

Stylus es una extensión gratuita para aplicar CSS personalizado en cualquier sitio web.

| Navegador | Enlace |
|-----------|--------|
| Chrome | [Instalar](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne) |
| Firefox | [Instalar](https://addons.mozilla.org/es/firefox/addon/styl-us/) |
| Edge | [Instalar](https://microsoftedge.microsoft.com/addons/detail/stylus/fjnbnpbmkenffdnngjfgmeleoegfcffe) |

---

### Crea el estilo

1. Haz clic en el ícono de **Stylus** en tu navegador
2. Selecciona **"Escribir nuevo estilo"**
3. Borra todo el contenido que aparece por defecto
4. Copia y pega esto:

```css
@-moz-document domain("aulavirtual.itla.edu.do") {
  #asgp-overlay {
    display: none !important;
    visibility: hidden !important;
    opacity: 0 !important;
    pointer-events: none !important;
  }
  body.asgp-locked {
    overflow: auto !important;
    position: static !important;
    height: auto !important;
  }
}
```

5. En el campo **"Nombre"** escribe: `Eliminar Modal ITLA`
6. Guarda con `Ctrl + S`

---

### 3️⃣ Verifica que funciona

- Entra a `aulavirtual.itla.edu.do` e inicia sesión
- El modal **no debe aparecer** ✅
- El ícono de Stylus debe mostrar el número **`1`** en esa página, indicando que el estilo está activo

---

## ¿No funciona?

Revisa estas cosas en orden:

| Problema | Solución |
|----------|----------|
| El modal sigue apareciendo | Recarga la página con `Ctrl + Shift + R` |
| Stylus no se activa | Verifica que el toggle del estilo esté en azul |
| URL diferente | Asegúrate de estar en `aulavirtual.itla.edu.do` exactamente |

Si nada de eso funciona, abre la consola del navegador (`F12 → Console`) y pega esto para quitarlo manualmente mientras tanto:

```js
document.querySelector('#asgp-overlay').style.cssText = 'display:none!important';
document.body.classList.remove('asgp-locked');
document.body.style.overflow = 'auto';
```

---

## Autor

**Anthony Guzman**
GitHub: [@anthonygzm](https://github.com/anthonygzm) 
