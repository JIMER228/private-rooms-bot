# private-rooms-bot
<img src='assest/img/Discord_VMraGB9rwp.png'>
<img src='assest/img/Code_hO1PlcTboF.png'>

# Как настроить бота?
Заходим в `config.py`, и задаём значения переменных:
```python
token = 'your_token_here'
guild_id = 0  # ID Сервера

category_id = 0 # ID Категории в котором находятся private_control_id и create_private_chan_id
private_control_id = 0 # ID канала для создания панели управления
create_private_chan_id = 0 # ID Voice канала в дискорде
message_id = 0 # ЧИТАЙТЕ ПОДРОБНЕЕ В FAQ!

# Все эти эмодзи есть в /assest/psd/PrivateRoomIcon.psd
emoji1 = '<:vip:1180438222082420818>' # передать владельца
emoji2 = '<:limitededition:1180444076697452544>' # изменить лимит
emoji3 = '<:lock:1180430104334172220>' # закрыть доступ
emoji4 = '<:unlock:1180430126933082143>' # открыть доступ
emoji5 = '<:microphone:1180433814888120410>' # размутить
emoji6 = '<:microphoneoff:1180433831757627393>' # замутить
emoji7 = '<:view:1180435453699182622>' # скрыть/открыть комнату
emoji8 = '<:signal:1180438867149590578>' # закрыть/открыть доступ
emoji9 = '<:pencil:1180434371723919420>' # изменить название
emoji10 = '<:door:1180441202135408650>' # выгнать участника
```

# Подробнее про `message_id`:
`message_id` используется для изменения прошлого сообщения, дабы не спамить водном и том же канале. Возникает вопрос, как его настроить? В `config.py` мы должны задать значения всем переменным кроме `message_id` (так и оставляем `0`), запускаете бота и проверяете что всё работает, выключаете бота и копируете ID сообщения, только потом задаём значение для `message_id`.

# Автоматическая установка бота на сервер
Переходим в деррикторию бота и пишем команду `chmod +x setup.sh`, и запускаем `./setup.sh`. Бот будет включатся автоматически даже после перезагрузки самого сервера (VDS/VPS).

Как включить/перезагрузить/остановить бота?
> Бот работает под сервисом 'privateroomsbot'

Для включения бота напишите:
```sh
sudo systemctl start privateroomsbot.service
```
Для перезапуска бота напишите:
```sh
sudo systemctl restart privateroomsbot.service
```
Для выключения бота напишите:
```sh
sudo systemctl stop privateroomsbot.service
```

Script by <a href='https://github.com/reques6e' style='display: block; text-align: center;'>Requeste Project<img src='https://github.com/reques6e/reques6e/blob/main/assets/images.png?v=1' alt='Мой баннер' width='20' height='20' style='float: right;'></a>
