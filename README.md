# DockerBasics

<h1> <i> Частина I. Вступ </i> </h1>

<h2> <b> 1.	Запуск контейнера Docker за допомогою Docker Desktop. </b> </h2>

1.1.	Відкриємо термінал командного рядка та запускаємо перший контейнер, виконавши `docker run` команду. [(Скріншот)](Screenshots/1.1.png) <br></br>
1.2.	Відвідуємо веб-сайт <a> http://localhost:8080 </a>. [(Скріншот)](Screenshots/1.2.png) <br></br>
1.3.	Відкриємо Docker Desktop і виберемо поле `Containers` на лівій бічній панелі. [(Скріншот)](Screenshots/1.3.png) <br></br>
1.4.	В вкладці `Exec` можемо отримати доступ до оболонки. [(Скріншот)](Screenshots/1.4.png) <br></br>
1.5.	Для детальної інформації про контейнер, виберемо поле `Inspect`. [(Скріншот)](Screenshots/1.5.png) <br></br>

<h2> <b> 2. Розробка контейнерів </b> </h2>

2.1.	В терміналі клонуємо проект `getting-started-todo-app` на локальну машину. [(Скріншот)](Screenshots/2.1.png) <br></br>
2.2.	Переходимо до нового каталогу, створеного клоном. [(Скріншот)](Screenshots/2.2.png) <br></br>
2.3.	Запускаємо проект за допомогою команди `docker compose watch`. [(Скріншот)](Screenshots/2.3.png) <br></br>
2.4.	В браузері відкриваємо веб-сайт <a> http://localhost </a>. [(Скріншот)](Screenshots/2.4.а.png) <br></br>
ㅤㅤВ цій програмі ми можемо: <br></br>
ㅤ•  Додавати та видаляти елементи. [(Скріншот створення двох елементів](Screenshots/2.4.б.png) [та видалення одного з них)](Screenshots/2.4.в.png) <br></br>
ㅤ•  Визначати елемент як виконаний. [(Скріншот)](Screenshots/2.4.в.png) <br></br>
2.5.	В `backend/src/routes` знаходимо файл `getGreeting.js` та відкриваємо його. [(Скріншот)](Screenshots/2.5.png) <br></br>
2.6.	Змінюємо константу, що містить привітання `GREETING` (перший рядок файла). Замість значення `Hello world!`, додамо масив привітань. [(Скріншот)](Screenshots/2.6.png) <br></br>
2.7.	Щоб надіслати випадкове привітання з цього списку, зробимо зміни в `res.send` (9 рядок коду). [(Скріншот)](Screenshots/2.7.png) <br></br>
2.8.	Щоб побачити всі привітання, потрібно постійно оновлювати сторінку. З кожним оновленням буде з’являтися нове привітання. [(Скріншот)](Screenshots/2.8.png) <br></br>
2.9.	В `client/src/components` знаходимо файл `AddNewItemForm.jsx` та відкриваємо його. [(Скріншот)](Screenshots/2.9.png) <br></br>
2.10.	Змінюємо значення текстової підказки поля введення інформації `placeholder` (37 рядок коду) на `What do you need to do?`. [(Скріншот)](Screenshots/2.10.png) <br></br>
2.11.	Оновлюємо веб-сторінку щоб побачити цю зміну. [(Скріншот)](Screenshots/2.11.png) <br></br>
2.12.	В `client/src` знаходимо файл `index.scss` та відкриваємо його. [(Скріншот)](Screenshots/2.12.png) <br></br>
2.13.	Змінюємо фон сайту `background-color` (4 рядок коду) на синій. [(Скріншот)](Screenshots/2.13.png) <br></br>
2.14.	Знову оновлюємо веб-сторінку, тепер фон сайту має синій колір. [(Скріншот)](Screenshots/2.14.png) <br></br>

<h2> <b> 3.	Створення і просування першого образу </b> </h2>

