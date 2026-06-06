# Super Agente IA Stripe - Expedientetalle

🚀 **Sistema integral de procesamiento de pagos con Stripe integrado con Zapier MCP Server**

## 📋 Características Principales

✅ **Gestión de Clientes** - Crear, actualizar y listar clientes
✅ **Procesamiento de Pagos** - Payment Intents, autorización, captura y 3D Secure
✅ **Suscripciones** - Crear, gestionar y cancelar suscripciones recurrentes
✅ **Facturación** - Generar, enviar y seguimiento de facturas
✅ **Reembolsos** - Reembolsos totales y parciales con historial
✅ **Webhooks** - Validación de firmas Stripe en tiempo real
✅ **Seguridad** - Bearer Token, Encryption, Audit logs, Rate limiting

---

## 🛠️ Instalación Rápida

```bash
npm install
cp .env.example .env
# Configurar STRIPE_API_KEY y STRIPE_WEBHOOK_SECRET
npm start
```

---

## 🚀 Endpoints Principales

- **Clientes**: `POST/GET/PUT /api/v1/customers`
- **Pagos**: `POST /api/v1/payments/create-intent|confirm-intent|charge`
- **Suscripciones**: `POST/GET/DELETE /api/v1/subscriptions`
- **Facturas**: `POST/GET /api/v1/invoices`
- **Reembolsos**: `POST/GET /api/v1/refunds`
- **Webhooks**: `POST /api/v1/webhooks/stripe`

---

## 📊 Health Check

```bash
curl http://localhost:3000/health
```

---

## 🐳 Docker

```bash
npm run docker:build
npm run docker:run
```

---

## 🧪 Tests

```bash
npm test
```

---

**Desarrollado con ❤️ por Expedientes Xero Source**
