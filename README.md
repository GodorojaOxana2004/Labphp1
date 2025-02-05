# Лабораторная работа N1 (Установка и настройка PHP + первая программа )

##  Цель работы
Целью данной лабораторной работы является установка и настройка среды разработки для работы с языком программирования PHP, а также создание первой программы на PHP.

###  **Способ 1: Установка PHP вручную**
(Данный способ я лично использовала)
1. Перейдите на официальный сайт PHP: [https://www.php.net/downloads](https://www.php.net/downloads).
2. Загрузите актуальную версию PHP для вашей операционной системы.
3. Распакуйте архив в удобное место, например: `C:\Program Files\php`.
4. Добавьте путь к PHP в переменные среды (Path):
   - Откройте Параметры системы (Win + R → `sysdm.cpl`).
   - Перейдите в **Дополнительно** → **Переменные среды**.
   - В разделе **Системные переменные** выберите `Path` и добавьте путь `C:\Program Files\php`.
   - Сохраните изменения.
5. Проверьте установку, выполнив команду:
   ```
   php -v
   ```
   Если установка прошла успешно, в терминале отобразится версия PHP.

   ###  **Способ 2: Быстрая установка PHP через XAMPP**
1. Перейдите на сайт: [https://www.apachefriends.org](https://www.apachefriends.org).
2. Скачайте и установите **XAMPP**, выбрав компоненты:
   - Apache
   - PHP
   - phpMyAdmin
3. Запустите **XAMPP Control Panel** и включите `Apache`.
4. Проверьте работу сервера, открыв в браузере:
   ```
   http://localhost
   ```
   ## Написание первой программы на PHP

### 1 Создание проекта
1. Создайте директорию для проекта:
   ```
   mkdir D:\Projects\PHP\01_Introduction
   ```
Так же можно создать ее вручную без командной строки. В такое случае сначала переходи на диск D:
  ```
    C:\Users\User>D:
  ```
 И после прописываем место нахождения нужной нам папки:
  ```
    cd PHP\01_Introduction
  ```


   
3. Создайте файл **index.php** и откройте его в редакторе.

### 2 Напишите код:
```php
<?php
echo "Привет, мир!";
?>
```

### 3 Запуск программы
####  Способ 1: Встроенный веб-сервер PHP
```
php -S localhost:8000
```
Откройте [http://localhost:8000](http://localhost:8000) в браузере.

###  Работа с переменными и выводом данных
```php
<?php
$days = 288;
$message = "Все возвращаются на работу!";

// Вывод с конкатенацией
echo  $days . $message "<br>";

// Вывод с двойными кавычками
echo  "$days . $message<br>";

// Вывод с через print
print $days . $message "<br>";
print  "$days . $message "<br>";
?>
```

##  Контрольные вопросы

1. **Какие способы установки PHP существуют?**
   - Установка вручную с [php.net](https://www.php.net/downloads).
   - Установка с помощью XAMPP (Apache, PHP, phpMyAdmin).
   - Использование Docker или других контейнеров.

2. **Как проверить, что PHP установлен и работает?**
   - Ввести команду `php -v` в терминале.
   - Запустить `phpinfo();` в PHP-скрипте.
   - Проверить через `http://localhost` (если используется XAMPP).

3. **Чем отличается `echo` от `print`?**
   - `echo` может выводить несколько строк через запятую, `print` принимает только один аргумент.


