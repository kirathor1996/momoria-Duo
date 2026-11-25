# Cómo publicar cambios de la app (2026-11-25)

- Yo publico con clasp (ya logueado en la cuenta personal del usuario; credenciales en ~/.clasprc.json, no copiarlas).
- Carpeta de deploy: `version-compartida\deploy\` (tiene .clasp.json). El archivo del servidor ahí se llama `Código.js` (con tilde) y es copia de `version-compartida\Codigo.gs`.
- Pasos: copiar Codigo.gs -> deploy\Código.js e Index.html -> deploy\Index.html; `clasp push --force`; `clasp create-deployment --deploymentId AKfycbzNGocAA16Ij2djmPFmaNTlt0YcSc6pO4gEUqmRxBdBK-HytmuMKkVurlccXYbdR9vilQ --description "..."` (mantiene la misma URL /exec).
- Verificar: curl a https://script.google.com/macros/s/<deploymentId>/exec y buscar un texto nuevo.
- Acceso de la web app: ANYONE_ANONYMOUS (Agustina entra sin login).
- Versión 2 publicada 2026-11-25 con "Gastos fijos".
