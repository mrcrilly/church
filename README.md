# Church
[![Build Status](https://travis-ci.org/lk-geimfari/church.svg?branch=master)](https://travis-ci.org/lk-geimfari/church)
[![PyPI version](https://badge.fury.io/py/church%2F.svg)](https://badge.fury.io/py/church%2F)
[![HitCount](https://hitt.herokuapp.com/lk-geimfar/church.svg)](https://github.com/lk-geimfari/church)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/d773f20efa67430683bb24fff5af9db8)](https://www.codacy.com/app/likid-geimfari/church?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=lk-geimfari/church&amp;utm_campaign=Badge_Grade)
[![Issues](https://img.shields.io/github/issues/lk-geimfari/church.svg)](https://github.com/lk-geimfari/church/issues)


![alt text](https://raw.githubusercontent.com/lk-geimfari/church/master/examples/church.png)

Church - is a library to generate fake data. It's very useful if you need to bootstrap your database.

## Installation
```zsh
➜  ~  pip install church

```

## Usage
```python
#  It's very useful if you need bootstrap your database.
# ...
# ... 

@staticmethod
def _church(c=100):
    from church import Personal

    ch = Personal('en_us')
    for i in range(c):
        user = User(username=ch.username(),
                    email=ch.email(),
                    name=ch.name('m'),
                    surname=ch.surname('m'),
                    credit_card=ch.credit_card_number(),
                    home_page=ch.home_page(),
                    password=ch.password(length=10),
                    gender=ch.gender(abbreviated=True),
                    profession=ch.profession(),
                    nationality=ch.nationality()
                    )
        try:
            db.session.add(user)
        except Exception:
            db.session.commit()

# ...
# ...

```

## Contributing
Your contributions are always welcome! Please take a look at the [contribution](https://github.com/lk-geimfari/church/blob/master/CONTRIBUTING.md) guidelines first.

## Runtime
[![PyPI](https://img.shields.io/pypi/pyversions/caravel.svg?maxAge=2592000)](https://pypi.python.org/pypi/church/)


## Licence 
[![MIT Licence](https://badges.frapsoft.com/os/mit/mit.svg?v=103)](https://github.com/lk-geimfari/church/blob/master/LICENSE)   


## Why church?
«Such teachings come through hypocritical liars, whose consciences have been seared as with a hot iron.» Timothy 1:4
