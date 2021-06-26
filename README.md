# RS.School. Task 2. Quiz for Android (2021)
Rolling Scopes School - Android 2021. Stage 1. Task 2. Quiz

:point_up: Во втором практическом задании создадим приложение-квиз, с возможностью шарить результат

<img alt="quiz app" src="/img/quiz.gif" width="250" height="500" />

[или см. демо-видео на YouTube](https://www.youtube.com/watch?v=jG3W5w6pfuw)

## Описание задания

Приложение состоит из нескольких экранов с вопросами (минимальное число вопросов 5) и экрана с результатом. На экране с вопросом:

- текст вопроса
- варианты ответов - оформить как radio buttons. Давайте для простоты установим, что только один вариант ответа правильный. Пользователь не может выбрать несколько вариантов ответа на вопрос, только один (принцип radio buttons). Пользователь может менять свой выбор. Минимальное число вариантов ответов 5.
- кнопка `Next` - ведёт на следующий экран с вопросом. На последнем экране с вопросом меняется на `Submit`. Нажатие на `Submit` открывает экран с результатом квиза. Кнопки `Next` и `Submit` недоступны, если вариант ответа не выбран.
- кнопка `Previous` - ведёт на предыдущий экран с вопросом. Недоступна для первого экрана с вопросом. 
- на `Toolbar` отображается порядковый номер вопроса

При переходах между экранами через кнопки `Previous` или `Next` уже выбранные варианты ответов сохраняются. Варианты ответов могут быть изменены до нажатия `Submit`. На toolbar доступна кнопка `<`, поведение которой аналогично поведению `Previous`.

На экране с результатом:

- текст результата, отображающий информацию о количестве верных ответов. Например, "Результат: 40 %" или "Результат: 5 из 5" - тут на ваше усмотрение.
- кнопка `Share` - возможность пошарить результат квиза. Например, через email. При этом сгенерированный текст должен содержать: результат квиза, список вопросов с порядковым номером вопроса и c выбранным пользователем вариантом ответа.
- кнопка `Back` - сбрасывает результаты квиза. Перенаправляет пользователя на начальный экран.
- кнопка `Exit` - закрывает приложение

📱 Требования к дизайну:

- смотрите пример возможного дизайна выше на видео. В layouts в этом репозитории дан возможный layout фрагмента с вопросом. Можно оставить как есть или сделать свой вариант.
- каждому отдельному экрану с вопросом должна соответствовать своя тема (Theme). В репозитории есть возможные варианты цветов и 2 темы. Можно добавить свои темы и цвета по аналогии, менять существующие темы и цвета.

💻 Требования к коду:

- в прошлый раз мы получали ссылки на view через `findViewById()`. На сегодня это не самый лучший вариант. Давайте использовать [view binding](https://developer.android.com/topic/libraries/view-binding#kotlin) 
- Kotlin
- способы хранения данных с вопросами, вариантами ответов, и правильными вариантами - на ваше усмотрение: можно захардкодить в виде списков прямо в исходниках, читать из файла или из базы данных, etc. - это никак не влияет на баллы, поэтому выбирайте способ, который вам удобнее. Вопросы можно любые, язык не важен, в рамках приличия и более-менее осмысленные 🙂
- в качестве рекомендации: используйте для этого и других проектов [ktx-library](https://developer.android.com/kotlin/ktx). Это общая практика. Код становится красивее, кодить удобнее... Например, `arguments` для фрагмента можно задавать используя [bundleOf()](https://developer.android.com/reference/kotlin/androidx/core/os/package-summary#bundleof)
- старайтесь, чтобы код выглядил читабельно. Следите за форматированием. Лучше разбить логику на несколько методов и дать им осмысленные названия, чем пытаться уместить всё в один метод. Не используйте `var` там, где достаточно `val`. Не стоит использовать уловки типа `!!` или `lateinit`, если без них можно обойтись... Изучайте [Kotlin Coding conventions](https://kotlinlang.org/docs/coding-conventions.html)
- не злоупотребляйте программированием, отдыхайте, депривация сна приводит к существенному снижению работоспособности 🛌🏼


## Cross-checking

- Изучите требования к <a href="https://docs.rs.school/#/cross-check-flow?id=cross-check">cross-check</a>
- Форму для оценки задания по критериям ищите <a href="https://ziginsider.github.io/checklist/index.html">здесь</a> ⚡️

Успехов! 🤞
