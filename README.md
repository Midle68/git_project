# Проект "обучение с учителем"

Отток клиентов

    Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.
    Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Вам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.
    Постройте модель с предельно большим значением F1-меры. Чтобы сдать проект успешно, нужно довести метрику до 0.59. Проверьте F1-меру на тестовой выборке самостоятельно.
    Дополнительно измеряйте AUC-ROC, сравнивайте её значение с F1-мерой.
    Источник данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling
  
<b>Введение:</b>
Предоставлена база данных с клиентами банка и различными данными о них. Целью данного проекта является выявление наиболее подходящей модели машинного обучения, которая бы наилучшим образом предсказала, уйдет клиент из банка в ближайшее время или же останется.

Задачами проекта (а соответственно и его план) являются:

1. Подготовка данных;
2. Исследование задачи (рассмотрение моделей без учета дисбаланса классов);
3. Борьба с дисбалансом (применение методов с целью устранения дисбаланса класса и рассмотрение показателя f1_score);
4. Тестирование моделей (на тестовой уже выборке).

По ходу проекта были рассмотрены следующие модели:
- DecisionTreeClassifier;
- RandomForestClassifier;
- LogisticRegression.

<b>Вывод:</b>
Единственная модель, которая на тестовой выборке продемонстрировала данный результат - это RandomForestClassifier со следующими параметрами: максимальная глубина дерева - 10, количество деревьев - 200. В дополнение к этому используется метод увеличения выборки (upsampling) для лучшего обучения модели на тренировочной выборке. Используя упомянутые параметры, модель достигла значения метрики f1_score в 0.627, а auc_roc = 0.77 (к слову чем ближе auc_roc к единице, тем лучше модель). 

