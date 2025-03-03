# Самостоятельные учебные работы по теме "Машинное обучение"

---
###  Задание: Изучить применение модели логистической регрессии и метода опорных векторов в задаче бинарной классификации
Нужно решить задачу классификации физических лиц по уровню дохода. Целевая переменная – уровень дохода income, который принимает два значения <=50K и >50K, поэтому классификация бинарная. 
Задачу классификации нужно решить при помощи модели логистической регрессии и модели опорных векторов.
Этапы работы:  
1. Проведите первичный анализ:  
a) проверьте данные на пропуски. Удалите в случае обнаружения.  
(*) Предложите альтернативный способ работы с пропусками  
b) постройте 1-2 графика на выбор. Визуализация должна быть основана на исследуемых данных и быть полезной (из графика можно сделать вывод об особенностях датасета/класса/признака)  
c) преобразуйте категориальные признаки  
2. Обучите модели логистической регрессии и опорных векторов на обучающем множестве. Для тестового множества предскажите уровень дохода и сравните с истинным значением, посчитав точность предсказания моделей. Для этого используйте встроенную функцию score. Сформулируйте выводы по проделанной работе:  
a) кратко опишите какие преобразования были сделаны с данными.  
b) cравните точность двух моделей.  
c) напишите свое мнение, в полной ли мере модели справились с поставленной задачей.   
(*) Что по вашему мнению нужно сделать, чтобы улучшить результат?
### [Ссылка на ноутбук в GoogleColab](https://colab.research.google.com/drive/1nL_5lxEfw73GDLcV_-oRw0p75-ptnoVV?usp=sharing)
---
###  Задание: Изучить применение методов оптимизации для решения задачи классификации
Необходимо применить полученные знания в теории оптимизации и машинном обучении для реализации логистической регрессии.
Этапы работы:
  - Загрузите данные. Используйте датасет с ирисами. В данных оставьте только 2 класса: Iris Versicolor, Iris Virginica.
  - Самостоятельно реализуйте логистическую регрессию, без использования метода LogisticRegression из библиотеки. Можете использовать библиотеки pandas, numpy, math для реализации. Оформите в виде функции. *Оформите в виде класса с методами.
  - Реализуйте метод градиентного спуска. Обучите логистическую регрессию этим методом.
  - Выберете и посчитайте метрику качества. Метрика должна быть одинакова для всех пунктов домашнего задания. Для упрощения сравнения выберете только одну метрику.
  - Повторите для метода скользящего среднего (Root Mean Square Propagation, RMSProp).
  - Повторите для ускоренного по Нестерову метода адаптивной оценки моментов (Nesterov–accelerated Adaptive Moment Estimation, Nadam).
  - Сравните значение метрик для реализованных методов оптимизации. Можно оформить в виде таблицы вида |метод|метрика|время работы| (время работы опционально). Напишите вывод.
### [Ссылка на ноутбук в GoogleColab](https://colab.research.google.com/drive/19pL7UmYfirBJRaCdNtnxN-mZoujBriU5?usp=sharing)
---
###  Задание: Закрепить знания о математическом смысле метрик TPR, FPR. Изучить построение ROC-кривой, графика Precision-Recall
Решить задачу классификации при помощи обучения модели логистической регрессии. Целевая переменная — пол спортсмена. Качество модели оценивается путем подсчета метрик TPR, FPR и построения графиков ROC-кривой, Precision-Recall.
Этапы работы:
1. Преобразуйте данные:
  a. проверьте наличие пропущенных значений. Преобразуйте/удалите пропуски по необходимости;
  b. закодируйте категориальные переменные числовыми значениями по необходимости.
