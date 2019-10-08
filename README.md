# Лабораторные работы по дисциплине "Методы оптимизации" на факультете ПМИ, НГТУ
&nbsp;  
&nbsp;  

## 1. Методы одномерного поиска
### Условия задачи

Реализовать **методы дихотомии**, **золотого сечения**, исследовать их сходимость и провести сравнение по числу вычислений функции для 
достижения заданной точности 
![](https://latex.codecogs.com/svg.latex?%5Clarge%20%5Cvarepsilon)
от 
![](https://latex.codecogs.com/svg.latex?10%5E%7B-1%7D)
до 
![](https://latex.codecogs.com/svg.latex?10%5E%7B-7%7D).  

Построить график зависимости количества вычислений минимизируемой функции от десятичного логарифма задаваемой точности.  

Реализовать **алгоритм поиска интервала, содержащего минимум функции**. Реализовать **метод Фибоначчи**, сравнить его с **методами дихотомии** и **золотого сечения**.  

Задачу выполнять для функции: 
![](https://latex.codecogs.com/svg.latex?f%28x%29%20%3D%20%28x%20-%202%29%5E%7B2%7D%2C%20x%20%5Cin%20%5B-2%2C%2020%5D).  
&nbsp;  

## 2. Методы спуска (0-го, 1-го и 2-го порядка и переменной метрики)
### Условия задачи

Реализовать два метода поиска экстремума функции: **метод Розенброка**, **метод Бройдена**. Включить в реализуемый алгоритм собственную процедуру, реализующую одномерный поиск по направлению.  

С использованием разработанного программного обеспечения исследовать алгоритмы на квадратичной функции 
![](https://latex.codecogs.com/svg.latex?f%28%5Cbar%7Bx%7D%29%20%3D%20100%28x_%7B2%7D%20-%20x_%7B1%7D%29%5E%7B2%7D%20&plus;%20%281-x_%7B1%7D%29%5E%7B2%7D), 
функции Розенброка 
![](https://latex.codecogs.com/svg.latex?f%28%5Cbar%7Bx%7D%29%20%3D%20100%28x_%7B2%7D%20-%20x_%7B1%7D%5E%7B2%7D%29%5E%7B2%7D%20&plus;%20%281-x_%7B1%7D%29%5E%7B2%7D)
и на заданной в соответствии с вариантом тестовой функции, осуществляя спуск из различных исходных точек (не менее двух). Исследовать сходимость алгоритма, фиксируя точность определения минимума/максимума, количество итераций метода и количество вычислений функции в зависимости от задаваемой точности поиска. Результатом выполнения данного пункта должны быть выводы об объёме вычислений в зависимости от задаваемой точности и начального приближения. 

Построить траекторию спуска различных алгоритмов из одной и той же исходной точки с одинаковой точностью. В отчете наложить эту траекторию на рисунок с линиями равного уровня заданной функции. 

Результат работы должен содержать:
* таблицы с результатами проведенных исследований, где должны быть отражены начальное приближение 
![](https://latex.codecogs.com/gif.latex?%5Cbar%7Bx_%7B0%7D%7D), 
задаваемая точность по функции и переменным 
(![](https://latex.codecogs.com/svg.latex?%5Clarge%20%5Cvarepsilon)
от 
![](https://latex.codecogs.com/svg.latex?10%5E%7B-1%7D)
до 
![](https://latex.codecogs.com/svg.latex?10%5E%7B-7%7D)), 
количество итераций, число вычислений целевой функции, найденная точка и значение функции в ней.  
* для каждой целевой функции при точности поиска по переменным и функции 
![](https://latex.codecogs.com/svg.latex?%5Cvarepsilon%20%3D0.001)
и одной начальной точке составить следующую таблицу  

|  i  | (xi, yi)  | f(xi, yi) | (S1, S2) | lambda | xi - xi-1 | yi - yi-1 | fi - fi-1 | grad(f) | A |
|:---:|:---------:| :--------:|:--------:|:------:|:---------:|:---------:|:---------:|:-------:|:-:|
|  1  |           |           |          |        |           |           |           |         |   |
|  2  |           |           |          |        |           |           |           |         |   |
| ... |           |           |          |        |           |           |           |         |   |

&nbsp;  

## 3. Методы штрафных функций
### Условия задачи

Применяя методы поиска минимума 0-го порядка, реализовать программу для решения задачи нелинейного программирования с использованием **метода штрафных функций**.  

Исследовать сходимость **метода штрафных функций** в зависимости от:  
* выбора штрафных функций,  
* начальной величины коэффициента штрафа,  
* стратегии изменения коэффициента штрафа,  
* начальной точки,  
* задаваемой точности 
![](https://latex.codecogs.com/svg.latex?%5Cvarepsilon).  

Применяя методы поиска минимума 0-го порядка, реализовать программу для решения задачи нелинейного программирования с ограничением типа неравенства (**только пункт а**) с использованием **метода барьерных функций**.  

Исследовать сходимость **метода барьерных функций** (**только пункт а**) в зависимости от:   
* выбора барьерных функций,
* начальной величины коэффициента штрафа,
* стратегии изменения коэффициента штрафа,
* начального приближения,
* задаваемой точности 
![](https://latex.codecogs.com/svg.latex?%5Cvarepsilon).

Выполнить для функции: 
![](https://latex.codecogs.com/svg.latex?f%28x%2C%20y%29%20%3D%20%28x%20-%20y%29%5E2%20&plus;%2010%28x%20&plus;%205%29%5E2%20%5Crightarrow%20min)  
при ограничении:  
а) ![](https://latex.codecogs.com/gif.latex?x%20&plus;y%20%5Cgeq%200)  
б) ![](https://latex.codecogs.com/gif.latex?x%20%3D%201%20-%20y)  
&nbsp;  

## 4. Статистические методы поиска
### Условия задачи 
Разработать программу для решения задачи поиска глобального экстремума с использо-ванием метода простого случайного поиска и трех алгоритмов глобального поиска.

Исследовать метод простого случайного поиска глобального экстремума при различных 
![](https://latex.codecogs.com/svg.latex?%5Cvarepsilon)
и *P*. Результат представить в таблице:			

| ![](https://latex.codecogs.com/svg.latex?%5Cvarepsilon) | *P*  | *N* | *(x\*, y\*)* | *f(x\*, y\*)* |
|:-------------------------------------------------------:|:----:| :--:|:------------:|:-------------:|
|                                                         |      |     |              |               |

Исследовать алгоритмы поиска глобального экстремума. Сравнить результаты поиска по количеству вычислений функции и найденной точке экстремума. Исследование провести при различных значениях числа попыток *m*.

Найти максимум заданной функции:  
![](https://latex.codecogs.com/gif.latex?f%28x%2Cy%29%3D%5Csum_%7Bi%3D1%7D%5E%7Bn%7D%20%5Cfrac%7BC_%7Bi%7D%7D%7B1&plus;%28x%20-%20a_%7Bi%7D%29%5E%7B2%7D%20&plus;%20%28y%20-%20b_%7Bi%7D%29%5E%7B2%7D%7D)  
на области 
![](https://latex.codecogs.com/gif.latex?-10%5Cleq%20x%20%5Cleq%2010), 
![](https://latex.codecogs.com/gif.latex?-10%5Cleq%20y%20%5Cleq%2010).

### Перечень алгоритмов
1) **Простой случайный поиск**  
Пусть нам необходимо решить задачу минимизации функции **f(x)** на заданной области **D**.  
В заданной области по равномерному закону выбираем случайную точку **x1** и вычисляем в ней значение функции **y1 = f(x1)**. Затем выбираем таким же образом случайную точку **x2** и вычисляем **y2 = (x2)**. Запоминаем минимальное из этих значений и точку, в которой значение функции минимально. Далее генерируем новую точку. Делаем **N** экспериментов, после чего лучшую точку берем в качестве решения задачи (точку, в которой функция имеет минимальное значение среди всех “случайно” сгенерированных).  
Оценим число экспериментов, необходимое для определения решения (точки минимума) с заданной точностью в n-мерном прямоугольнике, **x ϵ [A, B]**. Пусть **n** - размерность вектора переменных. Объем n-мерного прямоугольника, в котором ведется поиск минимума, **V = П(Bi - Ai)**.    
Если необходимо найти решение с точностью **eps_i**, **i = 1..n**, по каждой из переменных, то мы должны попасть в окрестность оптимальной точки с объемом **V_eps = П(eps_i)**.  
Вероятность попадания в эту окрестность при одном испытании равна **P_eps = V_eps / V**. Вероятность непопадания равна **1 - P_eps**. Испытания независимы, поэтому вероятность непопадания за **N** экспериментов равна **(1 - P_eps)^N**.  
Вероятность того, что мы найдем решение за **N** испытаний: **P = 1 - (1 - P)^N**.  
Отсюда нетрудно получить оценку необходимого числа испытаний **N** для определения минимума с требуемой точностью: **N >= ln(1 - P) / ln(1 - P_eps)**.  

2) **Алгоритмы глобального поиска**  
    * **Алгоритм 1**. В допустимой области **D** случайным образом выбирают точку **x1 ϵ D**. Приняв эту точку за исходную и используя некоторый детерминированный метод или алгоритм направленного случайного поиска, осуществляется спуск в точку локального минимума **x1\* ϵ D**, в области притяжения которого оказалась точка **x1**.  
Затем выбирается новая случайная точка **x2 ϵ D** и по той же схеме осуществляется спуск в точку локального минимума **x2\* ϵ D**, и т.д.  
Поиск прекращается, как только некоторое заданное число **m** раз не удается найти точку локального экстремума со значением функции, меньшим предыдущих.  
&nbsp;  
    * **Алгоритм 2**. Пусть получена некоторая точка локального экстремума **x1\* ϵ D**. После этого переходим к *ненаправленному случайному поиску* до получения точки **x2** такой, что **f(x2) < f(x1\*)**.  
Из точки **x2** с помощью детерминированного алгоритма или направленного случайного поиска получаем точку локального экстремума **x2\***, в которой заведомо выполняется неравенство **f(x2\*) < f(x1\*)**.  
Далее с помощью случайного поиска определяем новую точку **x3**, для которой справедливо неравенство **f(x3) < f(x2\*)**, и снова спуск в точку локального экстремума **x3\***, и т.д.  
Поиск прекращается, если при генерации некоторого предельного числа новых случайных точек **m** не удается найти лучшей, чем предыдущий локальный экстремум, который тогда и принимается в качестве решения.  
&nbsp;  
    * **Алгоритм 3**. Пусть **x1** – некоторая исходная точка поиска в области **D**, из которой осуществляется спуск в точку локального экстремума **x1\*** со значением **f(x1\*)**. Далее из точки **x1\*** движемся либо в случайном направлении, либо в направлении **x1\* - x1** до тех пор, пока функция снова не станет убывать (выходим из области притяжения **x1\***).  
Полученная точка **x2** принимается за начало следующего спуска. В результате находим новый локальный экстремум **x2\*** со значением функции **f(x2\*)**.  
Если **f(x2\*) < f(x1\*)**, точка **x1\*** забывается и ее место занимает точка **x2\***. Если **f(x2\*) >= f(x1\*)**, то возвращаемся в точку **x1\*** и движемся из нее в новом случайном направлении.  
Процесс прекращается, если не удается найти лучший локальный минимум после заданного числа попыток **m** или не удается найти “случайного” направления, в котором функция снова начинает убывать.
Такой подход позволяет найти глобальный экстремум в случае многосвязных допустимых областей.
