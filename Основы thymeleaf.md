# Основый thymeleaf

## Простой вывод строкового элемента.

С основном классе добавляем:  
`model.addAttribute("serverTime", dateFormat.format(new Date()));`

Вывод на странице:  
`Current time is <span th:text="${serverTime}" />`

## Вывод списка

В контроллере добавляем:
```
ArrayList<Book> books = new ArrayList<Book>();

books.add(new Book("Test book 1"));
books.add(new Book("Test book 2"));
books.add(new Book("Test book 3"));

model.addAttribute("books",books);
```

Вывод на странице (**таблица**):  
```
<tbody>
  <tr th:each="book: ${books}">
    <td th:text="${book.id}"></td>
    <td th:text="${book.name}"></td>
  </tr>
</tbody>
```
Вывод на странице (**список**):  
```
<ul th:each="book: ${books}">
  <li th:text="${book.name}"></li>
</ul>
```

