# Поднять сервис на Docker, используя FastAPI, который будет отправлять письма клиентам.

## Требования:

### Написать Dockerfile для сервиса mailer, который будет базироваться на образе Python 3.11.
Использовать FastAPI для создания HTTP-сервера.
Реализовать эндпоинт /send_email, который будет принимать POST-запросы с JSON-телом следующей структуры:

{
  "to": "recipient@example.com",
  "subject": "Test email",
  "message": "This is a test email."
}

### Данные электронной почты должны быть валидными (то есть корректный формат электронной почты должен быть обеспечен).
При получении запроса на /send_email, сервис должен отправлять письмо с использованием SMTP-сервера (например, Gmail или другого провайдера).
Добавить логирование действий сервиса в stdout или файл.
Написать тесты, которые проверяют работу сервиса с использованием фреймворка pytest. В тестах следует проверить корректность отправки писем, а также обработку ошибок.
Рекомендации:

### Разбейте код на модули/классы/функции в соответствии с лучшими практиками разработки.
Обратите внимание на обработку ошибок и обратную связь с клиентом в случае возникновения проблем.
Используйте документацию FastAPI и других библиотек, если необходимо.
Внимательно проверьте настройки безопасности, особенно при работе с SMTP-сервером.
Удачи в выполнении задания! Если у вас возникнут вопросы, не стесняйтесь задавать.

## Сборка образа в корне проекта

docker build -t myimage . 

## Запуск образа в корне проекта

docker run -d --name mycontainer -p 80:80 myimage

### гитигнор и запуск в другую ветку
### прихерачить пост запросы / отрегулировать в постмане
### прихерачить тесты а после все смержить
