# Calcu de Finanzas · DeUna Hackathon

Prototipo de hackatón que agrega una **calculadora de finanzas** a una billetera móvil estilo **Deuna**, para que
pequeños negocios y usuarios aprendan conceptos financieros básicos mientras usan su app de pagos:

- **Pago mensual de un préstamo** a partir del monto, la tasa de interés y el plazo.
- **Punto de equilibrio:** cuánto hay que vender para cubrir los costos.
- **Fijación de precios:** cuánto cobrar por un producto para obtener ganancia.

Cada calculadora explica la diferencia entre los conceptos para que el usuario tome decisiones informadas.

> Proyecto educativo hecho para una hackatón. No está afiliado a Deuna ni a Banco Pichincha; la interfaz solo
> imita la billetera para mostrar cómo encajaría la función.

## Detalles técnicos

| Capa | Tecnología |
|---|---|
| Backend | Django 5.1 + Django REST Framework |
| Base de datos | SQLite (modelo `Producto`: nombre, precio, cantidad) |
| Frontend | Plantillas Django con HTML, CSS y JavaScript |
| Referencias | [Deuna SDKs](https://docs.deuna.com/docs/deuna-sdks), sandbox `https://api.sandbox.deuna.io` |

```
my_project/            configuración de Django (settings, urls)
api/models.py          modelo Producto
api/views.py           vistas de las páginas
api/templates/         index (calculadora de préstamos), punto_equilibrio, precios, financial calculator
api/static/            estilos
```

### Ejecutar localmente

```bash
python -m venv venv
venv\Scripts\activate          # Windows (Linux/macOS: source venv/bin/activate)
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver     # http://127.0.0.1:8000
```

> Por defecto corre en modo desarrollo. Fuera de tu computador define las variables de entorno
> `DJANGO_SECRET_KEY` (una clave propia) y `DJANGO_DEBUG=False`.

## In English

Hackathon prototype that adds a finance calculator (loan payment, break-even point, pricing) to a Deuna-style mobile
wallet so small businesses can learn basic finance concepts. Django 5.1 + DRF with SQLite. Not affiliated with Deuna.

## Licencia

[MIT](LICENSE).
