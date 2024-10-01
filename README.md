# DockerBasics

<h1> <i> Частина I. Вступ </i> </h1>

<h2> <b> 1.	Запуск контейнера Docker за допомогою Docker Desktop. </b> </h2>

1.1. 	Відкриємо термінал командного рядка та запускаємо перший контейнер, виконавши <b>docker run</b> команду.
<p align="left"> <img src="Screenshots/1.1.png" alt="Зображення 1.1"/> </p>
1.2. 	Відвідуємо веб-сайт <a href="http://localhost:8080">http://localhost:8080</a>.
<p align="left"> <img src="Screenshots/1.2.png" alt="Зображення 1.2"/> </p>
1.3. 	Відкриємо Docker Desktop і виберемо поле <b>Containers</b> на лівій бічній панелі.
<p align="left"> <img src="Screenshots/1.3.png" alt="Зображення 1.3"/> </p>
1.4. 	В вкладці <b>Exec</b> можемо отримати доступ до оболонки.
<p align="left"> <img src="Screenshots/1.4.png" alt="Зображення 1.4"/> </p>
1.5. 	Для детальної інформації про контейнер, виберемо поле <b>Inspect</b>.
<p align="left"> <img src="Screenshots/1.5.png" alt="Зображення 1.5"/> </p>

<h2> <b> 2. Розробка контейнерів </b> </h2>

2.1. 	В терміналі клонуємо проект <b>getting-started-todo-app</b> на локальну машину.
<p align="left"> <img src="Screenshots/2.1.png" alt="Зображення 2.1"/> </p>
2.2. 	Переходимо до нового каталогу, створеного клоном.
<p align="left"> <img src="Screenshots/2.2.png" alt="Зображення 2.2"/> </p>
2.3. 	Запускаємо проект за допомогою команди <b>docker compose watch</b>.
<p align="left"> <img src="Screenshots/2.3.png" alt="Зображення 2.3"/> </p>
2.4.	В браузері відкриваємо веб-сайт <a href="http://localhost">http://localhost</a>. 
<p align="left"> <img src="Screenshots/2.4.а.png" alt="Зображення 2.4.a"/> </p>
ㅤㅤ	В цій програмі ми можемо: <br></br>
ㅤ•  Додавати та видаляти елементи. <br></br>
ㅤㅤСкріншот створення двох предметів:
<p align="left"> <img src="Screenshots/2.4.б.png" alt="Зображення 2.4.б"/> </p>
ㅤㅤСкріншот видалення одного з предметів:
<p align="left"> <img src="Screenshots/2.4.в.png" alt="Зображення 2.4.в"/> </p>
ㅤ•  Визначати елемент як виконаний:
<p align="left"> <img src="Screenshots/2.4.г.png" alt="Зображення 2.4.г"/> </p>
2.5. 	В <b>backend/src/routes</b> знаходимо файл <b>getGreeting.js</b> та відкриваємо його.
<p align="left"> <img src="Screenshots/2.5.png" alt="Зображення 2.5"/> </p>
2.6. 	Змінюємо константу, що містить привітання <b>GREETING</b> (перший рядок файла). Замість значення <b>Hello world!</b>, додамо масив привітань.
<p align="left"> <img src="Screenshots/2.6.png" alt="Зображення 2.6"/> </p>
2.7. 	Щоб надіслати випадкове привітання з цього списку, зробимо зміни в <b>res.send</b> (9 рядок коду).
<p align="left"> <img src="Screenshots/2.7.png" alt="Зображення 2.7"/> </p>
2.8. 	Щоб побачити всі привітання, потрібно постійно оновлювати сторінку. З кожним оновленням буде з’являтися нове привітання.
<p align="left"> <img src="Screenshots/2.8.png" alt="Зображення 2.8"/> </p>
2.9. 	В <b>client/src/components</b> знаходимо файл <b>AddNewItemForm.jsx</b> та відкриваємо його.
<p align="left"> <img src="Screenshots/2.9.png" alt="Зображення 2.9"/> </p>
2.10. 	Змінюємо значення текстової підказки поля введення інформації <b>placeholder</b> (37 рядок коду) на <b>What do you need to do?</b>.
<p align="left"> <img src="Screenshots/2.10.png" alt="Зображення 2.10"/> </p>
2.11. 	Оновлюємо веб-сторінку щоб побачити цю зміну.
<p align="left"> <img src="Screenshots/2.11.png" alt="Зображення 2.11"/> </p>
2.12. 	В <b>client/src</b> знаходимо файл <b>index.scss</b> та відкриваємо його.
<p align="left"> <img src="Screenshots/2.12.png" alt="Зображення 2.12"/> </p>
2.13. 	Змінюємо фон сайту <b>background-color</b> (4 рядок коду) на синій.
<p align="left"> <img src="Screenshots/2.13.png" alt="Зображення 2.13"/> </p>
2.14. 	Знову оновлюємо веб-сторінку, тепер фон сайту має синій колір.
<p align="left"> <img src="Screenshots/2.14.png" alt="Зображення 2.14"/> </p>

