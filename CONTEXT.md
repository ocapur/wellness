# Wellness OS — Contexto (cold-boot)

Doc maestro de este proyecto. Léelo completo al iniciar sesión de wellness. Actualízalo al cerrar cada sesión relevante.

---

## Qué es esto
Sistema de ejercicio + nutrición de Omar. Meta: constancia > intensidad, de por vida.
- Objetivo #1: masa muscular y fuerza
- Objetivo #2: longevidad (Z2 + VO2max + fuerza + mobility)
- Objetivo #3: cognitivo (correr en ayunas + creatina + sueño)

**Sitio vivo:** wellness.capur.co (repo `ocapur/wellness`, GitHub Pages, HTTPS activo)
**Contenido:** `index.html` — semana completa, día actual auto-destacado (JS por día CDMX), cada ejercicio clickeable con how-to + do's/don'ts + link a demo en video.

---

## Perfil
- 35 años (7 ago 1991), CDMX, Polanco. Hija Camila (7 meses en jul 2026).
- 13 años activo en fitness (crossfit → funcionales → running).
- Corre en Chapultepec, medita 20min a media corrida 3x/semana (Lun/Mié/Vie).
- Equipo: mancuernas ajustables (25lb→30kg y subiendo), parque público con barras/tubos en Polanco/Chapultepec.
- Ayuno intermitente 16:8 hace 4+ meses: come 2pm-8pm, café solo AM.

## Baseline — Fitness-50 Benchmark (enero 2026)
| Test | Resultado |
|---|---|
| Push-up 50s | 42 |
| Plank | 4:00 |
| Squats 50s | 50 |
| Wall squat hold | 84s |
| Lunges 50s | 40 |
| Grip test | 60s |
| **Sit-to-rise** | **0** ⚠️ prioridad |
| Single leg balance | 60s |
| 1 mile run | 10:30 |
| 25 burpees | 1:04 |

**Próximo re-test: octubre 2026** (6 meses). Ahí se miden resultados reales, no sensaciones.

---

## Sistema actual (vigente desde jul 2026)

**Semana:**
- Lun — Run Z2 easy, 3km+meditar+3km
- Mar — Strength HOME (dumbbells)
- Mié — Run Chapultepec Z2 + meditar
- Jue — Strength PARK (bodyweight, llega corriendo)
- Vie — Run Intervals VO2max (10min calentar + 6×[1min fuerte/2min suave] + 5min enfriar = 33min) + meditar al final
- Sáb — Long run Z2, 6km+
- Dom — Rest + mobility

**Diario no-negociable:** 30 push-ups · 10g creatina (monohidratada, con comida, cualquier hora) · mobility regada (movement snacks, no bloque) · 2.5L agua

**Nutrición:** 16:8 (2pm-8pm) · 170g proteína/día, proteína primero · finde: 1 comida libre no finde libre, alcohol tope 2-3

---

## Decisiones y por qué (no repetir el debate)

- **Creatina 10g, no 5g.** 5g satura músculo; cerebro necesita más (barrera hematoencefálica) — con meta cognitiva, 10g es el sweet spot. 20g es excesivo para uso diario.
- **Solo 2 días fijos de fuerza.** Con 4-5 corridas/semana, el limitante es recuperación no días. 30 push-ups diarios son la micro-dosis extra. 3er día opcional (upper, 15min) solo si recupera bien — no antes de 4 semanas de base.
- **Ritmo Z2 = conversación, no pace fijo.** ~7:00/km es guía, no regla. Solo viernes va rápido.
- **Farmer carry se mide en segundos con peso variable, no metros fijos.** Regla: si aguanta 50s+ fácil, sube peso.
- **Progresión de peso — regla "2 de sobra":** todas las series completas con 2+ reps en el tanque, 2 entrenos seguidos → sube el mínimo incremento disponible.
- **Sit-to-rise en niveles, no de golpe:** ① con 1 mano → ② solo dedos → ③ sin nada. Sube de nivel solo cuando el actual sale fácil.
- **Mobility es "movement snacks", no sesión de 5min.** Regarlo en el día (deep squat viendo cel, 90/90 al final de correr) — la sesión en bloque no se sostenía.

## Log de ajustes (más reciente arriba)

**Ago 2026 — retro mes 1:**
- Corriendo 7-8km por sesión (arriba del plan original 4-6km), viernes ~6km con sprints. On track, ningún ajuste al volumen aún — vigilar sueño.
- Park: pull-ups tope en 5, dips 6-7, push-ups fatiga notoria (40→15). → Agregadas 3 negativas post-serie en pull-ups para romper techo.
- Home: ya no cuesta trabajo con 25→30kg. Farmer carry aguanta 50s (señal de peso ligero). → Ajustado a regla de peso variable + nota "regla 2 de sobra" visible en la página.
- Deep squat hold: cuesta trabajo a los 2min → confirmado que es la señal correcta, no ajustar.
- Sit-to-rise: aún no sale → agregada progresión en 3 niveles.

**Jul 2026 — lanzamiento:**
- Baseline Fitness-50 revisado (enero 2026), sistema diseñado desde cero.
- Site v1→v2: agregado desglose de semana + highlight de "hoy" + do's/don'ts + demos en video + warm-up en Home day (5 min, escalera: jumping jacks→arm/leg swings→bodyweight squats→push-ups lentos→goblet ligero).
- Descansos entre sets estandarizados: 90s ejercicios grandes, 60s core/chicos.
- Deploy: repo `ocapur/wellness` → GitHub Pages → CNAME `wellness.capur.co` en Cloudflare (DNS only) → HTTPS activo.

---

## Próximos hitos
- [ ] Re-test Fitness-50 completo — octubre 2026
- [ ] Evaluar 3er día de fuerza opcional (upper, 15min) si recuperación es buena
- [ ] Posible registro de comidas por foto (aprox, no preciso) — pendiente decidir formato
- [ ] Samsung Health: sin API simple. Por ahora, input manual vía screenshot en chat.

## Notas técnicas
- Repo: `ocapur/wellness` (público). PAT: `ocapur-master` (agregar scope si falta permiso de Pages vía API — hasta ahora activado manual desde GitHub UI).
- Deploy: push a `main` → GitHub Pages sirve `index.html` desde root automáticamente. No hay build step, es HTML/CSS/JS puro sin dependencias.
- `CNAME` file en el repo apunta a `wellness.capur.co` — no borrar.
