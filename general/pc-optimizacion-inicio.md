# Optimización de la PC (2026-11-18)

- PC: i5-10400F, 32 GB RAM, 2 SSD Kingston, RTX 3060 Ti. El hardware no es el problema.
- Se desactivaron del inicio (vía StartupApproved, reversible desde Administrador de tareas → Aplicaciones de arranque): Riot Client, Riot Vanguard (bandeja), Steam, EA, D4Builds, SignalRGB, LonelyScreen, Sideloadly, Unified Remote, Adobe Acrobat Synchronizer, Edge, Firefox, Microsoft Lists, FxSound, Wondershare x2.
- Se dejaron: Alba Group agentes (trabajo, C:\Users\AGUSTIN\Desktop\alba-agentes), Ollama (lo usan los agentes de Alba), OneDrive, Tailscale, LG HUB, SteelSeries GG, Seagull (impresora), Realtek, antivirus, Apprunner (sin identificar).
- Trampa: la sesión no corre como admin; los ítems HKLM/Common Startup requieren elevar con Start-Process -Verb RunAs.
