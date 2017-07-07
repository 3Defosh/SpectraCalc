# SpectraCalc
My program for calculating spectra's relative intensity of gold and silver in LIBS.

Python 2.7, IPython notebook.

Данный блокнот предназначен для расчета средней интенсивности определенного пика в наборе спектров ЛИЭС. 

Краткое описание работы:

1) Предварительная обработка - вырезание небольшого участка заданной ширины вокруг интересующего пика. Участок должен содержать 
интенсивный пик другого элемента.
2) Выравнивание базовой линии.
3) Нормировка участка - каждая точка проецируется на отрезок [0,1], где 0 - базовая линия, 1 - глобальный экстремум.
4) Перемножение отнормированных данных с исходными(с выровненной базовой линией) и поиск максимума на окрестности интересующего пикселя
5) Расчет статистики - на данный момент статистика не совсем правильная, возможно будет переделана.

Использование:

В одной директории с файлом блокнота требуется создать две папки - Program и Results. В первую папку следует класть файлы 
спектров, для которых необходимо рассчитать интенсивность. В самом блокноте указать границы интересующего участка и примерный 
пиксель интересующего пика. Запустить блокнот, после окончания работы результаты будут лежать в папке Results. 

Файл результатов имеет следующее строение: (название первого файла в папке Program) (интенсивность) (абсолютная погрешность)

Комментарий: исходный код грязный, статистика рассчитывается не совсем верно, пользоваться удобно только мне;) 
             Будет время и желание - исправлю и доработаю.
