# Отчёт о тестировании приложения BaseApp

## Краткое описание

25.08.2020 было проведено функциональное тестирование приложения BaseApp на предмет проверки корректности отображения баланса счета при пополнении.

На тестирование затрачено: 2 часа

В результате тестирования выявлен один дефект: https://github.com/chugad/javaqa-homework-2.1/issues/1.
## Описание процесса тестирования

В процессе тестирования артефакты не использовались, так как тестирование производилось методом граничных значений для разных значений баланса счета клиента. По окончании тестирования как артефакт можно выделить данный отчет о тестировании и выявленный дефект.

В качестве тестовых данных для проверки корректности отображения баланса счета клиента при пополнении вручную сгенерированы данные для суммы пополнения счета (cash_transfer), при условии что изначально на счете клиента была сумма (balance) 2 000 000 000 рублей. 
Пример:

* ```  ```                *Пустое поле без символов*
* ```0```                    *граничное значение*
* ```2 147 483 647```        *граничное значение*
* ```2 147 483 648```      *граничное значение*
* ```2 147 483 646```       *граничное значение*

Ожидаемый результат будет выглядеть следующим образом:
```
"C:\Program Files\AdoptOpenJDK\jdk-11.0.8.10-hotspot\bin\java.exe" -javaagent:C:\Users\chuga\AppData\Local\JetBrains\Toolbox\apps\IDEA-C\ch-0\202.6397.94\lib\idea_rt.jar=61660:C:\Users\chuga\AppData\Local\JetBrains\Toolbox\apps\IDEA-C\ch-0\202.6397.94\bin -Dfile.encoding=UTF-8 -classpath C:\Users\chuga\IdeaProjects\BaseApp\out\production\BaseApp Main
2500000000

Process finished with exit code 0
```
Тестирование производилось в следующем окружении:
* Устройство: Windows 10 x64
* Браузер: Яндекс.Браузер Версия 20.8.0.894 (64-bit)
