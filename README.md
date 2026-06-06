# Super Agente IA Stripe - Expedientetalle

🚀 **Sistema integral de procesamiento de pagos con Stripe integrado con Zapier MCP Server**

## 📋 Características Principales

✅ **Gestión de Clientes**
- Crear, actualizar y listar clientes
- Almacenar información de pago de forma segura
- Metadatos personalizados

✅ **Procesamiento de Pagos**
- Crear Payment Intents
- Autorización y captura de fondos
- Soporte para 3D Secure
- Idempotencia para evitar duplicados

✅ **Suscripciones**
- Crear y gestionar suscripciones recurrentes
- Cancelaciones y cambios de plan
- Renovaciones automáticas

✅ **Facturación**
- Generar facturas automáticas
- Envío por email
- Seguimiento de estado

✅ **Reembolsos**
- Reembolsos totales y parciales
- Procesamiento automático
- Historial completo

✅ **Webhooks**
- Validación de firmas Stripe
- Eventos en tiempo real
- Integración con Zapier

✅ **Seguridad**
- Bearer Token authentication
- Encryción de datos sensibles
- Audit logs
- Rate limiting

---

## 🛠️ Instalación Rápida

```bash
# 1. Instalar dependencias
npm install

# 2. Configurar variables de entorno
cp .env.example .env
# Editar .env con tus credenciales de Stripe

# 3. Iniciar servidor
npm start
```

El servidor estará en: `http://localhost:3000`

---

## 🚀 Endpoints Principales

### 👥 Clientes
```bash
POST   /api/v1/customers              # Crear cliente
GET    /api/v1/customers              # Listar clientes
GET    /api/v1/customers/:id          # Obtener cliente
PUT    /api/v1/customers/:id          # Actualizar cliente
```

### 💳 Pagos
```bash
POST   /api/v1/payments/create-intent # Crear Payment Intent
POST   /api/v1/payments/confirm-intent # Confirmar pago
POST   /api/v1/payments/charge        # Procesar pago directo
```

### 🔄 Suscripciones
```bash
POST   /api/v1/subscriptions          # Crear suscripción
GET    /api/v1/subscriptions/customer/:id # Listar suscripciones
DELETE /api/v1/subscriptions/:id      # Cancelar suscripción
```

### 📄 Facturas
```bash
POST   /api/v1/invoices               # Crear factura
GET    /api/v1/invoices/:id           # Obtener factura
GET    /api/v1/invoices/customer/:id  # Listar facturas
POST   /api/v1/invoices/:id/send      # Enviar por email
```

### 💰 Reembolsos
```bash
POST   /api/v1/refunds                # Crear reembolso
GET    /api/v1/refunds/:id            # Obtener reembolso
GET    /api/v1/refunds/charge/:id     # Listar reembolsos
```

### 🔔 Webhooks
```bash
POST   /api/v1/webhooks/stripe        # Webhooks de Stripe
```

---

## 📊 Health Check

```bash
curl http://localhost:3000/health
```

**Respuesta:**
```json
{
  "status": "ok",
  "service": "Expedientetalle Stripe Agent",
  "version": "1.0.0",
  "timestamp": "2026-06-06T12:00:00.000Z"
}
```

---

## 🔐 Seguridad

✅ Validación de Webhooks con HMAC-SHA256
✅ Idempotencia en pagos (evita duplicados)
✅ Rate Limiting (100 req/min)
✅ Encryption AES-256
✅ Audit Logs completos
✅ PCI DSS compliance

---

## 🐳 Docker

```bash
# Build imagen
npm run docker:build

# Ejecutar contenedor
npm run docker:run
```

---

## 🧪 Tests

```bash
npm test
npm test:watch
npm test -- --coverage
```

---

## 📝 Documentación

Ver guía completa en: [SETUP.md](./docs/SETUP.md)

---

## 🆘 Soporte

Reportar issues: https://github.com/expedientesxero-source/Expedientetalle-/issues

---

**Desarrollado con ❤️ por Expedientes Xero Source**
