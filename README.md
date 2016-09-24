##Особенности рабочего процесса:

* Весь входящий материал на разработку предоставляется «одной пачкой»

* Весь ТЗ на разработку конкретизированное, полное, по одному формату

* Вас «не трогают» во время выполнения ТЗ.

* Ваше время не тратят «люди которые часто «не понимают»». Вы общаетесь изредка с менеджером по front-end для уточнения чего-то и с техническим директором.

* Технический директор проверяет качество выполнения по вышеуказанным требованиям, консультирует в случае трудностей

* Технический директор предоставляет и регулярно обновляет свою «базу знаний» - гайды по работе с инструментами, автоматизации рабочих процессов, обучающие гайды, gistbox,evernote

* Все взаимодействие с файлами проектов в команде ведется через github


##На данном этапе вы должны уметь:

* Скриптовать лендинги

* Писать css @keyframes

* Привязывать анимации и прочие плюшки с cordops

* Повторять функционал, указанный в ТЗ/примере

* Подключать ЯМ/ГА/подобные и устанавливать цели

* Быть способным к изучению новых фреймворков и АПИ


##Общие требования по роботе:

* Кроссбраузерность, кросплатформенность, 0 ошибок выполнения скриптов и подключения ресурсов - (10 последних версий браузеров OSX/iOS/Windows/Android).

* Весь код beautified – нормально структурирован.

* Изменения вносятся в оригинальные(не минифицированные) файлы

* При минификации css js файлов оригиналы остаются в папке проекта.

* Стартовые навыки по работе с grunt, github


##Требования к написанию html кода:

* Верстка по стандартам html5 – 0 ошибок валидатора https://validator.w3.org/

* Верстка должна иметь карту заголовков без ошибок(https://validator.w3.org/ опция outline) 

* До и после br в одной строке, перед br всегда есть пробел, даже после оптимизации

* Табуляция 4 пробела/Tab

* Нету пустых строк и лишних пробелов

* Прописаны meta charset,viewport,favicon

* Стили сайта (css) вынесены в отдельные файлы: libs.css(стили библиотек) style.css(стили статической верстки) media.css(медиазапросы) scripts.css(стили скриптов) head.css(часть css необходимая для отобржания(!) первого екрана)

* Допускается использовать блок style /style только(!) в head в целях оптимизации скорости загрузки, в этом случае они вынесены в src/css/head.css и импортируются средствами php - style ? include('css/head.css'); ? /style

* Для привязки стилей приоритетно пользуемся классами и вложениями

* Адекватные(понятные) названия для селекторов

* html  код сайта семантичен. Тексты должны быть текстами (p, span), заголовки заголовками (h1-h6), формы формами (form), списки-списками, тдтп. Контентовые картинки (не фоновые) img

* Только один h1

* html lang="ru"

* Кнопки a или button

* Запрещено использовать инлайн-стили (атрибут style="")

* Можно использовать только 1н класс на елементе(!), исключения елементы имеющие несколько состояний(active,disactive), в этом случае допускается использование второго (.active,.disactive) класса

* Не использовать on[event] атрибуты(onclick,onsubmit,onchange)

* Минимальное количество элементов html (исключить лишние вложения, чаще использовать :before и :after)

* Основные скрипты подключаются асинхронно перед  /head

* table tr td использовать только(!) для разметки таблиц

* Скрипты для карты и подобные подключаются синхронно перед /body

* Допускается script[code]/script в /head для перернаправления между страницами-версиями/АБ вариантами

* Коды трекингов/плагинов/сервисов вынесены в отдельные файлы для /head и /body соответвенно


##Требования к написанию css кода:

* Использовать библиотеку normalize.css

* Шрифты подключаются целыми семействами - {font-family:Open Sans;font-weight:300}, а не {font-family:opensanslight}

* Плавность css анимаций (.button{transition:all 0.25s})

* Правильное использование margin и padding

* Правильное использование css position и только там где это необходимо.

* Правильные выборы форматов изображений (png/jpg) и их размеров. Не использвоать картинки для одноцветных фонов.

* Выполнение функций фотошопа таких как тень, прозрачность скругливание углов средствами css.

* Срезы картинок, функция линейного градиента фотошоп -  средствами css

* Написание новых css правил в соответсвующих файлах

* Кроссбраузерность, кросплатформенность (android 4.4.1+, iOS7+, desctop)

* Автопрефикс ie >= 8,last 10 versions,> 0.1%

* Не вносить изменения в src/[version]/css/libs.css, src/[version]/css/libs.min.css, src/[version]/css/full.css, src/[version]/css/full.min.css, src/[version]/css/libs/*.css

* Не вносить изменения в src/[version]/css/style.css и src/[version]/css/style.min.css если они результат работы препроцессора

* Обязательное описание :hover и :active состояний на активных элементах

* Использовать !important только там где это необходимо

* При использовании position:absolute, position:relative, position:fixed в пределах правила должен стоять z-index (android 4.4.1 bug)

* Не использовать vh vw измерения, кроме как 100vh для создания фулл-пейдж блока(android 4.4.1 bug)

* Не использовать селекторы  :nth-child(), :first-child, last-child, на замену им - :nth-of-type() (iOS8 bug)

* Не использовать сокращенный(Универсальный) background, на замену ему background-color,background-image,background-repeat,background-position (android 4.4.1 bug)

* Не использовать transform:translateX(),transform:translateY(),transform:translateZ(), на замену им transform:translate3d() (android 4.4.1, iOS8 bug NS)

* При использовании background-size:cover в пределах правила должен стоять position:absolute/position:relative (android 4.4.1 bug)

* Если в текстовом блоке использовано br фиксировать размер блока по высоте (android 4.4.1 bug изменение ширины текстовых блоков до ширины экрана)

* Учитывать разный рендер шрифтов в разных осях, браузерах, размерах экранов - фиксировать ширины текстовых блоков с запасом min 10px

* Aктивно использвоать наследование и каскадирование

* Использование препроцессоров css приветстсвуется.


##Требования к написанию jsкода:

* Работа на фреймворке jquery

* Кроссбраузерность, кросплатформенность (android 4.4.1+, iOS7+, desctop)

* 0 ошибок выполнения

* Не вносить изменения в src/[version]/js/libs.js, src/[version]/js/libs.min.js, src/[version]/js/full.js, src/[version]/js/full.min.js, src/js/libs/*.js

* Основной скрипт сайта - src/[version]/js/main.js

* Каждая логическая часть откоментирована

* Правильное распределние функций между document.ready, window.load, $

* Максимально быстрый рендер страницы(минимум необходимых функций для инициализации) 

* “Классовая политика” функций. Используйте данные  в тегах html элементов (href,data-XXXX) для объединений аналогичных функций (например вызов попапов по клику, переход к слайду, тдтп).

* Минимум использования глобальных переменных

* Минимум setInterval функций.

* Рекомендуемая библиотека для галерей - fancybox, для слайдеров - bxslider, для модальных окон - arcticmodal

* Тэги <? в файлах php должны быть прописаны как <?php