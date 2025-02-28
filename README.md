Проект представляет собой интеллектуальную рекомендательную систему, которая помогает пользователям открывать для себя новые фильмы на основе их предпочтений и популярности кинокартин. Система предлагает рекомендации, учитывая такие факторы, как жанры, рейтинги, популярность, описание фильмов и ключевые слова. <br>
| Параметры | Описание данных |
| --- | --- |
| id | Уникальный идентификатор фильма. (тип: int) |
| title | Название фильма. (тип: str) |
| vote_average | Средняя оценка фильма зрителями. (тип: float) |
| vote_count | Общее количество оценок фильма. (тип: int) |
| status | Статус фильма (например, "Выпущен", "В разработке", "Постпродакшн" и т.д.). (тип: str) |
| release_date | Дата выхода фильма. (тип: str) |
| revenue | Общий доход от фильма. (тип: int) |
| runtime | Продолжительность фильма в минутах. (тип: int) |
| adult | Указывает, предназначен ли фильм только для взрослой аудитории. |
| backdrop_path | URL фонового изображения фильма. (тип: str) |
| budget | Бюджет фильма. (тип: int) |
| homepage | URL официального сайта фильма. (тип: str) |
| imdb_id | IMDB ID фильма. (тип: str) |
| original_language | Язык оригинала, на котором снят фильм. (тип: str) |
| original_title | Оригинальное название фильма. (тип: str) |
| overview | Краткое описание сюжета фильма. (тип: str) |
| popularity | Популярность фильма (числовой показатель). (тип: float) |
| poster_path | URL постера фильма. (тип: str) |
| tagline | Слоган фильма. (тип: str) |
| genres | Список жанров фильма (в виде строки). (тип: str) |
| production_companies | Список кинокомпаний, участвовавших в производстве (в виде строки). (тип: str) |
| production_countries | Список стран-производителей (в виде строки). (тип: str) |
| spoken_languages | Список языков, на которых говорят в фильме (в виде строки). (тип: str) |
| keywords | Ключевые слова, связанные с фильмом (используйте .split(", ") для преобразования в список). (тип: str) |

## Ссылка на датасет
https://drive.google.com/file/d/1xnKnmAgaW7KsOcjwzGAjw7xB0cK4k_R7/view?usp=sharing

## Клонировать репозиторий
git clone https://github.com/Joktun/Film-Reccomendation-System

## Список необходимых библиотек и их импорт
%matplotlib inline <br>
import pandas as pd <br>
import numpy as np <br>
import matplotlib.pyplot as plt <br>
import seaborn as sns <br>
from scipy import stats <br>
from ast import literal_eval <br>
from sklearn.feature_extraction.text import TfidfVectorizer, CountVectorizer <br>
from sklearn.metrics.pairwise import linear_kernel, cosine_similarity <br>
from nltk.stem.snowball import SnowballStemmer <br> 
from nltk.stem.wordnet import WordNetLemmatizer <br>
from nltk.corpus import wordnet
