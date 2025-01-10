# АНАЛИЗ СОВРЕМЕННЫХ САЙТОВ
## ЛАБОРАТОРНАЯ РАБОТА № 10 по дисциплине «Веб-технологии»
**Выполнила**: Студентка группы 241-671 Корышева А.А.

### Подбор сайтов и их описание
1. [Notamedia](https://nota.media/) - презентация и продажа услуг международного интегратора и Digital-агенства
1. [CreativePeople](https://cpeople.ru/) - презентация и продажа услуг агенства цифрового дизайна продуктов.
1. [Факт](https://fact.digital/) - проектирование и развитие гибких цифровых экосистем.
1. [CHIPSA](https://chipsa.ru/) - создание нестандартных сайтов и интерфейсов с креативной графикой.
1. [Магвай](https://magwai.ru/) - креативная студия дизайна, разработка сайтов с нуля.
1. [Mish](https://mish.design/) - создание цифровых продуктов для бизнеса
1. [Xpage](https://www.xpage.ru/) - разработчик высоконагруженных цифровых решений для среднего и крупного бизнеса.
1. [RuNetSoft](https://softcreators.ru/) - заказная разработка и внедрение сложных информационных систем для комплексной автоматизации бизнес-процессов.
1. [PINKMAN](https://www.pinkman.ru/) - создание продуктовых дизайнов, корпоративных сайтов, интерфейсов.
1. [ILAR.PRO](https://ilartech.com/) - продуктовая аналитика, маркетинг, дизайн и разработка digital-продуктов.

### Описание свойств CSS
|№|Свойство|Назначение|Где встретилось|
|-|--------|----------|---------------|
|1|letter-spacing|межбуквенное расстояние|[CreativePeople](https://cpeople.ru/)|
|2|pointer-events:[auto, none]|определяет реакцию элемента на наведение или клик курсора[реагирует, не реагирует]|[CreativePeople](https://cpeople.ru/)|
|3|aspect-ratio:[width/height, auto, inherit, initial, revert, unset]|явная установка соотношения сторон элемента|[Факт](https://fact.digital/)|
|4|unicode-bidi:[normal, embed, bidi-override, isolate, plaintext, initial, inherit]|определяет работу двунаправленного текста|[Магвай](https://magwai.ru/)|
|5|will-change:[auto, scroll-position, contents, transform, opacity, left, top]|указывает браузеру как должен изменяться элемент|[Mish](https://mish.design/)|
|6|:target{}|псевдокласс, управляющий стилем элемента, на который ссылкается якорная ссылка|[CHIPSA](https://chipsa.ru/)|
|7|:focus-within{}|псевдокласс, определяющий стиль элемента, когда он сам или элементы внутри него получают фокус|[CHIPSA](https://chipsa.ru/)|
|8|mobile|стиль, применяющийся только к мобильным устройствам|[PINKMAN](https://www.pinkman.ru/)|
|9|:focus-visible{}|псевдокласс, стилизующий элемент, если он получил фокус заданным образом ( ограничение на вид фокуса)|[PINKMAN](https://www.pinkman.ru/)|
|10|scroll-behavior:[auto, smooth]|определяет поведение прокрутки внутри элемента[стандартное, плавное]|[ILAR.PRO](https://ilartech.com/)|

### Структура сайта [RuNetSoft](https://softcreators.ru/)
![Вид сайта](<image src="вид сайта.jpg">)

Первый уровень. - ```<!DOCTYPE html>``` Объявление типа документа.

Второй уровень. - ```<html lang="ru">``` Корневой элемент документа. Атрибут lang указывает язык документа.

Третий уровень. 
1. ```<head>``` Метаданные страницы и подключение стилей/скриптов. Содержит ```<meta>, <link>, <title>, <script>``` и т.д. 
1. ```<body>``` Основное содержимое страницы.

Четвертый уровень (внутри body). Содержимое страницы делится на следующие основные секции:
1. Шапка - ```<header class="header fixedHeader">```.
1. Основная часть ```<div class="main__pageBlock-container">``` — контейнер. *Внутри*(пятый уровень):
- ```<div class="main__bg">``` — фон.
- ```<section class="main__section"></section>``` — раздел.
- ```<section class="main green-section"></section>``` — второй раздел.
3. Меню.
- ```<section id="about" class="about section"></section>``` — секция "О нас". В CSS отрегулированы отступы.
- ```<section id="news" class="news section"></section>``` — секция "Новости". В CSS отрегулированы отступы.
- ```<section id="partners" class="partners section"></section>``` — секция "Партнеры". В CSS отрегулированы отступы.
- ```<section id="form" class="form section"></section>``` — контактная форма.
4. Модальные окна.
- ```<div class="modaWindow modalThx modal-form"></div>``` — окно благодарности.
- ```<div class="modaWindow modalNews modal-news"></div>``` — окно для новостей.
5. Подвал (Footer) - ```<footer class="footer"></footer>```.

---

Анализ кода. 
1. Частично используется методология BEM, но встречаются плохо читаемые названия. Это усложняет поддержку кода.
1. Избыточные **div**, их можно заменить более семантическими тегами.
1. HTML5 теги используются, но не полностью эффективно. Присутствуют семантические теги, такие как **header**, **footer**, **section**. Вместо **div** можно было использовать другие элементы, например, тег **main**. 
1. Код можно считать удобно читаемым.

---

Описание основных классов CSS:
1. **.main__title-block{}**
    - position: relative; — элемент позиционируется относительно своего исходного положения в потоке.
    - padding: 126px 0 210px 0; — вертикальные внутренние отступы (126px сверху, 210px снизу) без отступов по горизонтали.
    - max-width: 551px; width: 100%; — ограничение ширины блока до 551px, присвоение ей 100% родителя.
    - margin-top: 135px; — смещение блока вниз на 135px относительно предыдущего элемента.
1. **.main__bg{}** 
    position: absolute; - позволяет элементу перемещаться из потока документа и быть позиционированным абсолютно внутри своего контейнера.
    min-width: 100%; - минимальная ширина элемента
    min-height: 100%; - минимальная высота элемента
    z-index: 0; - уровень слоя элемента, самый минимальный, что позволяет элементам с большим уровнем располагаться над ним.
    background: url(/img/back/background1.jpg) repeat-x; - устанавливает фоновое изображение, которое будет повторяться только по горизонтальной оси.
    background-size: cover; - масштабирует фоновое изображение так, чтобы оно полностью покрывало элемент, сохраняя свои пропорции.
1. **.body{}** 
    - font-family: 'Montserrat', sans-serif !important; - устанавливает для текста в шрифт "Montserrat" с запасным вариантом — стандартным шрифтом sans-serif (на случай, если "Montserrat" не загрузится). Присваивает свойству максимальный приоритет 
    - font-style: normal; - используется для предотвращения случайного применения курсивного текста из других стилей.
    - display: -webkit-box; - это свойство применялось в старых браузерах, до появления полноценной поддержки Flexbox.  
    - display: -webkit-flex, display: -ms-flexbox; - нужно для поддержки старых версий Chrome, Safari
    - display: flex; - указывает на управление дочерними элементами Flexbox
    - webkit-box-orient: vertical; - указывает вертикальную ориентацию контейнера для старых версий.
    - webkit-box-direction: normal; - указывает на стандартное расположение дочерних элементов контейнера для старых версий.
    - webkit-flex-direction: column, ms-flex-direction: column, flex-direction: column; - устанавливает вертикальное расположение всех дочерних элементов, например, для создания колонки в разных версиях.
    - position: relative; - элемент позиционируется относительно своего исходного положения в потоке.
1. **.main__pageBlock-container{}** 
    - display: -webkit-box, display: -webkit-flex, display: -ms-flexbox, display: flex; - задаёт блоку поведение Flexbox-контейнера
    - -webkit-box-orient: vertical, -webkit-box-direction: normal, -webkit-flex-direction: column, -ms-flex-direction: column, flex-direction: column; - устанавливает направление оси flex-контейнера по колонке. Элементы располагаются вертикально.
    - min-height: 100vh, height: 100%; - задаёт минимальную высоту контейнера равной 100% высоты окна браузера, дополняет поведение, задавая высоту в 100% относительно родительского элемента, если нужно.
    - overflow: hidden; - обрезает содержимое, которое выходит за границы контейнера.
    - background-color: #ccdbd9; - устанавливает фон контейнера светло-зелёного оттенка.
    - position: relative; - позиция контейнера остаётся в обычном потоке документа.
1. **.form__section{}**
    - background-image: url(../img/photoBgForm2.png); - задаёт фоновое изображение. 
    - background-position: center; - устанавливает позиционирование фонового изображения в центре контейнера.
    - background-repeat: no-repeat; - запрещает повторение фона.
    - background-size: cover; - указывает размер фоновой картинки так, чтобы она полностью покрывала контейнер, сохраняя пропорции.
    - padding: 96px 0 82px 0; - добавляет внутренние отступы.
    - background-image: url(../img/back/background2.jpg); - задаёт фоновое изображение. 
    - background-repeat: repeat-x; - фон будет повторяться только по горизонтали.
    - background-size: cover; - размер фона подстраивается для полного покрытия.
1. **.footer{}** 
    - padding: 62px 0px 46px 0px; - отступ определяет внутренние расстояния между содержимым элемента.
    - background-color: #124d52; - устанавливает фоновый цвет для элемента.

### Пошаговая реализация секции формы с сайта [RuNetSoft](https://softcreators.ru/)
1. **Создайте `section` для формы и укажите ей уникальный класс и идентификатор**   
    - `class="form__section"` — используется для стилизации данной секции.  
    - `id="form"` — для внутренних ссылок, чтобы перейти к форме по якорю.  

   Пример:
   ```html
   <section class="form__section" id="form"></section>
   ```
   ```css
   .form__section {
        padding: 96px 0 82px 0; 
        background: #1b616d; 
        background-image: url(../img/back/background2.jpg); 
        background-repeat: repeat-x; 
        background-size: cover;
    }
   ```

---

2. **Внутри `section` создайте контейнер для центрирования контента**  
   - `class="container"` — ограничивает ширину формы и позволяет использовать отступы по бокам.

   Пример:
   ```html
   <div class="container"></div>
   ```
   ```css
    .container {
        max-width: 1142px;
        margin: 0 auto;
        width: 100%;
    }
   ```

---

3. **Добавьте заголовок для секции**  
   - `class="title-section"` — применяет стили к заголовку секции.  

   Пример:
   ```html
   <p class="title-section">Оставить заявку</p>
   ```
   ```css
    .title-section {
        font-weight: 400;
        font-size: 32px; 
        line-height: 39px; 
        color: #124d52; 
        margin-bottom: 66px;
    }
   ```
   - Убедитесь, что отступы (margin-bottom) согласуются с общим дизайном секции.
---

4. **Создайте контейнер для самой формы**  
   - `class="form__container"` — заключает форму внутри отдельного блока для удобного управления.

   Пример:
   ```html
   <div class="form__container"></div>
   ```
   - Если потребуется дополнительный стиль для .form__container, например, настраиваемое позиционирование или тени, добавьте его.  

---

5. **Добавьте тег формы `<form>` с уникальным классом и настройками**  
    - `action="send.php"` — указывает на обработчик формы.  
    - `method="post"` — метод отправки.  
    - `autocomplete="off"` — отключает автозаполнение.  
    - `id="form-contact"` — уникальный идентификатор для действий с формой через JavaScript.  

   Пример:
   ```html
   <form class="form__body" action="send.php" autocomplete="off" id="form-contact"></form>
   ```
   - Обычно к самому тегу формы (form) стили добавляются редко, но можно указать отступы (padding) для дополнительного внутреннего пространства.

---

6. **Внутри формы добавьте контейнер для строк с полями**  
   - `class="form__rowInputs"` — заключает все поля формы в отдельный ряд.

   Пример:
   ```html
   <div class="form__rowInputs"></div>
   ```
   ```css
    .form__rowInputs {
        display: flex;
        flex-wrap: wrap;
        width: 100%; 
    }
   ```

---

7. **Добавьте поле ввода для имени пользователя**  
    - `type="text"`, `name="name"` — стандартное текстовое поле для имени.  
    - `placeholder="*Ваше имя"` — подсказка для пользователя.  
    - `required` — делает поле обязательным для заполнения.  

   Пример:
   ```html
   <div class="form__inputBlock">
       <input type="text" name="name" placeholder="*Ваше имя" required>
   </div>
   ```
   ```css
    .form__inputBlock {
        margin-bottom: 56px; 
        margin-right: 26px; 
    }
   ```

---

8. **Добавьте поле ввода для названия организации**  
   - Поле принимает текст с `name="org_name"` и полем подсказки `placeholder`.  

   Пример:
   ```html
   <div class="form__inputBlock">
       <input type="text" name="org_name" placeholder="*Название организации" required>
   </div>
   ```

---

9. **Добавьте поле ввода для email**  
    - Спецификация `type="email"` проверяет правильность ввода e-mail.  
    - Поле дополнено подсказкой (`placeholder`).  

   Пример:
   ```html
   <div class="form__inputBlock">
       <input type="email" name="email" placeholder="*E-mail" required>
   </div>
   ```

---

10. **Добавьте необязательное поле для телефона**  
    - Поле ввода телефона с `name="phone"` и полем подсказки `placeholder`.

    Пример:
    ```html
    <div class="form__inputBlock">
        <input type="tel" name="phone" placeholder="Телефон">
    </div>
    ```

---

11. **Добавьте текстовое поле (`textarea`) для описания проекта**  
    - `name="text"` — позволяет отправить текст предложения.  
    - `placeholder="Опишите проект"` — предлагает пользователю написать свой текст.

    Пример:
    ```html
    <div class="form__inputBlock">
        <textarea name="text" placeholder="Опишите проект"></textarea>
    </div>
    ```

---

12. **Скрытое поле для защиты от спама (antibot-check)**  
    - Поле с классом `display: none` предотвращает автоматическую отправку ботами.

---

13. **Добавьте кнопку отправки формы**  
    - Кнопка с текстом "Отправить" и атрибутом `type="submit"`.  

    Пример:
    ```html
    <button class="btn" type="submit">Отправить</button>
    ```
    ```css
    .btn {
        display: block;
        padding: 12px 48px; 
        background-color: transparent; 
        border: 1px solid #124d52;
        border-radius: 30px; 
        transition: 0.3s;
        font-weight: 400; 
        font-size: 18px;
        color: #124d52; 
    }
    ```
    - Вы можете добавить изменение кнопки при взаимодействии с ней.

---

14. **Сверстайте все элементы и проверьте стили**  
    Убедитесь, что секция корректно отображается на странице: структура разметки завершена, стили из подключенных CSS-файлов применяются правильно.

---

15. **Добавьте JavaScript для обработки формы**  
    Если форма требует валидации перед отправкой, подключите скрипт для проверки.

---

16. **Проверьте `action` пути к `send.php`**  
    Убедитесь, что обработчик формы существует и принимает необходимые данные.

---

17. **Протестируйте корректную отправку данных**  
    Проверьте заполнение всех полей и отправку данных на сервер. Убедитесь, что отсутствуют ошибки на собственных примерах.

### Ресурсы для изучения верстки
1. [Курс на Skillbox](https://bootcamp.skillbox.ru/digital-design-mini?utm_source=yandex&utm_medium=cpc&utm_campaign=all_all_yandex_cpc_master-campaign_bootcamp-623_all_short_skillbox_99997794&utm_content=adg_5325525788%7Cad_16397234244%7Cph_48245231145%7Ckey_---autotargeting%7Cdev_desktop%7Cpst_premium_1%7Crgnid_172_Уфа%7Cplacement_none%7Ccreative_%7Bcreative_name%7D&utm_term=---autotargeting&yclid=683355871678038015)
1. [Обучающие уроки](https://vk.com/web_and_graph?search_track_code=63957072r5TWKLxmrsxcCjkwinuMeO_LdCrC9O9A-m1KGxDuANj3C33ZaqAwW-TGDwnPKdUzv6VGKtzzh0GX&from=search)
1. [Канал веб-программирования](https://youtube.com/@educatterofficial?feature=shared)
1. [Создание веб-сайтов](https://youtube.com/@brainscloud?feature=shared)
1. [Онлайн школа программирования и веб-разработки](https://youtube.com/@itproger?feature=shared)
1. [Онлайн школа программирования и веб-разработки(2)](https://youtube.com/@webproschool?feature=shared)
1. [Веб-дизайн в Figma](https://t.me/figmaweb)
1. [HTML и CSS для новичков](https://code.mu/ru/markup/book/prime/)
1. [CSS учебник](https://www.schoolsw3.com/css/)
1. [HTML учебник](https://www.schoolsw3.com/html/index.php)