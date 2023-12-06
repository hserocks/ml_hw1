# ml_hw1
В ходе работы был выполнен разведочный анализ данных. Была построена модель обычной линейной регрессии только на вещественных признаках, модели Lasso и ElasticNet тоже на вещественных признаках.

Для построения интерпретируемых моделей данные были сначала стандартизированы, а затем нормализованы.

1.Линейная регрессия показала достаточно большую ошибку на тест и трейн выборках (большую для стандартизированной выборки). А также значение r2 на тесте и трейне получилось на среднем уровне (0.63 и 0.59 соответсвенно).
2.Модель Лассо строилась на нормализованных данных, был подобран параметр альфа такой, что у модели остались не зануленные коэффициенты перед x-ми. Лассо в целом оказалось хуже по метрикам качества, по r2 для тестового набора данных он равен 0.35, что мало.
3.Модель ElasticNet тоже строилась на нормализванном наборе данных. Был также выполнен подбор параметров, но r2 для тестового набора данных оказался еще хуже ( равен 0.22)
4. Модель Ridge, где с использовались закодированные категориальные переменные показал наилучший результат.
MSE <0.001, r2 = 0.655, что можно считать наилучшим результатом среди всех предыдущих.

Таким образом можно сказать что наибольший буст в качестве дало использование дополнительных параметров (категориальных) а также использование Ridge модели