<h2> <b> 3.	Створення і просування першого образу </b> </h2>

3.1. 	Переходимо до Docker Hub <a href="https://hub.docker.com/">https://hub.docker.com/</a>.
<p align="left"> <img src="Screenshots/3.1.png" alt="Зображення 3.1"/> </p>
3.2. 	Переходимо до вкладки <b>Repositories</b> та обираємо <b>Create repository</b>.
<p align="left"> <img src="Screenshots/3.2.png" alt="Зображення 3.2"/> </p>
3.3. 	Даємо назву репозиторію, короткий опис та обираємо в <b>Visibility</b> загальнодоступну видимість <b>Public</b>.
<p align="left"> <img src="Screenshots/3.3.png" alt="Зображення 3.3"/> </p>
3.4. 	Натискаємо на <b>Create</b>, після чого репозиторій буде створено.
<p align="left"> <img src="Screenshots/3.4.png" alt="Зображення 3.4"/> </p>
3.5. 	В терміналі командного рядка створюємо проект, застосувавши команду <b>docker build -t</b>, вказавши ім’я користувача та назву проекту.
<p align="left"> <img src="Screenshots/3.5.png" alt="Зображення 3.5"/> </p>
3.6. 	Скористаємося командою <b>docker image ls</b> для перевірки наявності Docker image.
<p align="left"> <img src="Screenshots/3.6.png" alt="Зображення 3.6"/> </p>
3.7. 	Надсилаємо image до Docker Hub, використовуючи команду <b>docker push</b>.
<p align="left"> <img src="Screenshots/3.7.png" alt="Зображення 3.7"/> </p>

<h1> <i> Частина II. Основні концепції контейнерів, images, реєстрів і Docker Compose. </i> </h1>

<h2> <b> 4.	Запуск контейнеру Docker за допомогою графічного інтерфейсу Docker Desktop </b> </h2>

4.1. 	Відкриємо Docker Desktop і в поле пошуку на верхній панелі навігації вказуємо <b>welcome-to-docker</b>, а потім виберемо кнопку <b>Pull</b>.
<p align="left"> <img src="Screenshots/4.1.png" alt="Зображення 4.1"/> </p>
4.2. 	Після того, як отримали Docker image, натискаємо на кнопку <b>Run</b>. При натисканні, ми потрапляємо до вікна додаткових параметрів.
<p align="left"> <img src="Screenshots/4.2.png" alt="Зображення 4.2"/> </p>
4.3. 	Розгортаємо <b>Optional settings</b> та вказуємо ім’я контейнеру <b>welcome-to-docker</b> та <b>8080</b> у якості хосту.
<p align="left"> <img src="Screenshots/4.3.png" alt="Зображення 4.3"/> </p>
4.4. 	Тепер ми можемо натиснути на <b>Run</b> для запуску контейнера.
<p align="left"> <img src="Screenshots/4.4.png" alt="Зображення 4.4"/> </p>
4.5. 	На інформаційній панелі Docker, перейшовши до вкладки <b>Containers</b>, можемо переглянути всі контейнери.
<p align="left"> <img src="Screenshots/4.5.png" alt="Зображення 4.5"/> </p>
4.6. 	Відкриємо веб-сайт, перейшовши за посиланням в стовпці <b>Port(s)</b> чи відвідавши <a href="http://localhost:8080">http://localhost:8080</a>.
<p align="left"> <img src="Screenshots/4.6.png" alt="Зображення 4.6"/> </p>
4.7. 	В Docker Desktop натискаємо на контейнер. Після цього обираємо вкладку <b>Files</b>, щоб дослідити ізольовану файлову систему контейнера.
<p align="left"> <img src="Screenshots/4.7.png" alt="Зображення 4.7"/> </p>
4.8. 	Повертаємося до <b>Containers</b>, обираємо контейнер, який потрібно зупинити та зупиняємо, натиснувши на кнопку зупинення, яка знаходиться біля стовпця <b>Actions</b>.
<p align="left"> <img src="Screenshots/4.8.png" alt="Зображення 4.8"/> </p>
4.9. 	Після чого контейнер буде призупинено.
<p align="left"> <img src="Screenshots/4.9.png" alt="Зображення 4.9"/> </p>

