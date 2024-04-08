Требовалось предсказать 7 типов дефектов стальных пластин по табличным данным (бинарная классификация с множеством выходов). 
Для проверки использовалась метрика ROC-AUC. Задача решалась двумя вариантами: с помощью XGBoost и LightGBM. 
Метод LightGBM не поддерживает классификацию с множеством выходов, поэтому строилась модель для каждого типа дефекта. Методом XGBoost строилась одна модель для всех дефектов. 
Для повышения точности использовалась предобработка фич, кроссвалидация и параллельное предсказание 5-ю моделями с нахождением среднего. Оба решения дали схожие результаты при тестировании.

Репозиторий был создан при участии в конкурсе [Steel Plate Defect Prediction](https://www.kaggle.com/competitions/playground-series-s4e2) на Kaggle.
