# Planazo

Plataforma para descubrir restaurantes, discotecas, hoteles y eventos en un **mapa en tiempo real** de Zona G y Zona T (Chapinero, Bogotá), con un **agente** que arma la ruta del plan. Proyecto académico de arquitectura de microservicios: seis retos de **tiempo real** y **concurrencia** demostrados sobre un producto real.

**Empieza por [`docs/contexto.md`](https://github.com/planazo-team/planazo-frontend/blob/main/docs/contexto.md).** Ahí está el producto, el equipo, los contratos y cómo correr todo.

**En producción:** https://planazo-frontend.vercel.app (Vercel), contra los cinco servicios en Railway: gateway `planazo-api-gateway-production.up.railway.app`, realtime `planazo-realtime-production.up.railway.app`, game `planazo-game-production.up.railway.app`; booking y promo solo por red privada. Entra con cualquiera de los nueve usuarios semilla.

| Repo | Qué es | Dueño |
|---|---|---|
| [planazo-frontend](https://github.com/planazo-team/planazo-frontend) | Next.js: app del cliente y panel del negocio · **documentación del proyecto** en `docs/` | Juan Diego |
| [planazo-api-gateway](https://github.com/planazo-team/planazo-api-gateway) | Entrada HTTP: JWT, CORS, rate limit, proxy · módulo `agent` | Juan Diego |
| [planazo-booking](https://github.com/planazo-team/planazo-booking) | Catálogo, franjas, cupos y reservas · **CC-3**, RT-1 | Fabián |
| [planazo-promo](https://github.com/planazo-team/planazo-promo) | Promociones de stock finito y cupones · **CC-1** | Fabián |
| [planazo-game](https://github.com/planazo-team/planazo-game) | Snake multijugador a 20 Hz y marcador, Java + Spring Boot · **RT-3**, **CC-2** | Diego Rozo |
| [planazo-realtime](https://github.com/planazo-team/planazo-realtime) | WebSocket, suscripciones por tópico y event log · **RT-2**, RT-1 | Juan Camilo |
| [planazo-infra](https://github.com/planazo-team/planazo-infra) | `docker compose` para todo en local, k6 de los retos, contratos, Bruno | Juan Diego |
| [planazo-service-template](https://github.com/planazo-team/planazo-service-template) | Plantilla NestJS de la que nacen booking, promo y realtime | Juan Diego |

Documentos: [dominios](https://github.com/planazo-team/planazo-frontend/blob/main/docs/dominios.md) · [diagramas](https://github.com/planazo-team/planazo-frontend/blob/main/docs/diagramas.md) · [arquitectura](https://github.com/planazo-team/planazo-frontend/blob/main/docs/arquitectura.md) · [seguridad](https://github.com/planazo-team/planazo-frontend/blob/main/docs/seguridad.md) · [plan y cronograma](https://github.com/planazo-team/planazo-frontend/blob/main/docs/plan-organizacion.md)

Cómo trabajamos: se entra a `main` por PR con CI verde y squash merge (GitHub lo exige en `planazo-frontend` y `.github`; en los privados es convención). Un cambio que toque rutas, cuerpos, headers o eventos lleva la etiqueta `contrato` y empieza por un PR a `planazo-frontend`.