<h2> <b> 5.	Пошук та витягування image контейнера за допомогою графічного інтерфейсу Docker Desktop </b> </h2>

5.1.	В Docker Desktop у навігаційному меню ліворуч переходимо до вкладки `Images`. [(Скріншот)](Screenshots/5.1.png) <br></br>
5.2.	В поле пошуку на верхній панелі навігації вказуємо `welcome-to-docker`, а потім натискаємо на кнопку `Pull`, щоб завантажити image. [(Скріншот)](Screenshots/5.2.png) <br></br> 
5.3.	Після чого в `Images` натискаємо на назву завантаженого image, щоб відкрити його детальну інформацію. [(Скріншот)](Screenshots/5.3.png) <br></br>
5.4.	Ця сторінка містить інформацію про шари, пакунки та бібліотеки, встановлені в image, а також будь-які виявлені вразливості. [(Скріншот)](Screenshots/5.4.png) <br></br>

<h2> <b> 6.	Створення та відправлення Docker image у репозиторій Docker Hub </b> </h2>

6.1.	Заходимо в Docker Hub. В вкладці `Repositories` обираємо `Create repository` для створення репозиторію. Даємо назву `docker-quickstart` та робимо публічним. [(Скріншот)](Screenshots/6.1.png) <br></br>
6.2.	Натискаємо кнопку `Create`, після чого створиться репозиторій. [(Скріншот)](Screenshots/6.2.png) <br></br>
6.3.	В терміналі командного рядка клонуємо репозиторій GitHub за допомогою команди `git clone`. [(Скріншот)](Screenshots/6.3.png) <br></br>
6.4.	Переходимо у щойно створений каталог. [(Скріншот)](Screenshots/6.4.png) <br></br>
6.5.	Виконаємо команду `docker build`, щоб створити Docker image. [(Скріншот)](Screenshots/6.5.png) <br></br>
6.6.	Виконаємо команду, щоб отримати список щойно створеного Docker image. [(Скріншот)](Screenshots/6.6.png) <br></br>
6.7.	Запускаємо контейнер, щоб перевірити зображення, виконавши команду `docker run`. [(Скріншот)](Screenshots/6.7.png) <br></br>
6.8.	Перевіряємо, чи контейнер працює, відвідавши веб-сайт <a>http://localhost:8080</a>. [(Скріншот)](Screenshots/6.8.png) <br></br>
6.9.	Використовуємо `docker tag` команду, щоб створити тег на Docker image, що дозволяє позначати та версіонувати image. [(Скріншот)](Screenshots/6.9.png) <br></br>
6.10.	Відправляємо щойно створений image у репозиторій Docker Hub за допомогою команди `docker push`. [(Скріншот)](Screenshots/6.10.png) <br></br>
6.11.	Відкриваємо Docker Hub і переходимо до нашого репозиторію. Переходимо до розділу `Tags`, щоб переглянути щойно надісланий image. [(Скріншот)](Screenshots/6.11.png) <br></br>

<h2> <b> 7.	Використання Docker Compose для запуску багатоконтейнерної програми </b> </h2>

7.1.	Відкриваємо термінал та клонуємо зразок програми. [(Скріншот)](Screenshots/7.1.png) <br></br>
7.2.	Переходимо до каталогу `todo-list-app`. [(Скріншот)](Screenshots/7.2.png) <br></br>
7.3.	Використовуємо команду `docker compose up` для запуску програми. [(Скріншот)](Screenshots/7.3.png) <br></br>
7.4.	Щоб переглянути сайт відкриємо <a>http://localhost:3000</a>. [(Скріншот)](Screenshots/7.4.png) <br></br>
7.5.	В Docker Desktop вкладці `Containers` ми зможемо побачити контейнери і зануритися в їхню конфігурацію. [(Скріншот)](Screenshots/7.5.png) <br></br>
7.6.	Щоб видалити контейнер, в терміналі скористаємося `docker compose down`. [(Скріншот)](Screenshots/7.6.png) <br></br>
7.7.	В Docker Desktop вкладці `Containers` ми помічаємо, що контейнер видалився. [(Скріншот)](Screenshots/7.7.png) <br></br>
 

	
