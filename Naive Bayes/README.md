# Лабораторная работа №2

## Задание на лабораторную работу.

Разработайте собственную реализацию байесовского классификатора и сравните её с классификаторами из SciKit-Learn: Gaussian Naive Bayes, Multinomial Naive Bayes, Complement Naive Bayes, Bernoulli Naive Bayes. При обучении классификаторов использовать набор данных, полученный при выполнении лабораторной работы 1.
Замерьте прозводительность классификаторов - время, затраченное на классификацию одного экземпляра данных (одна точка) - и сравните производительность разработанного вами классификатора с классификаторами SciKit-Learn. Замерьте точность классификаторов и сравните точность разработанного вами классификатора с классификаторами SciKit-Learn.

## Результаты, которые необходимо получить в итоге:
По завершению выполнения работы необходимо (первые 4 пункта обязательны для выполнения):
1. построить матрицы ошибок для каждого классификатора;
2. определить классификатор, имеющий наибольшую точность;
3. построить гистограммы производительности для всех классификаторов, разместив их на одном графике;
4. определить классификатор с наиболее стабильной производительностью. В качестве критерия стабильности использовать дисперсию времени, затраченного на классификацию одного экземпляра данных (одна точка);
5. *задание на дополнительные баллы:* найти более достоверный критерий оценки стабильности производительности и использовать его по аналогии с пунктом 4. Обосновать, почему он является более достоверным.

Соответствующие пункты задания (1-4 и 5, если выполнен) должны быть выведены в результате работы программы.

Документация байесовских классификаторов SciKit-Learn: https://scikit-learn.org/stable/modules/naive_bayes.html

## Матрица ошибок для каждого классификатора:

GaussianNB:

![gnb](https://github.com/nvnovitskiy/artificial-intelligence-and-machine-learning/blob/main/task2/images/gnb.png)

OwnNB:

![onb](https://github.com/nvnovitskiy/artificial-intelligence-and-machine-learning/blob/main/task2/images/onb.png)

MultinomialNB:

![mnb](https://github.com/nvnovitskiy/artificial-intelligence-and-machine-learning/blob/main/task2/images/mnb.png)

ComplementNB:

![сnb](https://github.com/nvnovitskiy/artificial-intelligence-and-machine-learning/blob/main/task2/images/cnb.png)

BernoulliNB:

![bnb](https://github.com/nvnovitskiy/artificial-intelligence-and-machine-learning/blob/main/task2/images/bnb.png)


## Точность классификаторов (лучшие OwnNB & GaussianNB):

|               |   Accuracy |
|:--------------|-----------:|
| GaussianNB    |    86.0309 |
| OwnNB         |    86.0309 |
| MultinomialNB |    51.3257 |
| ComplementNB  |    28.4923 |
| BernoulliNB   |    14.1274 |

## Гистограмма производительности классификаторов:

![hist](https://github.com/nvnovitskiy/artificial-intelligence-and-machine-learning/blob/main/task2/images/hist.png)


## Стабильность классификаторов (самый стабильный GaussianNB):

|    |   GaussianNB |   MultinomialNB |   ComplementNB |   BernoulliNB |   OwnNB |
|---:|-------------:|----------------:|---------------:|--------------:|--------:|
|  0 |   0.00305796 |     0.00227666  |    0.0015769   |   0.002141    | 3.99411 |
|  1 |   0.00187707 |     0.000941992 |    0.00072813  |   0.000884056 | 3.9992  |
|  2 |   0.00180721 |     0.000806093 |    0.000654936 |   0.000824928 | 4.01085 |
|  3 |   0.00182986 |     0.000729084 |    0.000651121 |   0.000829935 | 4.15459 |
|  4 |   0.00179005 |     0.000710964 |    0.000622988 |   0.000808001 | 4.01588 |
|  5 |   0.00175714 |     0.000674009 |    0.000622034 |   0.000818968 | 4.02801 |
|  6 |   0.00177002 |     0.000666857 |    0.000619888 |   0.000835657 | 4.01037 |

## График стабильности классификаторов в зависимости от времени:

![stability](https://github.com/nvnovitskiy/artificial-intelligence-and-machine-learning/blob/main/task2/images/stability.png)