2. Разделите выборку на обучающее (80% данных) и тестовое (20% данных) подмножества.
3. Постройте ROC-кривую с помощью функции roc_curve из библиотеки sklearn.metrics.
4. Вычислите значение ROC-AUC метрики с помощью функции roc_auc_score из библиотеки sklearn.metrics.
5. Реализуйте подсчет метрик TPR, FPR «вручную», без использования готовых функций из библиотеки sklearn.
6. Постройте ROC-кривую с помощью вычисленных в п. 5 метрик. Объедините графики из п. 3 и п. 6 в один. Сравните, сделайте вывод.
7. Постройте график Precision-Recall, используя метрики, посчитанные в п. 5.
   
8.* Вычислите значение ROC-AUC метрики, используя метрики, посчитанные в п. 5.

9.* Сформулируйте выводы по проделанной работе:  
a) как по полученным графикам сделать вывод о качестве модели? Как вы оцениваете обученную модель исходя из подсчитанных метрик?  
b) *может ли ROC-кривая проходить ниже диагонали?  
### [Ссылка на ноутбук в GoogleColab](https://colab.research.google.com/drive/1EZTDDizuD9TtnuKWkIXbNraUTYdnY1r0?usp=sharing)
---
###  Задание: Применить на практике методы по оценке качества данных
Проведите очистку данных на примере датасета с информацией о пассажирах корабля Титаник. На полученных данных обучите модель классификации, с целевым признаком Survived (1 – пассажир выжил, 0 – погиб). Обучите модель на необработанных данных и посчитайте метрику качества. Проведите очистку данных. Обучите модель на данных после обработки, посчитайте метрику качества. Сравнить полученные результаты. Значение метрики должно улучшиться.
Этапы работы:
1. Удалите все пропущенные значения и категориальные переменные. Обучите модель. Выберете и посчитайте метрику качества.
2. Снова загрузите полные данные. Удалите признаки, которые логически не нужны для построения модели. Обоснуйте.
3. Проверьте данные на наличие пропущенных значений.  
  a) Посчитайте, какой процент данных будет потерян, если просто удалить пропуски.  
  b) Заполните пропуски: средним значением; константой; классом, указывающим на то, что значение было пропущено; случайным числом. Для разных признаков используйте подходящий метод. Можно не использовать все перечисленные методы.  
4. Категориальные переменные переведите в цифровые значения. Можно использовать pd.get_dummies, preprocessing.LabelEncoder. Старайтесь не использовать для этой задачи циклы.
5. Проверьте данные на наличие выбросов. Удалите выбросы, если считаете это целесообразным. Обоснуйте.  
6.* Постройте 1-2 графика на выбор. Визуализация должна быть основана на исследуемых данных и быть полезной (из графика можно сделать вывод об особенностях датасета/класса/признака)  
7.* Попробуйте математически преобразовать признак Age.  
8. Обучите ту же модель, что в п. 1 на преобразованных данных. Посчитайте ту же, что в п. 1 метрику.  
9. Сформулируйте выводы по проделанной работе.  
  a) Кратко опишите какие преобразования были сделаны и почему.  
  b) Сравните метрики моделей из п. 1 и п. 8.  
  c) Напишите свое мнение о целесообразности работы с данными при построении моделей машинного обучения.    
  (*) Нужно ли аналогичным образом исследовать и дополнять действительно большие данные?
