# Задание №3: Services

## Требования:

1. Создать сервис `BooksService`, который будет возвращать книги с помощью метода `getBooks()`. Использовать этот сервис в компоненте `BooksListComponent` для доставки массива книг.
2. Создать сервис `CartService`, который должен содержать данные корзины магазина и управлять ее содержимым. Он будет доставлять список приобритенных книг в виде массива `CartItemComponent` в компонент `CartListComponent`. Кроме этого сервис должен содержать следующую информацию:  
    • `CartProduct` - о добавленных товарах в корзину;  
    • `totalQuantity` - общее количество товаров в корзине;  
    • `totalSum` - общую стоимость товаров в корзине;  
   Сервис должен предоставлять следующий функционал:  
    • `addBook()` - добавить товар в корзину с нужным колличеством;  
    • `removeBook()` - удалить указанный товар из корзины;  
    • `increaseQuantity()/decreaseQuantity()` - увеличить/уменьшить колличество указанного товара в корзине;
   • `removeAllBooks()` - очистить корзину;  
    • `updateCartData()` - пересчитать общее количество товароа и сумму после каждой операции, которая влияет на корзину;
3. Создайте сервис `LocalStorageService` _(core/services/local-storage.service.ts)_, который позволит работать
   с `window.localStorage` (как класс, `useClass`). Он должен предоставлять методы для:
   • установки значения: строки или объекта (`setItem()`)
   • получения значения: строки или объекта (`getItem()`)
   • удаления значения по ключу (`removeItem()`)
4. Создайте сервис `ConfigOptionsService` _(core/services/config-options.service.ts)_, который должен хранить объект настроек (id, login, email, ...). Сервис должен предоставлять методы для установки и извлечения данных. Метод установки на вход принимает объект, а метод извлечения данных возвращает объект. Предусмотреть возможность установки подмножества свойств. Например, { id, login }.

### Дополнительное задание

1. Создайте сервис `ConstantsService` _(core/services/constant.service.ts)_, в виде готового литерала объекта, например _{ App: "TaskManager", Ver: "1.0" }_. Зарегистрируйте его, используя `useValue`.
2. Создайте сервис `GeneratorService` _(core/services/generator.ts)_, который должен генерировать случайную последовательность символов длины n из набора _a-z, A-Z, 0-9_. Создайте функцию `GeneratorFactory(n: number)`, которая будет предоставлять сгенеренную строку, используя `GeneratorService`. Зарегистрируйте `GeneratorFactory` используя `useFactory`.
3. Создайте демо-компонент `AboutComponent` _(layout/components/about.component.ts)_ и внедрите перечисленные выше сервисы. Используйте декоратор `@Optional()`.

## Оценка

Максимальная оценка - **100** баллов
