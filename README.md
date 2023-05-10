# supervised-learning-train

# Отток клиентов

Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых. Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Для этого предоставлены исторические данные о поведении клиентов и расторжении договоров с банком. Источник данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling

#### Признаки в данных:
- RowNumber — индекс строки в данных
- CustomerId — уникальный идентификатор клиента
- Surname — фамилия
- CreditScore — кредитный рейтинг
- Geography — страна проживания
- Gender — пол
- Age — возраст
- Tenure — сколько лет человек является клиентом банка
- Balance — баланс на счёте
- NumOfProducts — количество продуктов банка, используемых клиентом
- HasCrCard — наличие кредитной карты
- IsActiveMember — активность клиента
- EstimatedSalary — предполагаемая зарплата
#### Целевой признак:
- Exited — факт ухода клиента

Для проверки качества модели будет использоваться F1-мера. Цель - обучить модель, для которой на тестовой выборке эта метрика будет больше 0.59. 

Модели, используемые в этом проекте: логистическая регрессия, решающее дерево и случайный лес.

#### Результат применения моделей:
- получена модель с наибольшей точностью предсказания - случайный лес, лучшие гиперпараметры: `n_estimators = 7, max_depth = 8, min_samples_leaf = 2, min_samples_split = 2, class_weight = balanced`;
- решающее дерево показало F1-меру немного хуже, чем у леса;
- логистическая регрессия показала худшие результаты в обучении.