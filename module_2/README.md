# skillfactory_rds
Цель проекта: отследить влияние условий жизни учащихся в возрасте от 15 до 22 лет на их успеваемость по математике, чтобы на ранней стадии выявлять студентов, находящихся в группе риска.

Задача проекта: провести разведывательный анализ данных и составить отчёт по его результатам.

В датасете содержатся данные относящиеся к ученикам, такие как возраст, пол, состав семьи, образование и работа родителей, время проведенное с друзьями и в пути в школу. Всего в данных 29 столбцов, один из них оценка, и влияние всех остальных признаков на данный столбец и есть задача проекта.

Основные этапы работы: 
-проверка данных на пропуски;

-заполнение пропусков; -анализ по отдельности цифровых и не цифровых столбцов; 

-анализ корреляции признаков; 

-удаление из итоговых данных не коррелируемых признаков с переменной оценкой

В данных содержится много пустых значений, столбы Pstatus, paid, famsup содержат более 10% пропусков. Данные пропуски с помощью функции я решил заменить на наиболее часто встречающее значение.
Выбросы найдены только в столбцах famrel и Fedu проанализировав данные явно видно что допущены ошибки или опечатки, которые были исправлены. 
На теловой карте корреляции заметна сильна взаимосвязь между столбцами studytime, granular и studytime, так как про столюец studytime, granular нам ничего не известно, то можем его удалить.

По графикам видно что столбцы studytime, granularadress, Mjob, Fjob, higher и schoolsupе могут влиять на переменную score. Статистически значимые различия выявления для колонок sex, address, reason, higher, romantic. Составим из данных колонок датафрейм для дальнейшего анализа.
 Данный проект показался сложным, не в плане реализации и написания функций и кода а именно в составлени выводов. Не совсем понятно как по boxplot проводить анализ. Также не совсем понятна функция get_stat_dif 
