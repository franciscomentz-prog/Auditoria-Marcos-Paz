# GUÍA DE INSTALACIÓN — Auditoría Institucional PWA
## Clínica Marcos Paz

---

## ARCHIVOS DEL PAQUETE

```
auditoria-pwa/
├── index.html       ← La app completa
├── manifest.json    ← Configuración PWA
├── sw.js            ← Service Worker (offline)
├── icons/
│   ├── icon-192.png ← Ícono para Android/iOS
│   └── icon-512.png ← Ícono splash screen
└── INSTRUCCIONES.md ← Este archivo
```

---

## PASO 1 — Crear los íconos

Necesitás dos imágenes PNG:
- `icons/icon-192.png` (192×192 px)
- `icons/icon-512.png` (512×512 px)

Podés usar el logo de la clínica o un ícono de clipboard/checklist.
Herramientas gratuitas: https://realfavicongenerator.net

---

## PASO 2 — Crear cuenta en GitHub (si no tenés)

1. Ir a https://github.com
2. Registrarse con cualquier email
3. Crear un repositorio nuevo → nombre: `auditoria-cmp`
4. Marcar como **Público**

---

## PASO 3 — Subir los archivos

### Opción A — Desde el navegador (más fácil):
1. Dentro del repositorio, hacer clic en **"uploading an existing file"**
2. Arrastrar los 4 archivos: `index.html`, `manifest.json`, `sw.js`, y la carpeta `icons/` con los dos PNG
3. Clic en **"Commit changes"**

### Opción B — Con GitHub Desktop (si preferís interfaz visual):
1. Descargar GitHub Desktop: https://desktop.github.com
2. Clonar el repositorio
3. Copiar los archivos a la carpeta del repositorio
4. Hacer commit y push

---

## PASO 4 — Activar GitHub Pages

1. En el repositorio, ir a **Settings** (engranaje)
2. En el menú izquierdo: **Pages**
3. En "Source": seleccionar **Deploy from a branch**
4. Branch: **main** | Folder: **/ (root)**
5. Clic en **Save**

Después de 1-2 minutos, tu app va a estar disponible en:
```
https://TU-USUARIO.github.io/auditoria-cmp/
```

---

## PASO 5 — Instalar como app en el celular

### Android (Chrome):
1. Abrir Chrome y navegar a la URL del paso 4
2. Tocar el menú (⋮) → **"Agregar a pantalla de inicio"**
3. Confirmar → aparece el ícono en el inicio como una app normal

### iPhone (Safari):
1. Abrir Safari (obligatoriamente Safari, no Chrome)
2. Navegar a la URL del paso 4
3. Tocar el botón compartir (□↑) → **"Agregar a pantalla de inicio"**
4. Confirmar → aparece el ícono en el inicio

---

## CARACTERÍSTICAS DE LA APP

✅ Funciona SIN internet (offline) una vez instalada
✅ Guarda progreso automáticamente (localStorage)
✅ No se pierden los datos al cerrar la app
✅ Dashboard con semáforos en tiempo real
✅ Exportación de resultados a .txt
✅ Compatible con Android e iPhone
✅ Sin costo de servidor

---

## ACTUALIZAR LA APP

Cuando quieras modificar el formulario:
1. Editar el archivo `index.html`
2. Cambiar el número de versión en `sw.js`: `const CACHE_NAME = 'auditoria-v2'` (v2, v3, etc.)
3. Subir los archivos actualizados a GitHub
4. Los usuarios verán la actualización automáticamente al abrir la app con conexión

---

## SOPORTE

Cualquier duda técnica podés consultarla directamente en la siguiente conversación con Claude.
