# 🤖 CRM Agéntico para Instagram y WhatsApp

## 1. Qué es el proyecto y para quién es
- **Qué es:** Un CRM integral con Agente de IA entrenado que automatiza la respuesta a comentarios de Instagram redirigiéndolos al DM con precios y tallas reales del catálogo, atiende DMs entrantes, realiza seguimiento automático y deriva la conversación a un humano cuando detecta intención de compra (con alerta sonora en escritorio y respaldo en Telegram).
- **Para quién es:** Para gestionar ventas propias por Instagram (Cuenta Creador `@patriciamdev`) y WhatsApp, permitiendo trabajar con un rol de **Administrador** (control total) y **Usuarios Adjuntos** (solo atención de Bandeja de Chats y Tablero de Clientes).

## 2. Arquitectura y Piezas Ensambladas (Astro + Tailwind CSS)
- `src/layouts/LayoutCRM.astro`: Armazón visual, selector de permisos (Admin vs. Usuario Adjunto) y notificaciones emergentes.
- `src/components/TableroKanban.astro`: Tablero de seguimiento en 5 etapas (*Pidió info*, *Pasé precio*, *Esperando pago*, *Vendido*, *Más adelante*).
- `src/components/CatalogoProductos.astro`: Gestión de productos, precios, stock, variantes y palabras clave (Keywords) para activar respuestas.
- `src/components/BandejaChats.astro`: Centro de mensajería filtrado por *Requiere Humano*, *Por leer* y *Atendido por IA*, más simulador de comentarios y DMs.
- `src/components/ConfiguradorAgente.astro`: Entrenamiento de Personalidad, Pautas, Acciones (`Cuando -> Hacer`), Límites, Alerta Sonora Web Audio y Bot de Telegram.
- `src/components/PanelEstadisticas.astro`: Métricas en vivo (Leads únicos, Conversaciones IA, Tasa de derivación, Tiempo de respuesta, Por leer y Respaldos Telegram) y gestión de Usuarios Adjuntos.

## 3. Plan por Fases Completado
- [x] **Fase 1:** Estructura del CRM en Astro, Control de Roles (Admin vs. Usuario Adjunto) y Catálogo de Productos.
- [x] **Fase 2:** Bandeja de Chats ("Por leer y atender") y Automatizador de Comentarios de Instagram a DM.
- [x] **Fase 3:** Entrenamiento del Agente IA, Derivación a Humano, Alerta Sonora en Desktop y Respaldo en Telegram.
- [x] **Fase 4:** Panel de Estadísticas en vivo, Gestión de Equipo, documentación `PROYECTO.md` y preparación para Vercel.

## 4. Reglas de Trabajo del Proyecto
- Explicaciones siempre en español simple (cada término técnico se explica en 1 línea).
- Control de versiones con Git al cierre de cada fase.
- Separación estricta de permisos: los Usuarios Adjuntos nunca pueden modificar el Catálogo, la IA ni la estructura del sistema.