# <font size = 5 color = #00FF00> <center>Project 3. EDA + Feature Engineering. Соревнование на Kaggle</center></font> 



##  <font color = #9ACD32> Содержание </font>

[1. Введение](https://github.com/DmitVasilev/Project_3_EDA#-1-%D0%B2%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-)   
[2. Описание задачи](https://github.com/DmitVasilev/Project_3_EDA#2-%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B7%D0%B0%D0%B4%D0%B0%D1%87%D0%B8)   
[3. Описание данных](https://github.com/DmitVasilev/Project_3_EDA#3-%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85)   
[4. Результат](https://github.com/DmitVasilev/Project_3_EDA#4-%D1%80%D0%B5%D0%B7%D1%83%D0%BB%D1%8C%D1%82%D0%B0%D1%82)                  
[5. Выводы](https://github.com/DmitVasilev/Project_3_EDA#5-%D0%B2%D1%8B%D0%B2%D0%BE%D0%B4%D1%8B)

### <font color = #9ACD32> 1. Введение </font>

 Решаем задачу для компании Booking. Одна из проблем компании — это нечестные отели, которые накручивают себе рейтинг. Одним из способов обнаружения таких отелей является построение модели, которая предсказывает рейтинг отеля. Если предсказания модели сильно отличаются от фактического результата, то, возможно, отель ведёт себя нечестно, и его стоит проверить.

 :arrow_up:[in table of contents](https://github.com/DmitVasilev/Project_3_EDA#-%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5-)  

###  <font color = #9ACD32>2. Описание задачи</font>

В качестве модели машинного обучения в проекте используеться алгоритм RandomForestRegressor, реализованный в библиотеке sklearn. Задача состоит в том, чтобы качественно подготовить данные для обучения модели. Требуется провести очистку данных, проектирование признаков и разведывательный анализ данных с целью  повысить точность модели машинного обучения. Кроме этого нужно принять участие в закрытом соревновании на платформе Kaggle.
Для оценки качества модели — точности прогнозов, сделанных моделью, — используеться метрика MAPE (mean absolute percentage error), средняя абсолютная процентная ошибка.

Критерии оценивания:

    Качество кода (соблюдение стандартов оформления PEP-8, комментирование кода, README к проекту). Оформление проекта на GitHub, GitLab, Kaggle.
    Очистка данных.
    Исследование данных (качество визуализации, наличие идей, гипотез, комментариев).
    Генерация признаков.
    Отбор признаков.
    Преобразование признаков.
    Качество решения: результат метрики MAPE.

:arrow_up:[in table of contents](https://github.com/DmitVasilev/Project_3_EDA#-%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5-)  

###  <font color = #9ACD32>3. Описание данных</font>

В проекте используется датасет, в котором содержатся сведения о 515 000 отзывов на отели Европы. Исходная версия датасета содержит 17 полей со следующей информацией:

    hotel_address — адрес отеля;
    review_date — дата, когда рецензент разместил соответствующий отзыв;
    average_score — средний балл отеля, рассчитанный на основе последнего комментария за последний год;
    hotel_name — название отеля;
    reviewer_nationality — страна рецензента;
    negative_review — отрицательный отзыв, который рецензент дал отелю;
    review_total_negative_word_counts — общее количество слов в отрицательном отзыв;
    positive_review — положительный отзыв, который рецензент дал отелю;
    review_total_positive_word_counts — общее количество слов в положительном отзыве.
    reviewer_score — оценка, которую рецензент поставил отелю на основе своего опыта;
    total_number_of_reviews_reviewer_has_given — количество отзывов, которые рецензенты дали в прошлом;
    total_number_of_reviews — общее количество действительных отзывов об отеле;
    tags — теги, которые рецензент дал отелю;
    days_since_review — количество дней между датой проверки и датой очистки;
    additional_number_of_scoring — есть также некоторые гости, которые просто поставили оценку сервису, но не оставили отзыв. Это число указывает, сколько там действительных оценок без проверки.
    lat — географическая широта отеля;
    lng — географическая долгота отеля.


:arrow_up:[in table of contents](https://github.com/DmitVasilev/Project_3_EDA#-%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5-)  





###  <font color = #9ACD32>4. Результат</font>

Ноутбук с решением на GitHub: [project-3-eda-kaggle.ipynb](https://github.com/DmitVasilev/Project_3_EDA/blob/master/project-3-eda-kaggle.ipynb).     
Для отображения интерактивных графиков решения на GitHub можно воспользоваться ссылкой [project-3-eda-kaggle.ipynb](https://nbviewer.org/github/DmitVasilev/Project_3_EDA/blob/dadf854e177a2fc1d24ec5b1c9184642dfcc03ff/project-3-eda-kaggle.ipynb).        
Ноутбук с решением на Kaggle: [Project-3-EDA](https://www.kaggle.com/code/dmitryva/project-3-eda).    

 
Обеспечить воспроизводимость кода поможет файл requirements.txt:           
для решения на GitHub: [requirements.txt](https://github.com/DmitVasilev/Project_3_EDA/blob/master/requirements.txt);                        
для решенияя на Kaggle:  [requirements_for_kaggle.txt](https://github.com/DmitVasilev/Project_3_EDA/blob/master/requirements_for_kaggle.txt).                     

:arrow_up:[in table of contents](https://github.com/DmitVasilev/Project_3_EDA#-%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5-)     


###  <font color = #9ACD32>5. Выводы</font>

В данном проекте была проведена работа по разведывательному анализу данных на примере датасета содержащего рейтинг отелей.
Было проведено восстановление пропущенных данных, генерация новых признаков с использованием исходных и внешних данных. Выполнено кодирование признаков и преобразование данных различными методами. Найдены признаки с высокой корреляцией, определена важность признаков с помощью стаистических тестов хи-квадрат и anova. Проведен отбор признаков по важности. Итоговый результат оценки предсказаний модели по метрике МАРЕ на Kaggle - 12.42939.    
:arrow_up:[in table of contents](https://github.com/DmitVasilev/Project_3_EDA#-%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5-)  