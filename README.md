# EconoGrow - Dashboard Financiero

Dashboard web moderno y responsivo para visualizar y analizar gastos personales o familiares, con integración dinámica a un webhook de Google Sheets.

## Características principales

- **Visualización de Gastos del Mes**: Pie chart interactivo con leyenda y colores únicos por categoría.
- **Análisis Kakebo (Necesidades vs Deseos)**: Gráfico de torta con colores altamente contrastantes y leyenda dedicada.
- **Control Semanal (Últimos 7 Días)**: Pie chart semanal, solo gastos, colores diferenciados y leyenda.
- **Tabla de Detalle**: Gastos/ingresos con formato amigable, color por tipo, y columnas adaptadas a móvil.
- **Estadísticas**: Tarjetas con total gastado, presupuesto mensual, semanal y promedio diario, todos formateados con separador de miles.
- **Responsive**: UI adaptable a dispositivos móviles y escritorio.
- **Logo personalizado**: PNG centrado y scrollable.
- **Sin datos mock**: Solo muestra datos reales del backend.

## Instalación y uso

1. **Clona el repositorio:**
   ```sh
   git clone https://github.com/tu-usuario/finanzas_app.git
   cd finanzas_app
   ```
2. **Estructura:**
   - `index.html` — Todo el código HTML, CSS y JS embebido (sin dependencias externas salvo Google Fonts).
   - `logo.png` — Logo de la app (coloca tu logo aquí).
   - `README.md` — Este archivo.

3. **Personalización:**
   - Cambia el logo por el tuyo en `logo.png`.
   - Ajusta la URL del webhook si tu endpoint cambia.

4. **Despliegue:**
   - Sube todos los archivos a GitHub.
   - Puedes publicar el dashboard en GitHub Pages, Netlify, Vercel, etc. Solo necesitas servir `index.html` y `logo.png`.

## Requisitos
- Navegador moderno (Chrome, Firefox, Edge, Safari).
- Acceso a Internet para consumir el webhook y Google Fonts.

## Estructura de archivos
```
finanzas_app/
├── index.html
├── logo.png
└── README.md
```

## Webhook esperado
- El dashboard espera un endpoint tipo:
  `https://n8n.iaexperience.com.ar/webhook/get-gastos?sheetName=mes_año`
- El JSON debe incluir los campos:
  - `gasto_mensual`, `presupuesto_mensual`, `presupuesto_semanal` (en el primer elemento)
  - `fecha`, `categoria_principal`, `categoria_kakebo`, `descripcion`, `notas`, `monto`, `tipo`

## Licencia
MIT

---
¡Contribuciones y sugerencias son bienvenidas!
