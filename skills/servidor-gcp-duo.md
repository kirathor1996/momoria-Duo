# Servidor en Google Cloud para correr Duo (2026-11-22)

- Objetivo del usuario: armar agentes con subagentes que trabajen de forma independiente, con cargos, sectores y tareas, desde un servidor siempre prendido.
- Decisión propuesta: Duo es una app de escritorio de Windows, así que se instala DENTRO de la VM Windows Server 2025 (GCP, us-east1). No se "conecta" a la nube de otra forma.
- El portal Open WebUI + OpenRouter NO se conecta con Duo ni corre sus agentes/skills: se recomendó dejarlo para después (opcional).
- Se entregó el script de la fase 1 para Cloud Shell: proyecto, facturación, presupuesto de USD 220, VM, IP fija, firewall solo a la IP del usuario y apagado a las 23:00.
- TRAMPAS: Cloud Shell NO ve la IP de la PC (hay que leerla en ifconfig.me desde la PC). Un proyecto nuevo trae la regla default-allow-rdp abierta a 0.0.0.0/0, que hay que borrar. El presupuesto solo avisa, no corta el gasto. Si se apaga a las 23:00, los agentes no trabajan de noche. La memoria de Duo es local, así que la PC y el servidor no la comparten solos.
- Pendiente: fase 2 (Tailscale + Windows App + cerrar 3389 + instalar Duo en el servidor). Fase 3 opcional (portal).
