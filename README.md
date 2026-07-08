# Radar pisos 28022 web

Web estatica publica del radar de pisos.

Esta carpeta esta pensada para publicarse con GitHub Pages. Contiene solo la version saneada del dashboard:

- sin telefonos;
- sin nombres de contacto;
- sin notas internas;
- sin mensajes personales;
- sin comandos locales.

Para actualizarla desde el proyecto principal:

```powershell
python .\manage.py publish-web --public-safe
Copy-Item -Force .\public\index.html .\deploy\github-pages\public\index.html
```

Despues, dentro de `deploy\github-pages`:

```powershell
git add .
git commit -m "Update dashboard"
git push
```
