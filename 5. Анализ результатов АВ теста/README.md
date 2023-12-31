# Тема: Принятие решений в бизнесе
# Проект: Анализ крупного интернет-магазина. Проверка гипотез для увеличения выручки
#### Описание 
Вместе с отделом маркетинга мы подготовили список гипотез для увеличения выручки.
Наша задача — приоритизировать гипотезы, запустить A/B-тест и проанализировать результаты.

#### Используемые инструменты и методы:
* изучение общей информации о данных: display(), info()
* замена типов данных: pandas.to_datetime()
* обработка дубликатов: duplicated(), drop_duplicates()
* классификация: unique(), groupby(), nunique()
* анализ данных: pivot_table(), value_counts(), query(), sort_values(), numpy.percentile(), stats.mannwhitneyu()
* визуализация результатов: plot()

#### Краткий вывод
- Есть статистически значимое различие по среднему количеству заказов между группами и по «сырым», и по данным после фильтрации аномалий;
- Нет статистически значимого различия по среднему чеку между группами ни по «сырым», ни по данным после фильтрации аномалий;
- График различия среднего количества заказов между группами сообщает, что результаты группы B лучше группы A и нет значительной тенденции к ухудшению;
- График различия среднего чека говорит о том, что результаты группы B заметно улучшились в середине эксперимента, но на это сильно повлияли выбросы;
- Проблемы данных:
    1. Неодинаковый размер групп
    2. Часть посетителей попала в обе группы

Исходя из обнаруженных фактов, если не обращать внимание на проблемы в данных, то тест следует остановить и признать его успешным. Продолжать смысла нет, потому как вероятность, что при имеющихся данных сегмент B на самом деле хуже сегмента A — практически нулевая. Но с другой строны мы не можем точно знать, что результаты теста не были координально испорчены неправильным подбором групп. 

С учетом успеха группы В имеет смысл распространить эту практику на всех посетителей, это приведет к увеличению количества заказов и соответственно увеличит выручку.
