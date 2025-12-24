# Система учета книг в библиотеке
## Выполнила: Латынцева В.Р. 2 курс ИТ-8
<img width="1387" height="680" alt="главная страница" src="https://github.com/user-attachments/assets/97fcbe54-60ee-4179-a29c-5931fcb516e6" />
<img width="1389" height="678" alt="таблица" src="https://github.com/user-attachments/assets/2f186e46-0e49-4c02-9525-569f412ed168" />
Проект представляет из себя Spring Boot Web MVC приложение для автоматизации библиотечных процессов с 4 таблицами в БД.
## Функциональность
## Управление книгами
Просмотр каталога книг
Добавление новых книг
Редактирование информации о книгах
Удаление книг (с проверкой активных выдач)
Поиск по названию и автору
Проверка уникальности инвентарного номера
## Управление читателями
Регистрация новых читателей
Обновление данных читателей
Удаление читателей (с проверкой активных выдач)
Поиск по ФИО
Проверка уникальности номера читательского билета и телефона
## Управление библиотекарями
Добавление сотрудников библиотеки
Редактирование информации о библиотекарях
Удаление библиотекарей (с проверкой связанных выдач)
Поиск по ФИО
Проверка уникальности номера сотрудника
## Выдача и возврат книг
Оформление выдачи книг читателям
Отметка о возврате книг
Просмотр всех выдач
Фильтрация по статусу (активные, просроченные, возвращенные)
Поиск выдач по различным критериям
Установка сроков возврата 

## Структура проекта

```
library_system/
│
├── pom.xml                                 # Maven конфигурация
│
├── src/main/java/com/library/library_system/
│   ├── LibrarySystemApplication.java       # Главный класс приложения
│   │
│   ├── controller/                         # Контроллеры
│   │   ├── BookController.java             # Контроллер книг
│   │   ├── ReaderController.java           # Контроллер читателей
│   │   ├── LibrarianController.java        # Контроллер библиотекарей
│   │   ├── BookLoanController.java         # Контроллер выдач книг
│   │   └── MainController.java             # Главный контроллер
│   │
│   ├── entity/                             # Сущности JPA
│   │   ├── Book.java                       # Сущность книги
│   │   ├── Reader.java                     # Сущность читателя
│   │   ├── Librarian.java                  # Сущность библиотекаря
│   │   └── BookLoan.java                   # Сущность выдачи книги
│   │
│   ├── repository/                         # Репозитории Spring Data JPA
│   │   ├── BookRepository.java             # Репозиторий книг
│   │   ├── ReaderRepository.java           # Репозиторий читателей
│   │   ├── LibrarianRepository.java        # Репозиторий библиотекарей
│   │   └── BookLoanRepository.java         # Репозиторий выдач
│   │
│   └── service/                            # Сервисный слой
│       ├── BookService.java                # Сервис книг
│       ├── ReaderService.java              # Сервис читателей
│       ├── LibrarianService.java           # Сервис библиотекарей
│       └── BookLoanService.java            # Сервис выдач
│
├── src/main/resources/
│   ├── application.properties              # Конфигурация Spring Boot
│   │ 
│   │
│   ├── static/                             # Статические ресурсы
│   │  
│   │
│   └── templates/                          
│       ├── index.html                      
│       ├── dashboard.html                  
│       │
│       ├── books/                          
│       │   ├── list.html                  
│       │   └── form.html                  
│       │
│       ├── readers/                        
│       │   ├── list.html                   
│       │   └── form.html                   
│       │
│       ├── librarians/                    
│       │   ├── list.html                   
│       │   └── form.html                   
│       │
│       └── loans/                         
           ├── list.html                   
           └── form.html  
```
