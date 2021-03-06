# Отчёт о тестировании Java-кода для рассчета баланса счета клиента при пополнении

## Краткое описание

03.09.2020 - было проведено тестирование Java-кода для рассчета баланса счета клиента при пополнении

На тестирование затрачено: <0,2 часа>

## В результате тестирования выявлен неправильный рассчет итогового баланса клиента при пополнении счета
* [Bug-report #1](https://github.com/MFV72/homework2-1/issues/1#issue-692102009)

## Описание процесса тестирования

Для тестирования кода было использовано приложение IntelliJ IDEA.
В IntelliJ IDEA был создан новый проект и в этот проект был вставлен тестируемый Java-код.
При исполнении кода результат работы, выведенный в консоль не совпал с ожидаемым значением баланса.
Ожидаемое значение "2_500_000_000"
Фактическое значение "-1794967296"

В качестве тестовых данных использовались:
* Текущий баланс счета (переменная Balance) - 2_000_000_000;
* Сумма пополнения (переменная transfer) - 500_000_000;
* тестируемый Java-код
```
public class main {
    public static void main(String[] args) {
        int balance = 2_000_000_000;
        int transfer = 500_000_000;
        int newBalance;
        newBalance = balance + transfer;
        System.out.println(newBalance);
    }
}
```


Тестирование производилось в следующем окружении:
* <Windows 7 Максимальная 64bit>
* <Java 11 (OpenJDK11), version "11.0.8" 2020-07-14>
* <IntelliJ IDEA 2020.2 (Community Edition) Build #IC-202.6397.94, built on July 27, 2020>