### [Ссылка на ноутбук в GoogleColab](https://colab.research.google.com/drive/1Vw6m66wt1wQKqZUXtUz3pQQcVzQVOdJt?usp=sharing)
---
###  Задание: Изучить применение методов разведочного анализа данных (EDA) для улучшения качества работы моделей машинного обучения  
В домашнем задании нужно улучшить метрики RMSE, R2 модели линейной регрессии путем работы с данными, а именно проведения разведочного анализа данных. В качестве датасета загрузить данные о недвижимости Калифорнии из библиотеки sklearn.datasets. Целевая переменная – MedHouseVal.
Этапы работы:  
1. Проверьте данные на наличие пропусков. Удалите их в случае обнаружения.
2. Разделите выборку на обучающее и тестовое подмножества. 80% данных оставить на обучающее множество, 20% - на тестовое.
3. Постройте модель линейной регрессии. Вычислите метрики RMSE, R2 на обучающем и тестовом множестве.
4. Постройте график распределения целевой переменной. Сделайте вывод. Присутствуют ли в этом признаке выбросы?  
5. Посчитайте и выведите корреляционную матрицу. Убедитесь, что ячейки матрицы поделены на цветные категории, в ячейках указано числовое значение корреляции.  
a.) Сделайте выводы.  
b.) Удалите признаки на основании полученных значений, выводов.  
c.) Повторите п. 3, п. 4 на измененных данных.  
6. Исследуйте оставленные признаки на выбросы.  
a.) Удалите выбросы в случае обнаружения.  
b.) Повторите п. 3, п. 4 на измененных данных.  
7. Измените несколько признаков на выбор математически. Например, вычислите логарифм, возведите в квадрат, извлеките квадратный корень.  
a.) Повторите п. 3, п. 4 на измененных данных.  
8. Сформулируйте выводы по проделанной работе.  
a.) Кратко опишите какие преобразования были сделаны с данными.  
b.) Сравните метрики всех моделей. Желательно оформление в виде таблицы вида |модель|RMSE|R2|признаки, на которых проводилось обучение с указанием их преобразований|.  
c.) Напишите свое мнение, в полной ли мере модели справились с поставленной задачей.  
### [Ссылка на ноутбук в GoogleColab](https://colab.research.google.com/drive/1oeirvLuKRwuJhw5WR_WlGLOT-Vd6CDru?usp=sharing)
---
###  Задание: Изучить применение дерева решений в рамках задачи регрессии  
Нужно решить задачу регрессии. В качестве датасета необходимо взять данные о недвижимости Калифорнии из библиотеки sklearn.datasets.
Целевая переменная – MedHouseVal. На полученных данных построить модель регрессии и дерево решений.  
Этапы работы:  
1. Проведите первичный анализ.  
a.)Проверьте данные на пропуски. Удалите в случае обнаружения.  
b.)*Нормализуйте один из признаков.  
2. Разделите выборку на обучающее и тестовое подмножества. 80% данных оставить на обучающее множество, 20% - на тестовое.  
3. Обучите модель регрессии на обучающем множестве.  
4. Для тестового множества предскажите целевую переменную и сравните с истинным значением, посчитав точность предсказания модели.  
5. Обучите дерево решений на обучающем множестве.  
a.) Повторите п. 4 для полученной модели.  
b.) Визуализируйте часть дерева решений. Убедитесь, что график получился читабельным. Посмотрите примеры визуализации по ссылке.  
6. Оптимизируйте глубину дерева (max_depth). *Оптимизируйте ещё один параметр модели на выбор.  
a.) Повторите п. 3 для полученной модели.  
7. Сформулируйте выводы по проделанной работе.  
a.) Сравните точность двух моделей.  
b.) Напишите свое мнение, для каких задач предпочтительнее использовать обученные в работе модели? Какие у них есть плюсы и минусы?  
### [Ссылка на ноутбук в GoogleColab](https://colab.research.google.com/drive/10ipsK5lV_bHemZiehu-dVNKylKHkVw4L?usp=sharing)
---
###  Задание: Применить на практике базовые ансамблевые методы  
Нужно решить задачу классификации наличия болезни сердца у пациентов. Целевая переменная – наличие болезни сердца (HeartDisease), принимает значения 0 или 1 в зависимости от отсутствия или наличия болезни соответственно. 

