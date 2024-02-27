# Онлайн калькулятор
### 1. Создал файл "CalcController.java" и добавил код для сложения и вычитания аргументов 
```java
package ru.neoflex.practice.controller;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class CalcController {
    @GetMapping("/plus/{a}/{b}")
    public Integer sumNumbers(@PathVariable("a") Integer a, @PathVariable("b") Integer b){
        return a+b;
    }

    @GetMapping("/minus/{a}/{b}")
    public Integer subtractNumbers(@PathVariable("a") Integer a, @PathVariable("b") Integer b){
        return a-b;
    }
}
```
Результат тестирования контроллера:  
![Тестирование суммы](https://github.com/Appollosxtcry/MyCalculate/blob/main/test_calc1.png?raw=true, "Тестирование суммы")
![Тестирование разности](https://github.com/Appollosxtcry/MyCalculate/blob/main/test_calc2.png?raw=true, "Тестирование разности")
### 2. Подключил Swagger, добавив в pom.xml необходимую зависимость
```java
<dependency>
    <groupId>org.springdoc</groupId>
    <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
    <version>2.0.4</version>
</dependency>
```
Интерфейс Swagger:  
![Контроллер суммы Рис.1](https://github.com/Appollosxtcry/MyCalculate/blob/main/swagger3.png?raw=true, "Контроллер суммы Рис.1")
![Контроллер суммы Рис.2](https://github.com/Appollosxtcry/MyCalculate/blob/main/swagger4.png?raw=true, "Контроллер суммы Рис.2")
![Контроллер разности Рис.1](https://github.com/Appollosxtcry/MyCalculate/blob/main/swagger5.jpg?raw=true, "Контроллер разности Рис.1")
![Контроллер разности Рис.2](https://github.com/Appollosxtcry/MyCalculate/blob/main/swagger6.jpg?raw=true, "Контроллер разности Рис.2") 
![Самый низ Рис.1](https://github.com/Appollosxtcry/MyCalculate/blob/main/swagger7.jpg?raw=true, "Самый низ Рис.1") 
