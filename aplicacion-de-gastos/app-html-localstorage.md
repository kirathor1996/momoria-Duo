# App de gastos: estado inicial (2026-11-24)

- La app es un solo archivo `index.html` en la carpeta del proyecto (HTML+JS, sin servidor).
- Guarda los datos en localStorage del navegador, clave `gastos_agus_v1`. Cada gasto: {id, fecha (YYYY-MM-DD), desc, cat, monto, quien: "Agustina"|"Agustín"}.
- Tiene: carga/edición/borrado, resumen por mes con total por persona, lista agrupada por día, exportar CSV (separador ; para Excel en español), respaldo/restauración JSON.
- Limitación: los datos no se comparten entre dispositivos. Si piden usarla desde dos celulares hace falta una base en la nube (ej. Firebase/Supabase o Google Sheets).

## Actualización 2026-11-24
- El usuario aclaró: es para gastos PERSONALES de la pareja (Agustina y Agustín), NO de la empresa. No mezclar con cuentas/herramientas de trabajo.
- Se hizo `version-compartida/` (Codigo.gs + Index.html + COMO-INSTALAR.txt): Google Apps Script como aplicación web, datos en la pestaña "Gastos" de una Google Sheet de la cuenta personal. Columnas: id, Fecha (texto ISO), Descripción, Categoría, Monto, Quién. Así los dos ven lo mismo desde el celular.
- La instalación la hace el usuario (necesita su login de Google). Para actualizar código: Gestionar implementaciones > Nueva versión (mantiene la URL).
- (2026-11-24) INSTALADA: proyecto Apps Script "Gastos de la casa" en script.google.com (proyecto suelto, no dentro de una planilla; Codigo.gs crea sola la planilla "Gastos casa (datos)"). Versión 1 implementada como app web; la URL /exec la tiene el usuario. No le gusta nada que parezca Excel: quiere usarla como app del celular.
