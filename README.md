Проект представляет собой интеллектуальную рекомендательную систему, которая помогает пользователям открывать для себя новые фильмы на основе их предпочтений и популярности кинокартин. Система предлагает рекомендации, учитывая такие факторы, как жанры, рейтинги, популярность, описание фильмов и ключевые слова. <br>
## Описание данных: <br>
* #### id <br>
Уникальный идентификатор фильма. (тип: int)
* #### title <br>
Название фильма. (тип: str)
* #### vote_average <br>
Средняя оценка фильма зрителями. (тип: float)
* #### vote_count <br>
Общее количество оценок фильма. (тип: int)
* #### status <br>
Статус фильма (например, "Выпущен", "В разработке", "Постпродакшн" и т.д.). (тип: str)
* #### release_date <br>
Дата выхода фильма. (тип: str)
* #### revenue <br>
Общий доход от фильма. (тип: int)
* #### runtime <br>
Продолжительность фильма в минутах. (тип: int)
* #### adult <br>
Указывает, предназначен ли фильм только для взрослой аудитории. (тип: bool)
* #### backdrop_path <br>
URL фонового изображения фильма. (тип: str)
* #### budget <br>
Бюджет фильма. (тип: int)
* #### homepage <br>
URL официального сайта фильма. (тип: str)
* #### imdb_id <br>
IMDB ID фильма. (тип: str)
* #### original_language <br>
Язык оригинала, на котором снят фильм. (тип: str)
* #### original_title <br>
Оригинальное название фильма. (тип: str)
* #### overview <br>
Краткое описание сюжета фильма. (тип: str)
* #### popularity <br>
Популярность фильма (числовой показатель). (тип: float)
* #### poster_path <br>
URL постера фильма. (тип: str)
* #### tagline <br>
Слоган фильма. (тип: str)
* #### genres <br>
Список жанров фильма (в виде строки). (тип: str)
* #### production_companies <br>
Список кинокомпаний, участвовавших в производстве (в виде строки). (тип: str)
* #### production_countries <br>
Список стран-производителей (в виде строки). (тип: str)
* #### spoken_languages <br>
Список языков, на которых говорят в фильме (в виде строки). (тип: str)
* #### keywords <br>
Ключевые слова, связанные с фильмом (используйте .split(", ") для преобразования в список). (тип: str)

## Ссылка на датасет
https://drive.google.com/file/d/1xnKnmAgaW7KsOcjwzGAjw7xB0cK4k_R7/view?usp=sharing

## Клонировать репозиторий
git clone https://github.com/Joktun/Film-Reccomendation-System

## Список необходимых библиотек и их импорт
%matplotlib inline
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy import stats
from ast import literal_eval
from sklearn.feature_extraction.text import TfidfVectorizer, CountVectorizer
from sklearn.metrics.pairwise import linear_kernel, cosine_similarity
from nltk.stem.snowball import SnowballStemmer
from nltk.stem.wordnet import WordNetLemmatizer
from nltk.corpus import wordnet
