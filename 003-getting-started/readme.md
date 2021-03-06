## Початок роботи з Invenio

### Крок перший:

Перед початком подальшої роботи, перевірте, будь-ласка, чи встановлено у Вас необхідне програмне забезпечення. Перелік передумов наведено у розділі [передумови](002-prerequisites/)

### Крок другий:

Відкрийте термінал та перевірте тренувальний вихудний код. Для цого застуйте наступні команди:

```bash
$ cd ~/src
$ git clone https://github.com/inveniosoftware/training.git
```

### Крок третій:

Побудуйте основу для першого екземпляра Invenio:

```bash
$ cookiecutter gh:inveniosoftware/cookiecutter-invenio-instance -c v3.4 --no-input
```

### Крок четвертий:
Перейдіть до створеного коду та запустіть служби Docker (база даних, Elasticsearch, RabbitMQ та кеш Redis). Для цього 
потрібно заствосувати команди:

```bash
$ cd my-site
$ docker-compose up -d
```

Встановіть та побудуйте Python та NPM зв'язки наступним чином:

```bash
$ ./scripts/bootstrap
```

### Крок п'ятий:

Налаштуйте таблиці бази даних, індекси пошуку, черги та кеші наступним чином:

```bash
$ ./scripts/setup
```

Запустіть сервер розробки та фонового працівника такою командою:

```bash
$ ./scripts/server
```
Далі відкрийте [https://127.0.0.1:5000/](https://127.0.0.1:5000/) у своєму браузері:

```bash
$ firefox https://127.0.0.1:5000/
```

Firefox та інші браузери відображатимуть попередження про безпеку, оскільки ми намагаємось
відкрити безпечне з'єднання з сервером із самопідписаним сертифікатом:

![Попередження](Попередження.png)

Просто пропустіть це попередження, натиснувши "Додатково" та підтвердьте сертифікат
як виняток. Ви побачите свій перший примірник:

![FirstPage](FirstPage.png)
