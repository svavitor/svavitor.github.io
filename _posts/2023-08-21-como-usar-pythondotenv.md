---
title: Como usar python-dotenv
date: 2023-08-21 18:40:00 +0800
categories: [Blogging]
tags: [python, dotenv]
pin: true
math: true
mermaid: true
---

Pequeno tutorial de como instalar e usar python-dotenv


## Usando



Crie seu arquivo .env preencha suas variáveis.

```python
# Exemplo .env

SECRET_KEY = "1234ABC"
DEBUG = "True"
```

Faça o import no arquivo que você precisará usar as variáveis.

```python
# Exemplo settings.py
import os

from dotenv import load_dotenv
load_dotenv() # Esse metodo carrega as variáveis no os.

# Para ter acesso as variáveis use o os

SECRET_KEY = os.getenv("SECRET_KEY")
DEBUG = (os.getenv("DEBUG") == "True")
```
