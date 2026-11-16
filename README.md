# Finance Calculator · DeUna Hackathon

🇬🇧 **English** · 🇪🇨 [Español](README.es.md)

Hackathon prototype that adds a **finance calculator** to a **Deuna**-style mobile wallet, so small businesses and
users learn basic finance concepts while using their payments app:

- **Monthly loan payment** from the amount, interest rate and term.
- **Break-even point:** how much you need to sell to cover your costs.
- **Pricing:** how much to charge for a product to make a profit.

Each calculator explains the difference between the concepts so the user can make informed decisions.

> Educational project built for a hackathon. It is not affiliated with Deuna or Banco Pichincha; the interface only
> imitates the wallet to show how the feature would fit in. The interface is in Spanish.

## Technical details

| Layer | Technology |
|---|---|
| Backend | Django 5.1 + Django REST Framework |
| Database | SQLite (`Producto` model: name, price, quantity) |
| Frontend | Django templates with HTML, CSS and JavaScript |
| References | [Deuna SDKs](https://docs.deuna.com/docs/deuna-sdks), sandbox `https://api.sandbox.deuna.io` |

```
my_project/            Django configuration (settings, urls)
api/models.py          Producto model
api/views.py           page views
api/templates/         index (loan calculator), punto_equilibrio (break-even), precios (pricing), financial calculator
api/static/            styles
```

### Run locally

```bash
python -m venv venv
venv\Scripts\activate          # Windows (Linux/macOS: source venv/bin/activate)
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver     # http://127.0.0.1:8000
```

> By default it runs in development mode. Outside your own computer, set the environment variables
> `DJANGO_SECRET_KEY` (your own key) and `DJANGO_DEBUG=False`.

## License

[MIT](LICENSE).
