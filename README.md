## WebCore

* [Общие вопросы](General/README.md)
* [Web Technologies](WebTech/README.md)
* [CSS](CSS/README.md)
* [Ещё CSS](CSSfaq/README.md)
* [Web API](WebAPI/README.md)
* [HTML](HTML/README.md)
  
**CORS** (Cross-Origin Resource Sharing, англ. «совместное использование ресурсов разных источников»)
  
стандарт, позволяющий предоставлять веб-страницам доступ к объектам сторонних интернет-ресурсов. Сторонним считается любой интернет-ресурс, который отличается от запрашиваемого протоколом, доменом или портом.  
механизм использует дополнительные HTTP-заголовки.  
С ним браузер пользователя получает разрешения на доступ к выбранным ресурсам, если домен сайта и домен запрашиваемого ресурса отличаются.  
[CORS](https://github.com/AntonGitCode/FEFAQ/blob/master/General/16.md)  
    
**REST** [читать](https://github.com/AntonGitCode/FEFAQ/tree/master/WebTech#rest) Representational State Transfer - архитектурный стиль API.  
стиль общения компонентов, при котором все необходимые данные указываются в параметрах запроса — всё взаимодействие между клиентом и сервером сводится к 4 операциям (CRUD).
  
**OSI** [читать](https://github.com/AntonGitCode/FEFAQ/blob/master/WebTech/README.md#ossi)

**прогрессивный рендер** [читать](https://github.com/AntonGitCode/FEFAQ/blob/master/WebTech/README.md#prorender)   
  **прогрессивные SSR** [читать](https://github.com/AntonGitCode/FEFAQ/blob/master/WebTech/README.md#ssr)  
  SSR, CSR, SSG [читать](https://github.com/AntonGitCode/FEFAQ/blob/master/WebTech/README.md#diff)  
  
**веб-компоненты** - переисп комп ,с брауз напрямую без исп библ [читать](https://github.com/AntonGitCode/FEFAQ/blob/master/WebTech/README.md#webcomp)  
**Поток** - это принцип организации элементов на странице, при отсутствии стилей - [читать](https://github.com/AntonGitCode/FEFAQ/blob/master/WebTech/README.md#potok)  

**Web Storage API**  - механизм п веб-приложениям хранить данные на клиентской стороне [cookie, sessionStorage localStorage](https://github.com/AntonGitCode/FEFAQ/tree/master/WebTech#webstorage)  
  
**History API** - DOM-объект Window предоставляет доступ к истории текущей сессии браузера через объект history - back frwd go() [читать](https://github.com/AntonGitCode/FEFAQ/blob/master/WebTech/README.md#historyApi)  


**ARIA** [читать](https://github.com/AntonGitCode/FEFAQ/blob/master/General/14.md)  
       
**6 принципов REST**: 
  - Клиент-серверная архитектура - - п добиться масштабируемости.
  - Stateless - сервер не хранит инфу о сессии клиента
  - Кэширование - сервер при след запросе клиента выдаст из кэша (идемпотентность)
  - Единообразие интерфейса - Hypermedia as the Engine of Application State - одно из ограничений REST- сервер возвращает не только ресурс, но и его связи с другими ресурсами и действия, которые можно с ним совершить.
  - Layered system - ни клиент, ни сервер не должны знать о том, как происходит цепочка вызовов дальше своих прямых соседей.
  - Code on demand - Идея передачи некоторого исполняемого кода от сервера клиенту.

**Critical Rendering**  

`Парсинг HTML и создание DOM`  
`DOM` - ответы в виде HTML превращаются в токены, которые в свою очередь превращаются в узлы и в последующем формируют DOM дерево.  
`CSSOM` - все данные о том как стилизовать DOM.  
`JavaScript` - загрузка всех скриптов.  
`Accessibility Tree` - при парсинге HTML, анализируются специальные атрибуты по типу role и aria.  
`Render Tree` - Соединение DOM и CSSOM.  
Layout/Reflow - это процесс определения размеров и позиций всех элементов на странице, а также их отношений друг к другу. Это происходит на основе CSS-правил и содержимого страницы.  
`Paint/Repaint` - это процесс рендеринга элементов на странице. Он включает в себя применение цветов, текстур, градиентов и других стилей к элементам.  
`Compositing` - это процесс объединения всех элементов на странице в одно изображение. Каждый элемент имеет свою прозрачность и слои, которые могут быть объединены в одно изображение для отображения на экране. Это происходит с помощью графического процессора  
  

<img src="https://github.com/AntonGitCode/FEFAQ/assets/117078390/3b9051ae-c74e-4aff-8979-fb766b8260c8" alt="Image Description" width="550">  

**Richardson** [Richardson](https://github.com/AntonGitCode/FEFAQ/blob/master/WebTech/README.md#richardson)
 
**PRPL** (**Push**, **Render**, **Pre-cache**, **Lazy-load**) - **это стратегия оптимизации загрузки веб-приложений**, особенно в контексте разработки Progressive Web Applications (PWA). Этот паттерн позволяет улучшить производительность загрузки страницы и сократить время отклика для пользователей.

PRPL п **шаги**:  
1. **Push** (предварительная загрузка): Загрузка наиболее критических ресурсов (например, HTML, CSS, JavaScript) в фоновом режиме, чтобы сократить время загрузки страницы.  
  
2. **Render** (рендеринг): Пользователю показывается минимальный набор контента, необходимый для начала отображения страницы. Это позволяет ускорить первоначальное отклика и создать ощущение быстрой загрузки страницы.  
  
3. **Pre-cache** (предзагрузка): Загрузка остальных ресурсов, которые понадобятся в дальнейшем, в фоновом режиме. Это позволяет кэшировать ресурсы для более быстрой загрузки при последующих запросах.  
  
4. **Lazy-load** (ленивая загрузка): Загрузка остальных ресурсов необходимых для отображения страницы по мере их фактического использования. Это позволяет снизить инициальную загрузку страницы и оптимизировать использование сетевых ресурсов.
  
Использование паттерна PRPL помогает создать более быстрые и отзывчивые веб-приложения, уменьшить размер загрузки страницы и улучшить опыт пользователя. 

**preload, prefetch, preconnect и prerender**  
  
- `preload` - говорит браузеру как можно скорее загрузить и кэшировать ресурс.
- `prefetch` - просит браузер загрузить и кэшировать ресурс (например, скрипт или таблицу стилей) в фоновом режиме. Загрузка происходит с низким приоритетом,
- поэтому не мешает более важным ресурсам.
- `preconnect` - просит браузер заранее подключиться к домену, когда вы хотите ускорить установку соединения в будущем.
- `prerender` - просит браузер загрузить URL-адрес и отобразить его на невидимой вкладке. Когда пользователь нажимает на ссылку, страница должна отобразиться немедленно.  prerender полезен для страниц, которые пользователи обычно посещают, таких как главная страница или страницы с популярным контентом

 
 <h2>GraphQL</h2>  

 **GraphQL** - это язык запросов для API, который позволяет **клиентским приложениям запрашивать только те данные, которые им нужны, и получать их в удобном формате.**   
  
GraphQL работает следующим образом:  
- Определение схемы: разработчик определяет схему, которая описывает типы данных и операции, которые могут быть выполнены.
- Создание запроса: клиентское приложение создает запрос, указывая необходимые данные и операции.
- Обработка запроса: сервер GraphQL обрабатывает запрос и возвращает только запрошенные данные.
- Обновление данных: если данные на сервере изменились, клиент может подписаться на определенные данные и получать уведомления об изменениях.  

**В GraphQL используется одна ссылка(эндпоинт) для всех запросов**. Всегда идет POST запрос, даже если мы просто хотим получить какие-то данные.  

GraphQL позволяет улучшить производительность и эффективность API, уменьшив количество запросов и объем передаваемых данных.  

mutations
query
overfetching
underfetching

## JS  

* [Вопросы по JavaScript](JavaScript/README.md)
* [Вопросы по тестированию](Testing/README.md)
* [Вопросы по производительности](Performance/README.md)
* [Вопросы по сетям](Network/README.md)
* [Примеры кода на JavaScript](Coding/README.md)
