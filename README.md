Беременность - критический период в жизни женщины, и мониторинг здоровья матери является важным для обеспечения благополучия как матери, так и нерожденного ребенка. Этот проект сосредоточен на использовании методов машинного обучения для прогнозирования уровня риска для беременных женщин на основе ключевых атрибутов здоровья. <br>
## Описание данных: <br>
### Age: 
Возраст в годах, когда женщина беременна <br>
### BodyTemp: 
Температура тела, измеряемая в фаренгейтах <br>
### SystolicBP:
Верхнее значение артериального давления в мм рт. ст., другой значимый атрибут во время беременности <br>
### DiastolicBP:
Нижнее значение артериального давления в мм рт. ст., другой значимый атрибут во время беременности <br>
### BS:
Уровень глюкозы в крови, измеряемый молярной концентрацией, ммоль/л <br>
### HeartRate:
Нормальная частота сердечных сокращений в минуту <br>
### Risk Level:
Предсказанный уровень риска во время беременности, учитывая предыдущие атрибуты <br>

## Ссылка на датасет
https://drive.google.com/file/d/1xnKnmAgaW7KsOcjwzGAjw7xB0cK4k_R7/view?usp=sharing

## Клонировать репозиторий
git clone https://github.com/Joktun/Pregnancy-Risk-Levels

## Команды для установки библиотек
pip install shap <br>
pip install catboost

## Список необходимых библиотек и их импорт
import pandas as pd <br>
import numpy as np <br>
import matplotlib.pyplot as plt <br>
import seaborn as sns <br>

from catboost import CatBoostClassifier <br>
from sklearn.metrics import confusion_matrix <br>
from sklearn.model_selection import train_test_split <br>
from sklearn.model_selection import GridSearchCV <br>
from sklearn.metrics import accuracy_score, f1_score  <br>
import shap
