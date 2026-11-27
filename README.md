# Sprint_3

Финальный проект третьего спринта — класс онлайн-кассы
`OnlineSalesRegisterCollector`.

Решение находится в файле `online_sales_register_collector.py`.
Требуется Python 3. Внешние зависимости не нужны.

Касса хранит товары чека, добавляет и удаляет позиции, рассчитывает
стоимость, скидку 10% при количестве товаров больше 10 и налоги
по ставкам из задания. Статические методы возвращают номер телефона
с префиксом `+7` и текущие дату и время покупки.

Выполнено также дополнительное задание `get_date_and_time`.

Пример использования:

```python
from online_sales_register_collector import OnlineSalesRegisterCollector

register = OnlineSalesRegisterCollector()
register.add_item_to_cheque('чипсы')
register.add_item_to_cheque('молоко')

print(register.name_items)
print(register.number_items)
print(register.check_amount())
print(register.total_tax())
print(register.get_telephone_number(9123456789))
print(register.get_date_and_time())
```

Проверка длины телефона следует из условия задания: исключение возникает,
если передано больше 10 символов. Более короткие целые числа условием
не запрещены. Значения других типов отклоняются.
