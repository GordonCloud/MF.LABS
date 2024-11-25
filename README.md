# Задание №1. Реализация и исследование модели Хольта-Уинтерса

Цель работы: изучить прогнозирование временных рядов с использованием модели Хольтера-Уинтерса.

Задачи:
1. Реализовать модель Хольтера-Уинтерса на Python без использования специализированных библиотек.
2. Добавить возможность тюнинга гиперпараметров для получившейся реализации модели.
3. Испытать модель на синтетических данных, визуализировать результаты на графиках.
4. Применить модель на реальных данных. В качестве источника данных для работы взята статистика
среднемесячной номинальной начисленной заработной платы работников по полному кругу организаций
в целом по экономике Российской Федерации в 1999-2024гг по данным Росстата
(https://rosstat.gov.ru/labor_market_employment_salaries)

Описание модели:
Модель при инициализации принимает на вход следующие параметры:
series - данные (временной ряд)
season_length - длина сезона (по-умолчанию 12)
n_pred_seasons - количество сезонов прогнозирования (по-умолчанию 1)
mode ('normal' - режим с заданными параметрами alpha, beta, gamma, 'tuning' - режим с автоматическим подбором параметров сглаживания)
model_params - значения параметров сглаживания. Используется только в случае, если выбран режим 'normal'

Использование модели:
- **`fit`** возвращает сам объект модели после обучения, что позволяет использовать методы последовательного вызова.
- **`predict`** и **`fit_predict`** возвращают список прогнозных значений, которые можно использовать для дальнейшего анализа или визуализации.

# Скриншоты с визуализацией результатов применения модели на данных Росстата:
![image](https://github.com/user-attachments/assets/e171eb72-53f9-4675-82f9-eaf34567df72)
![image](https://github.com/user-attachments/assets/d39ac0da-63c1-4332-a7e0-1706adc2267b)
