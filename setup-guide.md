# Guia de Setup — Order Processing Automatizado

## Descripcion
Automatizacion del ciclo de ordenes: recepcion via webhook, validacion, procesamiento de pago con Stripe, y confirmacion por email.

## Pasos
1. Importar `workflow.json` en n8n
2. Configurar credencial de Stripe (Secret Key)
3. Configurar credencial de Email
4. Reemplazar `${CLIENT_ID}` con el Stripe Secret Key del cliente
5. Conectar tu e-commerce para enviar ordenes al webhook
6. Activar el workflow

## Variables Configuradas
| Variable | Valor |
|----------|-------|
| CLIENT_ID | ${CLIENT_ID} |
| CLIENT_NAME | ${CLIENT_NAME} |
| CLIENT_EMAIL | ${CLIENT_EMAIL} |
| CLIENT_PHONE | ${CLIENT_PHONE} |

## Webhook URL
`https://ai50m.app.n8n.cloud/webhook/order-${CLIENT_ID}`

## Payload Esperado
```json
{
  "order_id": "ORD-001",
  "customer_email": "cliente@email.com",
  "customer_name": "Nombre",
  "items": [{ "name": "Producto", "qty": 1, "price": 99.99 }],
  "total": 99.99
}
```

## Soporte
contact@ai50m.com | ai50m.com
