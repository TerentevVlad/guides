## JavaScript (для встроенного в Ruby on Rails фронтенда) :coffee:
  ![VANILLA JS](https://habr.com/share/publication/150594/7ce1d7a6e38e1ec47b4d7ad0e92069d2/?v=1)
  * В проекте используется код нативного JavaScript (без jQuery и frontend-фреймворков) и сторонние модули.
  * Кода должно быть минимум, он должен соответствовать стандарту ECMAScript 2019.
  * Мы НЕ пользуемся JavaScript в Slim, потому что код должен проходить через webpacker.
  * Названия переменные и модулей в camelCase. Они должны быть понятными (ясно говорить о содержимом).
  * К странице и объектам на ней обращаться через document.querySelector() с использованием data-attributes.
  * Так как используется один js файл на всех страницах - необходимо проверять присутствие используемых элементов в модулях, а также использовать замыкания вида () => {functionCall()}(), чтобы защитить работу всего кода.
  * Использовать, где возможно, нативные методы объектов.