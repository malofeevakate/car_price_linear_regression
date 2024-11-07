Имеются данные о размещенных объявлениях о продаже подержанных автомобилей на август 2020. 
Однако есть объявления, в которых есть описание автомобиля, но не указана цена. Эти объявления без цены по набору признаков соответствуют генеральной совокупности (то есть это не систематическая ошибка в какой-то конкретной области: дорогих автомобилях, каком-то регионе размещения объявления). Необходимо на имеющихся данных научиться хотя бы с точностью до 1900 фунтов в среднем (а лучше меньше) предсказывать цену автомобиля, т.е. построить модель, которая будет предсказывать цену автомобиля по его характеристикам (оцениваем MAE):

## Описание данных: ## 
- model - модель автомобиля
- year - год производства
- transmission - тип трасмиссии (автомат/механика/полуавтомат)
- mileage - пробег в милях
- fuelType - используемый тип топлива
- tax - включенный в стоимость автомобиля налог
- mpg (miles per gallon) - сколько миль авто может проехать на 3,78 литрах топлива
- engineSize - объем двигателя
- car_maker - производитель

  ## Реализация: ##
  - Проведен EDA,  
  - Проеобразованы категориальные фичи (one_hot_encoding, mean_target_encoding, smoothed means),  
  - Оценено влияние предикторов на таргет,  
  - Удалены выбросы,  
  - Построены модели линейной регрессии для двух категорий объектов с разными параметрами (регуляризация, кодирование кат фичей) с MAE < 1500
