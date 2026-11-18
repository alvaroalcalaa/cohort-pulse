# Cohort Pulse

> Analítica de retención por cohortes, privada y 100% en el navegador.

[English](#english) · [Demo rápida](#demo-rápida) · [MIT License](LICENSE)

## Español

**Cohort Pulse** convierte un CSV de eventos en una matriz de retención clara y accionable. Agrupa usuarios por su primera actividad, calcula su permanencia por semana y resalta qué cohortes están creciendo o perdiendo impulso. Todo se procesa localmente: el archivo nunca sale de tu navegador.

### Funcionalidades

- Importación de CSV con `user_id` y `event_date`.
- Cohortes semanales basadas en el primer evento de cada usuario.
- Tabla de retención con mapa de calor y tamaño de cada cohorte.
- Métricas rápidas: usuarios, cohortes y retención media de la primera semana.
- Exportación de la matriz calculada a CSV.
- Dataset de ejemplo incluido y sin dependencias ni backend.

### Stack

HTML5, CSS3 y JavaScript moderno (ES modules implícitos, sin build step).

### Cómo ejecutarlo

```bash
git clone https://github.com/alvaroalcalaa/cohort-pulse.git
cd cohort-pulse
python -m http.server 8000
```

Abre [http://localhost:8000](http://localhost:8000). También puedes abrir `index.html` directamente.

### Demo rápida

1. Pulsa **Cargar demo**.
2. Explora las cohortes de enero y febrero.
3. Importa tu propio CSV con este formato:

```csv
user_id,event_date
u-100,2026-01-05
u-100,2026-01-12
u-205,2026-01-08
```

`event_date` admite fechas ISO como `2026-01-05` o `2026-01-05T10:30:00Z`.

### Estructura

```text
├── index.html          # Interfaz
├── styles.css          # Diseño responsive
├── app.js              # Parser y cálculo de cohortes
├── sample-events.csv   # Datos de demostración
└── LICENSE             # MIT
```

### Ideas para extenderlo

Conectar una API de producto, añadir cohortes mensuales, segmentación por plan/canal o exportar una imagen para un informe de BI.

---

## English

**Cohort Pulse** turns an event CSV into a concise, actionable retention matrix. It groups users by their first activity, calculates weekly retention, and highlights cohorts that are gaining or losing momentum. Processing is fully local: your file never leaves the browser.

### Features

- CSV import using `user_id` and `event_date`.
- Weekly cohorts based on each user's first event.
- Retention table with heatmap and cohort size.
- Quick metrics: users, cohorts and average week-one retention.
- Export of the calculated matrix as CSV.
- Included sample data, zero dependencies and no backend.

### Run locally

```bash
git clone https://github.com/alvaroalcalaa/cohort-pulse.git
cd cohort-pulse
python -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000), then select **Load demo** or import a compatible CSV.

## License

Distributed under the [MIT License](LICENSE).
