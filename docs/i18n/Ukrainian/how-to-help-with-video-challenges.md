# Як допомогти з відеовикликами

Відеовиклики - це новий тип виклику у навчальній програмі freeCodeCamp.

Відео-виклик - це маленька частина курсу з повною тривалістю на певну тему. Вкладення відео до відео з завданням. Кожна сторінка завдання має одне питання з безліччю вибору, яке стосується відео. Користувач повинен правильно відповісти на питання, перш ніж перейти до наступного відео-виклику в курсі.

Сторінки з відео-викликів створюються членами команди freeCodeCamp . Відео від YouTube також завантажуються членами безкоштовного Кодексу. Багато відеовикликів ще не мають питань, пов'язаних з ними.

Ви можете допомогти, створивши питання з декількома відповідями на вибір для відео розділів і додавши питання до файлів розмітки для відео-задач.


## Шаблон виклику

Нижче наведено шаблон того, як виглядають файли виклику markdown.

````md
---
Унікальний ідентифікатор (alphanumeral, MongoDB_id)
title: Заголовок виклику
challengeType: 11
videoId: 'YouTube videoId для відеодзвінка
---

## Опис

<section id='description'>
Факультативний опис з корисною інформацією, пов'язаною з відео.
</section>

## Тести

<section id='tests'>

`yml
question:
  текст: 'Питання'
  відповідей:
    - 'Відповісти Одній'
    - 'Відповідь Two'
    - 'Відповідь Three'
  solution: 3
````

</section>
````

## Створення питань для відео-викликів

### Доступ до відео файлів з комплексом розмітки

Ви можете знайти файли markdown для відео-викликів на таких місцях у навчальній програмі:

- [Аналізатор даних з Python Курсом](https://github. om/freeCodeCamp/freeCodeCamp/tree/master/curriculum/challenges/english/08-data-analysis-with-python/data-analysis-with-python-course)
- [TensorFlow 2.0 Курс](https://github. om/freeCodeCamp/freeCodeCamp/tree/master/curriculum/challenges/english/11-machine-learning-with-python/tensorflow)
- [Numpy Course](https://github.com/freeCodeCamp/freeCodeCamp/freeCodeCamp/treric/curriculum/challenges/english/08-data-Analis-with-python/numpy)
- Як несільські Неробочі Курси(https://github.com/freeCode/freeCode/tree/master/curulum/challenges/englum/engle-learning-with-py/11-machin-al-thon-neurs-uk-network

Вибрати варіант з відповідного файлу зверху.

### Скайм через відео, пов'язане з викликом та створити мультиплікаційне запитання

Спочатку, знайти відеоматеріал.

Наприклад, у наступному коді з заголовка файлу з відеоспостереженням, відео містить "nVAaxZ34khk". На GitHub, інформація повинна зберігатися в форматі таблиці.
````
---
id: 5e9a093a74c4063ca6f7c14d title: Аналізатор даних приклад challengeType: 11
videoId: nVAaxZ34khk
---
```

Далі доступ до відео на YouTube з цим відеороликом. URL-адреса для відео буде так:
https://www.youtube. om/watch?v=[videoId]    (додайте videoId на URL без квадратних дужок)

У прикладі вище, URL-адреса - https://www. outube.com/watch?v=nVAaxZ34khk

Skim відео YouTube з цим відеоID та думати про множинний вибір на основі вмісту відео.

### Додайте питання до файлу розмітки

Ви можете додати питання локально або безпосередньо через GitHub інтерфейс. Щоб додати питання локально, вам потрібно [налаштувати безкоштовноCodeCamp локально](як-setup-freecodecamp-locally.md). Ви також можете знайти файл на GitHub і натисніть кнопку редагування, щоб додати питання прямо в вашому браузері.

Якщо питання ще не було додане до певної відео-виклику, у нього буде наступне запитання за замовчуванням:

```yml
питання:
  текст: |
    Питання
  відповідей:
    - |
      один
    - |
      два
    - |

  рішення: 3
```

Оновіть слово "Питання" своїм питанням. Оновіть "один", "два" та "трійку" з можливими відповідями. Переконайтеся, що оновлення номеру розв'язку з відповіддю буде правильною. Ви можете додати більше відповідей використовуючи такий же формат. Питання і відповіді можна оточити лапками.

#### Використовувати markdown для форматування вашого питання

Текст у питанні розцінюється як розмітка. Найпростіший спосіб переконатися, що він відформатований правильно, це розпочати питання з `тексту: |`, на зразок цього:

```yml
запитання:
  текст: |
    Питання
```

Тоді ви повинні переконатися, що ваше питання знаходиться на новому рядку, і для відступу на один рівень більше, ніж `текст: |`.

Один і той самий підхід можна використовувати для відповідей тому повне питання стає

```yml
запитання:
  текст: |
    Питання
  відповіде:
  - |
    Перша відповідь
  - |
    Друга
  - |
    Трет
  рішення: 2
```

Переконайтеся, що кожна відповідь правдоподібна, але є лише одна правильна відповідь.

#### Використання HTML

Питання та відповіді можуть містити певні теги HTML, такі як `<br>` - новий рядок. HTML-теги повинні використовуватися одночасно, якщо питання не можуть бути виражені без них.

### Приклади питань

#### Приклади без HTML

````yml
запитання:
  текст: |
    Що робить цей JavaScript код в консоль?
    ```js
    console.log('Привіт світ');
    ````


    Виберіть відповідь!
  відповідей:
    - | привіт *світ*
    - | **привіт** світ
    - | привіт світ рішення: 3
````

``yml
питання:
  текст: |
    Що виведе на екран після запуску цього коду:
    ```py
    width = 15
    висота = 12.
    print(висота/3)
    ````
  відповідей:
    - | 39
    - | 4
    - | 4.0
    - | 5.0
    - | 5 рішення: 3
````

#### Приклад з HTML

`yml
question:
  текст: |
    Що виведе після запуску цього коду:
    <pre><code>ширина = 15<br>висота = 12.<br>print(height/3)<code></pre>
  відповідей:
    - |
      39
    - |
      4
    - |
      4.
    - |
      5.
    - |
      5
  рішення: 3
````

Остаточний приклад демонструє, що HTML можна використовувати, але він не такий читабельний, як версія без нього.

Для прикладів, ви можете переглянути файли markdown для наступного відео-курсу. Усі виклики вже мають запитання: [Python для всіх курсів](https://github.com/freeCodeCamp/freeCodeCamp/tree/master/curriculum/challenges/english/07-scientific-computing-with-python/python-for-everybody)

## Відкрити запит на злиття

Після створення одного або декількох запитань, ви можете затвердити зміни до нової гілки і [відкрити pull request](how-to-open-a-pull-request.md).
