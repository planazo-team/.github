## Qué cambia

<!-- Una o dos frases. Si cierra un issue: "Cierra #12". -->

## Reto que toca

- [ ] RT-1 mapa en tiempo real · [ ] RT-2 consistencia ante desconexión · [ ] RT-3 leaderboard en vivo
- [ ] CC-1 promociones limitadas · [ ] CC-2 leaderboard concurrente · [ ] CC-3 cupos limitados
- [ ] Ninguno (infra, docs, refactor)

## ¿Cambia el contrato?

- [ ] **No.** Rutas, cuerpos, headers y eventos quedan igual.
- [ ] **Sí.** Ya está el PR a `planazo-frontend` (`types.ts` + `docs/contexto.md`) y `planazo-infra/contracts/` → enlace: 

## Cómo se probó

<!-- Comandos o pasos. Para recurso finito: el k6 con cero sobreventas. Para tiempo real: cortar y reconectar sin pérdida ni duplicados. -->

## Checklist

- [ ] `npm run typecheck`, `lint`, `test` y `build` pasan en local
- [ ] Los errores responden `{ code, message }` con los códigos que el frontend conoce
- [ ] No se subió ningún secreto (`.env` está en `.gitignore`)
- [ ] README o docs actualizados si algo cambió para los demás
