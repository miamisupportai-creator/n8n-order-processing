# Setup: E-commerce Order Automation

## Requisitos
- n8n Cloud activo (plan Starter o superior)
- Zoho CRM API key / OAuth token configurado en n8n
- Claude API key (Anthropic) configurada en n8n

## Variables a reemplazar
| Variable | Descripcion |
|----------|-------------|
| `${CLIENT_ID}` | ID único del cliente (ej: acme-corp) |
| `${CLIENT_NAME}` | Nombre del negocio (ej: ACME Corp) |
| `${ZOHO_OAUTH_TOKEN}` | Token OAuth de Zoho CRM |
| `${NTFY_TOPIC}` | Topic de ntfy.sh para alertas (ej: acme-orders) |

## Activacion
1. Importar `workflow.json` en n8n: **Settings → Import Workflow**
2. Buscar y reemplazar todas las variables de la tabla anterior
3. Configurar credenciales en cada nodo que las requiera
4. Activar el workflow desde el toggle superior derecho
5. Probar con un payload de prueba usando **Test Workflow**

## Prueba rapida
```bash
curl -X POST https://TU-N8N.app.n8n.cloud/webhook/YOUR-PATH \
  -H "Content-Type: application/json" \
  -d '{"test": true}'
```

## Soporte
- Documentacion n8n: https://docs.n8n.io
- ai50m: https://ai50m.com
