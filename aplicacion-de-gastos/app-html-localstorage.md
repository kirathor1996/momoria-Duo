# App de gastos: estado inicial (2026-11-24)

- La app es un solo archivo `index.html` en la carpeta del proyecto (HTML+JS, sin servidor).
- Guarda los datos en localStorage del navegador, clave `gastos_agus_v1`. Cada gasto: {id, fecha (YYYY-MM-DD), desc, cat, monto, quien: "Agustina"|"Agustín"}.
- Tiene: carga/edición/borrado, resumen por mes con total por persona, lista agrupada por día, exportar CSV (separador ; para Excel en español), respaldo/restauración JSON.
- Limitación: los datos no se comparten entre dispositivos. Si piden usarla desde dos celulares hace falta una base en la nube (ej. Firebase/Supabase o Google Sheets).
