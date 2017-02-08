remote_sensing
==============

Содержатся файлы IPython Notebook, посвященные обрабоке ДЗЗ, и примеры данных, которые анализируются.

Запускать с использованием следующих ключей:

```
ipython2 notebook --script --pylab=inline 
```
slides
------
Каталог со слайдами презентаций и материалами для них



Данные:
-------

### Landsat

В каталоге data/Landsat лежат файлы с даными Landsat по некоторым точкам:

Номер точки| Координаты           | Категория точки | Название категории
-----------|----------------------|-----------------|---------
1          | 572677.37,7016668.9  | 1               | sphagnum bog
2          | 543260.77,7092610.5  | 1               | sphagnum bog
3          | 631319.81,7117411.6  | 1               | sphagnum bog
4          | 596653.87,7016474.2  | 2               | pine dwarf-schrubs-moss forest
5          | 629473.58,7008545.5  | 2               | pine dwarf-schrubs-moss forest
6          | 555870.52,7137658.6  | 2               | pine dwarf-schrubs-moss forest
7          | 632624.48,7140575.6  | 3               | pine lichen forest
8          | 569391.08,7041149.9  | 3               | pine lichen forest
9          | 542134.57,7010379.4  | 3               | pine lichen forest
10         | 581268.5,7029838.7   | 4               | black water
11         | 632599.86,7012853.4  | 4               | black water
12         | 607983.45,7129479.8  | 4               | black water


### MODIS

В каталоге data/MODIS лежат файлы с даными MODIS (MOD13) по некоторым точкам:

Номер точки| Координаты           		| Категория точки | Название категории
-----------|----------------------------|-----------------|---------
1          | 635020.857758,6672766.68594| 1     	      | Темная вода
2  		   | 628557.346378,6674488.5637	| 1				  | Темная вода
3		   | 627022.338203,6667836.86161| 1 			  | Темная вода
4		   | 638799.836006,6680917.9604	| 2				  | сосново-кустарничково-сфагновое олиготрофное болото (густой рям)
5		   | 631327.415767,6672295.79568| 2				  | сосново-кустарничково-сфагновое олиготрофное болото (густой рям)
6		   | 669583.556026,6675885.22365| 2				  | сосново-кустарничково-сфагновое олиготрофное болото (густой рям)
7		   | 631466.41992,6683975.7757	| 3				  | осоково-(C. rostrata) сфагновое мезоолиготрофное болото или олиготрофное пушицево-сфагновое болото
8		   | 639087.772819,6678711.77445| 3				  | осоково-(C. rostrata) сфагновое мезоолиготрофное болото или олиготрофное пушицево-сфагновое болото
9		   | 614413.193783,6669010.80609| 3				  | осоково-(C. rostrata) сфагновое мезоолиготрофное болото или олиготрофное пушицево-сфагновое болото
10		   | 635175.035749,6678916.10013| 4				  | Сосняки-зеленомошники
11		   | 630647.923211,6679094.80194| 4				  | Сосняки-зеленомошники
12		   | 626905.227527,6677146.57632| 4				  | Сосняки-зеленомошники




IPython Notebook:
-----------------

Основные статьи и модули:

1. Фильтрация данных NDVI от шумов (фильтр Savitzky-Golay): [NDVI filtering by Savitzky-Golay.ipynb](http://nbviewer.ipython.org/github/KolesovDmitry/remote_sensing/blob/master/NDVI%20filtering%20by%20Savitzky-Golay.ipynb)
2. Фильтрация данных NDVI от шумов (МНК и полиномы): [NDVI-LeastSquares.ipynb](http://nbviewer.ipython.org/github/KolesovDmitry/remote_sensing/blob/master/NDVI-LeastSquares.ipynb)
3. Классификация данных ДЗЗ на основе анализа временных рядов NDVI и преобразования Фурье:
  1. Теория и примеры [FFT_NDVI_Segmentation.ipynb](http://nbviewer.ipython.org/github/KolesovDmitry/remote_sensing/blob/master/FFT_NDVI_Segmentation.ipynb)
  2. Реализация:
    1. Разведочный анализ [FFT_NDVI_Segmentation_GRASS.ipynb](http://nbviewer.ipython.org/github/KolesovDmitry/remote_sensing/blob/master/FFT_NDVI_Segmentation_exploratory_analysis.ipynb)
    2. Кластеризация на основе коэффициентов разложения [FFT_NDVI_Segmentation_Unsupervised.ipynb](http://nbviewer.ipython.org/github/KolesovDmitry/remote_sensing/blob/master/FFT_NDVI_Segmentation_Unsupervised.ipynb)

Вспомогательные статьи и модули:

1. Инструменты (импорт данных ndvi из csv): [tools.ipynb](http://nbviewer.ipython.org/github/KolesovDmitry/remote_sensing/blob/master/tools.ipynb)
2. Инструменты работы с GRASS [FFT_NDVI_Segmentation_GRASS.ipynb](http://nbviewer.ipython.org/github/KolesovDmitry/remote_sensing/blob/master/FFT_NDVI_Segmentation_GRASS.ipynb)
