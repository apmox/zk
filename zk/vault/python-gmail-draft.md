# Plugin Gmail Draft per aditre

- Virtualenv in cartella aditre con
https://realpython.com/python-virtual-environments-a-primer/
``` dos
> pip install virtualenv
> cd dev
> virtualenv env
> \env\scripts\activate
(env) > _
```
- Attivo Gmail API:
https://developers.google.com/gmail/api/quickstart/python
Clicco enable e scarico `credentials.json`

- Installo pacchi per gmail api:
```
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib
```

- Creo file `quickstart.py`:
https://developers.google.com/gmail/api/quickstart/python

- Eseguo Quickstart:
```
> python quickstart.py
```

- Apro URL in account Aditre e autorizzo applicazione

- Lo script `send_mail.py` è in python 2 va corretto per python 3