Этапы работы:  
1. Подготовьте датасет к обучению моделей.  
a) Категориальные переменные переведите в цифровые значения. Можно использовать pd.get_dummies, preprocessing.LabelEncoder. Старайтесь не использовать для этой задачи циклы.  
b) *Постройте 1-2 графика на выбор. Визуализация должна быть основана на исследуемых данных и быть полезной (из графика можно сделать вывод об особенностях датасета/класса/признака).  
2. Разделите выборку на обучающее и тестовое подмножество. 80% данных оставить на обучающее множество, 20% на тестовое.  
3. Обучите дерево решений на обучающем множестве. Используйте следующие модели:  
a) tree.DecisionTreeClassifier  
b) ensemble.RandomForestClassifier  
4. Для тестового множества сделайте предсказание целевой переменной. Выведите метрики для каждой построенной модели с помощью metrics.classification_report.  
5. Выведите важность признаков, полученную после обучения модели из п. 4b в виде столбчатой диаграммы. Отсортируйте важность по убыванию.  
6. Обучите бэггинг над моделью из п. 3a. Используйте ensemble.BaggingClassifier.  
a) Повторите п. 4  
7. Обучите стекинг трех моделей: из п. 3a, п. 3b и svm.LinearSVC. Используйте ensemble.StackingClassifier.  
a) Повторите п. 4  
8. Сформулируйте выводы по проделанной работе.  
a) Сравните метрики построенных моделей.  
b) Напишите свое мнение, какая модель наилучшая и почему.  
### [Ссылка на ноутбук в GoogleColab](https://colab.research.google.com/drive/1JrDIvtHd8nzEf7K-yYdLdHLX0KjvJ65J?usp=sharing)
---
### Задание: Изучить применение методов по поиску выбросов в данных, попрактиковаться в обработке экстремальных значений.  
Нужно решить задачу классификации типа стекол. Целевая переменная – тип стекла «Type». Остальные признаки описывают химические элементы в составе материала. Датасет нужно исследовать на наличие выбросов, провести EDA.  
Этапы работы:  
1. Проведите первичный анализ.  
а) Проверьте количество записей для каждого класса. Сделайте вывод.  
2. Разделите выборку на обучающее и тестовое подмножество. 80% данных оставить на обучающее множество, 20% на тестовое.  
3. Обучите модель дерева решений RandomForestClassifier на обучающем множестве.  
4. Для тестового множества предскажите тип стекла и сравните с истинным значением, посчитав точность предсказания модели (accuracy).  
5. Обработайте выбросы в данных.  
а) Визуализируйте распределение значений для каждой переменной. Можно использовать функции sns.boxplot, sns.distplot. Есть ли признаки с нормальным распределением?  
b) Исследуйте признаки на выбросы несколькими способами.  
c) Удалите выбросы. *Посчитайте процент удаленных записей от общего числа записей для каждого класса.  
6. Повторите п. 3, п. 4.  
7. Сформулируйте выводы по проделанной работе.  
а) Кратко опишите, какие преобразования были сделаны с данными.  
b) Сравните точность двух моделей.  
c) Напишите свое мнение, нужно ли исследовать данные на выбросы, для чего это делается, плюсы и минусы подхода.
### [Ссылка на ноутбук в GoogleColab](https://colab.research.google.com/drive/1yHUKpqSQ2yAjGubv2Vm1Vz2lx6NbxTaE?usp=sharing)
---
### Задание: Изучить методы отбора признаков для эффективного обучения моделей машинного обучения.  
Нужно решить задачу классификации точек наиболее эффективно. Для этого в работе необходимо применить различные методы по отбору признаков. Отбор признаков предпочтительнее осуществлять основываясь на математическом аппарате, поэтому данные для этого задания будут сгенерированы, чтобы избежать признаков с физическим смыслом.
Этапы работы:

1. Сгенерируйте данные с помощью кода:  
from sklearn.datasets import make_classification  
x_data_generated, y_data_generated = make_classification(scale=1)  

2. Постройте модель логистической регрессии и оцените среднюю точность. Для этого используйте следующий код:  
cross_val_score(LogisticRegression(), x, y, scoring=‘accuracy’).mean()

3. Используйте статистические методы для отбора признаков:  
a) Выберите признаки на основе матрицы корреляции.  
b) Отсеките низковариативные признаки (VarianceThreshold).  
c) Повторите п. 2 на отобранных признаках в п. 3a, п. 3b.  

