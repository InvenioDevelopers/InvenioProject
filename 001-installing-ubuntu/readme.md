## Установка Ubuntu 20.04 LTS паралельно з Windows 10

У цьому розділі Ви зможете дізнатися, як крок за кроком встановити операційну систему [Ubuntu](https://ubuntu.ru/) паралельно з операційною системою [Windows](https://www.microsoft.com/uk-ua/software-download/), так як це необхідно для подальшої роботи в програмному забезпеченні [Invenio](https://inveniosoftware.org/).

### Основними кроками в даному варіанті установки є:
- крок 1 - завантажити ІСО-образ Убунту
- крок 2 - створити завантажувальний флешку
- крок 3 - стиснути диск С і виділити місце під У
- крок 4 - запустити комп'ютер з завантажувальної флешки
- крок 5 - слідувати подальшим вказівкам установки Убунту 

### Якщо потрiбна детальна iнструкцiя, будь-ласка, скористайтеся наведеними нижче посиланнями:

Переходячи за цим посиланням, Ви можете отримати детальну iнструкцiю по покроковiй установці: [текстова iнструкцiя](https://info-comp.ru/install-ubuntu-next-to-windows-10)

Переходячи за цим посиланням, Ви можете дiзнатися як встановити Ubuntu за відео-інструкцією: [відео-інструкція](https://www.youtube.com/watch?v=8sJIGQzCjzQ&t=319s)


## Установка Ubuntu 20.04 на VirtualBox у Windows 10

VirtualBox підходить для особистих семінарів, Забезпечує узгоджене налаштування для всіх учасників та полегшує життя тренерам. Для того, щоб встановити Ubuntu 20.04 на VirtualBox, як ще одну операційну систему, можна скористатися [цією інструкцією](https://ithowto.ru/ustanovka-ubuntu-2004-virtualbox.html).

### VirtualBox (для майстер класів)

-  [Встановіть VirtualBox](https://www.virtualbox.org/wiki/Downloads) для своєї платформи
-  Завантажте файл OVA з https://inveniosoftware.web.cern.ch/inveniosoftware/download/virtualbox/Invenio%20Bootcamp%20Ubuntu%202019.ova (~ 3 ГБ)
-  Відкрийте програму VirtualBox і перейдіть до «Файл -> Імпортувати пристрій ...» та виберіть завантажений файл OVA з попереднього кроку. Натисніть "Далі", а потім "Імпорт"
- Після завантаження приладу він з’явиться у списку віртуальних машин як «Invenio Bootcamp Ubuntu»
- Двічі клацніть запис, щоб запустити віртуальну машину
- Ім'я користувача / пароль для користувача - bootcamp/bootcamp

### Локальне налаштування (для нових розробників)

Для налаштування локальної розробки переконайтеся, що у вас є:

- Сучасна IDE, яка підтримує Python, наприклад, VSCode, Sublime, Atom, PyCharm тощо.
- Git
- Python 3.6+
- [pip](https://pip.pypa.io/en/stable/) і [pipenv](https://pipenv.pypa.io/en/latest/) встановлений і повністю працює
- [cookiecutter](https://cookiecutter.readthedocs.io/en/latest/installation.html) для риштування
- NodeJS версії 14+ та NPM ( [див. Офіційну інсталяцію](https://nodejs.org/en/download/) )
- [Docker](https://docs.docker.com/get-docker/) і [Docker Compose](https://docs.docker.com/compose/install/)
- [Google Chrome](https://www.google.com/chrome/https://www.google.com/chrome/) і [ChromeDriver](http://chromedriver.chromium.org/getting-started) для тестів E2E
- Якщо ви працюєте під Linux / MacOS, вам доведеться підняти ваш, vm.max_map_countяк описано в [документах Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/current/vm-max-map-count.html)
Якщо ви використовуєте Ubunut / Debian, ви можете запустити, sudo bootstrap.sh $(whoami)щоб встановити деякі з вищезазначених. Не соромтеся заглядати всередину bootstrap.shсценарію, щоб зрозуміти / відрегулювати встановлене / змінене.
