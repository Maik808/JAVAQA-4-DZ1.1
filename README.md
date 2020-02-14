﻿# Отчёт о тестировании установки OpenJDK11 под Windows 10 64 bit

## Краткое описание

12 февраля 2020 было проведено Installation Testing  приложения OpenJDK11 под Windows 10 64 bit.

На тестирование затрачено: 30 минут.

В результате тестирования дефектов не выявлено.


## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты:
* Инструкция по установке OpenJDK11 под Windows.


Тестирование производилось в следующем окружении:
* Windows 10 Pro, 64 bit, Версия 1809, Сборка 17763.1039 
* Java  version "11.0.6" 2020-01-14
* В процессе тестирования использовался инсталятор
OpenJDK11U-jdk_x64_windows_hotspot_11.0.6_10.msi


# Отчёт о тестировании программы KeyValidator

## Краткое описание

12 февраля 2020г было проведено smoke test, пользовательское тестирование по позитивному и негативному сценарию  приложения KeyValidator.

На тестирование затрачено: 1 час.

На smoke test дефектов не выявлено приложение запускается и совместимо с Java 11

В результате тестирования выявлены следующие дефекты:
* При проверке валидных ключей:  
Ключ 80b427f8-92cd-3aae-ba04-3927fbe17c6  
Ожидаемый результат: OK  
Фактический результат: FAIL  
Ключ 387eedc6-12e9-3b32-9881-63b6b5e85317  
Ожидаемый результат: OK  
Фактический результат: FAIL  

* При проверке невалидных ключей:  
Ключ 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1  
Ожидаемый результат: FAIL  
Фактический результат: OK  

* При вводе некоректного значения (qwerty)  
Ожидаемый результат: Корректная обработка ошибки программой (Вывод сообщения).  
Фактический результат: Аварийное завершение программы.   

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты:
* Руководство использования KeyValidator


В качестве тестовых данных использовались данные из руководства использования KeyValidator:
Ключи для проверки
Валидные ключи:

* 8f05e6a7-70e9-33d7-bfe7-b19eae0d8998
* 80b427f8-92cd-3aae-ba04-3927fbe17c6
* b295bc63-9f03-3b4b-af80-969b39f8c262
* 387eedc6-12e9-3b32-9881-63b6b5e85317
* c19a8cf9-5c3a-37c5-b7f3-d16d38a0c180   
Невалидные ключи:

* 18252235-78e0-44a5-8720-556f0c7da17a
* e66075b6-ddad-445e-baf6-161b3289522b
* b6d53250-f07e-4352-a293-6102ddf7f1ca
* c2bc778a-1cb9-46c6-b435-0489649d2a42
* 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1


Тестирование производилось в следующем окружении:
* Windows 10 Pro, 64 bit, Версия 1809, Сборка 17763.1039 
* Java  version "11.0.6" 2020-01-14


