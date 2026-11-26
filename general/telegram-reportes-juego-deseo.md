---
name: telegram-reportes-juego-deseo
description: Cómo leer el grupo de Telegram "Negocios con DamicoBULL" (reportes diarios del bot Rentabilidad CS) y dónde quedó el resumen de octubre 2026
metadata:
  type: reference
---

(2026-11-25)
- Telegram Web (K) está logueado en el Chrome de MAPLISH, puerto CDP 9445 (herramientas\chrome-maplish). Helper: herramientas\cdp\cdp.mjs <puerto> <archivo.js> 'web\.telegram'.
- Grupo "Negocios con DamicoBULL" = inputPeerChat chat_id 5463150752. Lo más rápido: rootScope.managers.apiManager.invokeApi('messages.getHistory', {peer, offset_date, limit:100,...}) en vez de scrollear el DOM. Ojo: location.hash no abre el chat; clickear desde el buscador.
- El bot (user id 8691569539) publica ~08:00 el reporte del día anterior en 2 mensajes: 1) Argentina (ARS, header "🎲 El Juego del Deseo — dd/mm/aaaa"), Chile (CLP), México, EE.UU., España; 2) Colombia, Italia, Alemania (Francia solo 1-2/10). Cada bloque: pedidos, facturación bruta/neta, publicidad USD, Margen (x% profit), y "Mes hasta hoy" con gastos del mes y Ganancia neta (% profit real).
- El margen operativo del mes que da el bot difiere de la suma de márgenes diarios (recalcula); pedidos y bruta sí cuadran.
- Resumen octubre 2026 hecho: entornos\general\reportes\juego-del-deseo-octubre-2026.xlsx
