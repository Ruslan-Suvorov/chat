Создание чата на NodeJS

В папке client вёрстка и клиетская часть, т.е. :
1 - в файле unauth.js описана работа с формой в случае, если Вы не авторизованы. Вы можете войти или зарегистрироваться (описан метод POST для передачи на бекенд)
2 - в файле auth.js описана работа в самом чате, в случае если Вы авторизованы. Вы можете написать сообщение в чат и отправить его либо выйти из авторизации (описан метод POST для передачи на бекенд и вставка клоков с сообщением)

В папке server собственно серверная часть:
1 - в файле server.js сам сервер, который мы будем запускать в нём инициализированы все подключаемые библиотеки, прописан запуск сервера, подключение к базе данных(MongoDB)
2 - в файле router.js прописана регистрация, аутентификация и выход из аутентификации
3 - в файле sockets.js прописана проверка аутентификации, отправка сообщения и отправка истории сообщений, если пользователь пропустил
4 - в файде config.js прописана проверка токена из куки для авторизации
5 - в файле users.model.js прописана структура внесения пользователеё в базу даных, а так же шифрование пароля
6 - в файле messages.model.js прописана структура внесения сообщений в базу даных