3.1.	Переходимо до Docker Hub (<a>https://hub.docker.com/</a>). [(Скріншот)](Screenshots/3.1.png) <br></br>
3.2.	Переходимо до вкладки `Repositories` та обираємо `Create repository`. [(Скріншот)](Screenshots/3.2.png) <br></br>
3.3.	Даємо назву репозиторію, короткий опис та обираємо в `Visibility` загальнодоступну видимість `Public`. [(Скріншот)](Screenshots/3.3.png) <br></br>
3.4.	Натискаємо на `Create`, після чого репозиторій буде створено. [(Скріншот)](Screenshots/3.4.png) <br></br>
3.5.	В терміналі командного рядка створюємо проект, застосувавши команду, `docker build -t`, вказавши ім’я користувача та назву проекту. [(Скріншот)](Screenshots/3.5.png) <br></br>
3.6.	Скористаємося командою `docker image ls` для перевірки наявності Docker image. [(Скріншот)](Screenshots/3.6.png) <br></br>
3.7.	Надсилаємо image до Docker Hub, використовуючи команду `docker push`. [(Скріншот)](Screenshots/3.7.png) <br></br>

<h1> <i> Частина II. Основні концепції контейнерів, images, реєстрів і Docker Compose. </i> </h1>

<h2> <b> 4.	Запуск контейнеру Docker за допомогою графічного інтерфейсу Docker Desktop </b> </h2>

4.1.	Відкриємо Docker Desktop і в поле пошуку на верхній панелі навігації вказуємо welcome-to-docker, а потім виберемо кнопку Pull. (Скріншот)
4.2.	Після того, як отримали Docker image, натискаємо на кнопку Run. При натисканні, ми потрапляємо до вікна додаткових параметрів. (Скріншот)
4.3.	Розгортаємо Optional settings та вказуємо ім’я контейнеру welcome-to-docker та 8080 у якості хосту. (Скріншот)
4.4.	Тепер ми можемо натиснути на Run для запуску контейнера. (Скріншот)
4.5.	На інформаційній панелі Docker, перейшовши до вкладки Containers, можемо переглянути всі контейнери. (Скріншот)
4.6.	Відкриємо веб-сайт, перейшовши за посиланням в стовпці Port(s) чи відвідавши http://localhost:8080. (Скріншот)
4.7.	В Docker Desktop натискаємо на контейнер. Після цього обираємо вкладку Files, щоб дослідити ізольовану файлову систему контейнера. (Скріншот)
4.8.	Повертаємося до Containers, обираємо контейнер, який потрібно зупинити та зупиняємо, натиснувши на кнопку зупинення, яка знаходиться біля стовпця Actions. (Скріншот)
4.9.	Після чого контейнер буде призупинено. (Скріншот)

<h2> <b> 5.	Пошук та витягування image контейнера за допомогою графічного інтерфейсу Docker Desktop </b> </h2>

5.1.	В Docker Desktop у навігаційному меню ліворуч переходимо до 
вкладки Images. (Скріншот)
5.2.	В поле пошуку на верхній панелі навігації вказуємо welcome-to-docker, а потім натискаємо на кнопку Pull, щоб завантажити зображення. (Скріншот) 
5.3.	Після чого в Images натискаємо на назву завантаженого image, щоб відкрити його детальну інформацію. (Скріншот)
5.4.	Ця сторінка містить інформацію про шари зображення, пакунки та бібліотеки, встановлені в image, а також будь-які виявлені вразливості. (Скріншот)

<h2> <b> 6.	Створення та відправлення Docker image у репозиторій Docker Hub </b> </h2>

6.1.	Заходимо в Docker Hub. В вкладці Repositories обираємо Create repository для створення репозиторію. Даємо назву docker-quickstart та робимо публічним. (Скріншот)
6.2.	Натискаємо кнопку Create, після чого створиться репозиторій. (Скріншот)
6.3.	В терміналі командного рядка клонуємо репозиторій GitHub за допомогою команди git clone. (Скріншот)
6.4.	Переходимо у щойно створений каталог. (Скріншот)
6.5.	Виконаємо команду docker build, щоб створити Docker image. (Скріншот)
6.6.	Виконаємо команду, щоб отримати список щойно створеного Docker image. (Скріншот)
6.7.	Запускаємо контейнер, щоб перевірити зображення, виконавши команду docker run. (Скріншот),
6.8.	Перевіряємо, чи контейнер працює, відвідавши веб-сайт http://localhost:8080. (Скріншот)
6.9.	Використовуємо docker tag команду, щоб створити тег на Docker image, що дозволяє позначати та версіонувати image. (Скріншот)
6.10.	Відправляємо щойно створений image у репозиторій Docker Hub за допомогою команди docker push. (Скріншот)
6.11.	Відкриваємо Docker Hub і переходимо до нашого репозиторію. 
Переходимо до розділу Tags, щоб переглянути щойно надісланий image. (Скріншот)

<h2> <b> 7.	Використання Docker Compose для запуску багатоконтейнерної програми </b> </h2>

7.1.	Відкриваємо термінал та клонуємо зразок програми. (Скріншот)
7.2.	Переходимо до каталогу todo-list-app. (Скріншот)
7.3.	Використовуємо команду docker compose up для запуску 
програми. (Скріншот)
7.4.	Щоб переглянути сайт відкриємо http://localhost:3000. (Скріншот)
7.5.	В Docker Desktop вкладці Containers ми зможемо побачити контейнери і зануритися в їхню конфігурацію. (Скріншот)
7.6.	Щоб видалити контейнер, в терміналі скористаємося docker compose down. (Скріншот)
7.7.	В Docker Desktop вкладці Containers ми помічаємо, що контейнер видалився. (Скріншот)
 

	
