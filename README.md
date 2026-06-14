# Crediapp
App crédito 
# 💳 CréditoApp — Guía de Campo v1.0

## ¿Qué hay en este paquete?

```
📁 CréditoApp/
│
├── microcreditos-pwa.html   ← LA APP  (ábrela en Chrome)
│
├── 📁 servidor-ia/          ← Solo si quieres el Soporte IA
│   ├── server.js
│   ├── package.json
│   ├── test-api.js
│   └── .env.example
│
└── LEEME.md                 ← Este archivo
```

---

## INICIO RÁPIDO — 3 pasos

### Paso 1 — Instalar la app en tu celular

**Android:**
1. Copia `microcreditos-pwa.html` a tu celular (WhatsApp, USB, Drive)
2. Ábrela con **Chrome**
3. Menú (⋮) → **"Agregar a pantalla de inicio"**
4. Confirma → ya tienes el ícono en tu pantalla

**iPhone:**
1. Copia el archivo y ábrelo en **Safari**
2. Botón compartir (□↑) → **"Añadir a inicio"**
3. Confirma

---

### Paso 2 — Configurar tu negocio

1. Abre la app → **Configuración** (⚙️)
2. Cambia el **nombre** de tu negocio
3. Sube tu **logo** (PNG o JPG)
4. Configura la **tasa por defecto**
5. Activa un **PIN de seguridad** (recomendado)

---

### Paso 3 — Limpiar datos de demo

Los datos de ejemplo que ves son solo para mostrar cómo funciona.

Para borrarlos: **Soporte IA → escribe** "borra todos los datos demo"

O manualmente: borra cada crédito/cliente desde las tablas.

---

## USO DIARIO

### Registrar un crédito nuevo
1. Click en **"+ Nuevo Crédito"** (arriba a la derecha)
2. Selecciona el cliente (créalo primero si no existe)
3. Ingresa monto, tasa % y número de cuotas
4. Elige la frecuencia: Diario / Semanal / Quincenal
5. Verifica el preview automático → **Registrar**

### Fórmula que usa la app
```
Interés     = Monto × Tasa%
Total       = Monto + Interés
Cuota       = Total ÷ Número de cuotas

Ejemplo:
  Monto:   $500.000
  Tasa:    20%
  Cuotas:  30 diarias

  Interés  = $500.000 × 20% = $100.000
  Total    = $600.000
  Cuota    = $600.000 ÷ 30 = $20.000/día
```

### Registrar un abono
1. Ve a **Créditos** o **Dashboard**
2. Click en 💰 del crédito
3. Confirma el monto (se precarga la cuota automáticamente)
4. Elige método de pago
5. Se genera el recibo → puedes compartirlo por WhatsApp

### Semáforo de mora
| Color | Significado | Acción |
|-------|-------------|--------|
| 🟢 Verde | Al día | Ninguna |
| 🟡 Amarillo | 1-3 días sin pagar | Recordatorio |
| 🟠 Naranja | Mora activa | Llamada |
| 🔴 Rojo | Mora crítica | Visita |

---

## BACKUP — MUY IMPORTANTE

**Haz backup cada semana** o antes de cambiar de celular.

1. **Configuración** → **Backup de Datos**
2. Click **"Exportar backup completo"**
3. Guarda el archivo `.json` en Drive o WhatsApp

Para restaurar: mismo menú → **"Restaurar desde backup"** → selecciona el archivo.

⚠️ Los datos viven en el navegador. Si borras la caché o cambias de celular sin backup, **se pierden**.

---

## INFORMES

Ve a **Informes** → elige el período:
- **1 Mes** — vista del mes en curso
- **3 Meses** — visión trimestral
- **6 Meses** — tendencia semestral
- **Todo** — histórico completo

**Exportar PDF:** Click "Exportar PDF" → el navegador abre el diálogo de impresión → "Guardar como PDF"

**Exportar CSV:** Click "CSV" → abre en Excel directamente

---

## SOPORTE IA (Opcional)

Requiere instalar el servidor proxy en un PC con internet.

**Instalación:**
```powershell
# En tu PC con Node.js instalado
mkdir servidor-ia
cd servidor-ia
# Copia los archivos server.js, package.json, test-api.js, .env.example

# Renombrar y configurar
copy .env.example .env
# Edita .env y pega tu API Key de console.anthropic.com

npm install
npm start
```

**Conectar la app:**
1. **Configuración** → **Conexión Soporte IA**
2. URL: `http://localhost:3001`
3. Click **"Verificar conexión"**
4. Badge verde = activo ✅

---

## PROBLEMAS COMUNES

| Problema | Solución |
|----------|----------|
| "No se ven los cambios" | Cierra y reabre el archivo en Chrome |
| "Se perdieron los datos" | Restaura desde tu backup .json |
| "El PIN no funciona" | Desactívalo desde Configuración → Quitar PIN |
| "La app no instala en iPhone" | Usa Safari, no Chrome |
| "El Soporte IA no conecta" | Verifica que `npm start` está corriendo |

---

## PRÓXIMAS FUNCIONES (siguiente versión)

- [ ] Gestión de cobradores con acceso limitado
- [ ] Refinanciación de créditos
- [ ] Notificaciones de mora automáticas
- [ ] Backend con base de datos real (PostgreSQL)
- [ ] Acceso multiusuario desde cualquier dispositivo
- [ ] App en tienda (Android/iOS)

---

**Versión:** 1.0.0  
**Fecha:** Junio 2025  
**Soporte:** Reporta bugs y mejoras en el chat de desarrollo
