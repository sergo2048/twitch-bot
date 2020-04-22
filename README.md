# twitch-bot #

## Описание ##

Основная идея заключается в том, чтобы бот мог отслеживать количество времени проведенного зрителями в чате.  
Так же если написать в чат команду **!time** бот должен вывести топ-5 зрителей по времени в чате.  
~~В перспективе, добавить команду **!time+nickname**, которая будет выводит в чат время определенного зрителя.~~

## Зависимости ##

В этом проекте используется *Python* ***версии 3.7***. Это обусловлено тем, что я использую модуль *asyncio*, в котором есть функции которых не было в предыдущих версиях Python например *asyncio.run*  
  
Я так же использую **aiohttp**, это не стандартный модуль и его нужно дополнительно установить.

```python
pip3 install aiohttp
```

Так же я использую стандартные модули time, re, json.

## Настройка ##

После установки вышеперечисленных зависимостей, для корректной работы необходимо создать файл **config.py**, который должен содержать примерно следующие:

```python
HOST = 'irc.twitch.tv'  # host name
MESSAGE_INTERFACE = 'tmi.twitch.tv' # message host name
PORT = 6667  # number of port
NICK = ''  # bot nickname
PASSWORD = ''  # chat token
CHANNEL = ''  # the name of the channel on which the bot will work 
RATE = (20/30)
```

Если вы установили все необходимое и создали в папке проекта config файл, то все должно работать. Запустите бота что бы проверить это. Что бы запустить бота необходимо запустить *main.py*.

```python
python3 main.py
```

## База данных ##

Пока это не доступно, но если я еще вернусь к этому проекту, это будет следующие, что я попробую реализовать.  
Сейчас бот считает время проведенное в чате просто так, хранит его в оперативной памяти и никуда не сохраняет. Я считаю это не правильно, но подключение БД дело не из простых.