4. Осуществите отбор признаков на основе дисперсионного анализа:  
a) Выберите 5 лучших признаков с помощью скоринговой функции для классификации f_classif (SelectKBest(f_classif, k=5)).  
b) Повторите п. 2 на отобранных признаках.  

5. Отбор с использованием моделей:  
a) Реализуйте отбор признаков с помощью логистической регрессии. Отобранные признаки подайте далее на вход в саму логистическую регрессию (SelectFromModel). Используйте L1 регуляризацию.  
b) Реализуйте отбор признаков с помощью модели RandomForest и встроенного атрибута feature_impotance.  
c) Повторите п. 2 на отобранных признаках в п. 5a, п. 5b.  

6. Перебор признаков:  
a) SequentialFeatureSelector.  
b) Повторите п. 2 на отобранных признаках.  

7. Сформулируйте выводы по проделанной работе:  
a) Сделайте таблицу вида |способ выбора признаков|количество признаков|средняя точность модели|.
### [Ссылка на ноутбук в GoogleColab](https://colab.research.google.com/drive/1Q2GC-_jGj8d7YIsbyJK8mNncNNgLVhuq?usp=sharing)
---
### Задание: Изучить применение моделей кластеризации  
Нужно сократить число цветов в палитре изображения. Картинку для выполнения работы можно выбрать любую, главное условие – наличие на ней разных цветов, для того, чтобы результат работы моделей был заметен.
Для выполнения работы необходимо выделить кластеры в пространстве RGB, объекты соответствуют пикселям изображения. После выделения кластеров все пиксели, отнесенные в один кластер, заполняются одним цветом. Цвет – центроид соответствующего кластера.  
1. Реализуйте три модели кластеризации:  
a) KMeans. Рассмотрите число кластеров K = 2, 5, 10, 20.  
b) DBSCAN  
c) AgglomerativeClustering. Рассмотрите число кластеров K = 2, 5, 10, 20.  
2. Для каждой модели оцените потери от уменьшения цветов при помощи метрики SSIM.  
3. Сформулируйте выводы по проделанной работе.  
a) Какая модель показала лучший результат?
### [Ссылка на ноутбук в GoogleColab](https://colab.research.google.com/drive/18NNZd-jDhMv9wLMXQOATfNp_qCUr9QkS?usp=sharing)
---
### Задание: Применить на практике алгоритмы по автоматической оптимизации параметров моделей машинного обучения  
Нужно решить задачу классификации наличия болезни сердца у пациентов наиболее эффективно. Целевая переменная – наличие болезни сердца (HeartDisease). Она принимает значения 0 или 1 в зависимости от отсутствия или наличия болезни соответственно.  
Этапы работы:

1. Подготовьте датасет к обучению моделей:  
a) Категориальные переменные переведите в цифровые значения. Можно использовать pd.get_dummies, preprocessing.LabelEncoder. Старайтесь не использовать для этой задачи циклы.  
2. Разделите выборку на обучающее и тестовое подмножество. 80% данных оставить на обучающее множество, 20% на тестовое.  
3. Обучите модель логистической регрессии с параметрами по умолчанию.  
4. Подсчитайте основные метрики модели. Используйте следующие метрики и функцию:  
cross_validate(…, cv=10, scoring=[‘accuracy’,‘recall’,‘precision’,‘f1’])
5. Оптимизируйте 3-4 параметра модели:  
a) Используйте GridSearchCV.  
b) Используйте RandomizedSearchCV.  
c) *Добавьте в п. 6b 2-5 моделей классификации и вариации их параметров.  
d) Повторите п. 5 после каждого итогового изменения параметров.  
6. Сформулируйте выводы по проделанной работе:  
a) Сравните метрики построенных моделей.  
b) *Сравните с полученными результатами в задании по теме «Ансамблирование».
### [Ссылка на ноутбук в GoogleColab](https://colab.research.google.com/drive/1D_TOf0kwQ-BVimtBGRiSgQXI71izObLI?usp=sharing)
