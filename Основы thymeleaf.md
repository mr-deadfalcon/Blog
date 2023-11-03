# Основый thymeleaf

С основном классе добавляем:  
`model.addAttribute("serverTime", dateFormat.format(new Date()));`

Вывод на странице:  
`Current time is <span th:text="${serverTime}" />`

