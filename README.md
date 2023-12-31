# English_scores

Просмотр фильмов на оригинальном языке - это популярный и действенный метод прокачаться при изучении иностранных языков. Важно выбрать фильм, который подходит студенту по уровню сложности, т.ч. студент понимал 50 - 70 % диалогов. Чтобы выполнить это условие, преподаватель должен посмотреть фильм и решить, какому уровню он соответствует. Однако это требует больших временных затрат.

Целью данного проекта является разработка ML решения для автоматического определения уровня сложности англоязычных фильмов по субтитрам.

В ходе работы были пройдены все основные этапы полноценного исследования:

- загрузка и ознакомление с данными,
- предварительная обработка,
- лемматизация,
- стемминг,
- оценка релевантности слов с помощью частотно-обратной частоты термина в документе,
- выбор и обучение модели,
- предсказание уровня английского языка для загружаемых субтитров.

Входные данные:

- Файл excel с указанием фильма и разметкой уровня языковой сложности.
- Субтитры к указанным в файле Excel.
- Папки с субтитрами, распределенные по разным уровням сложности.
(данная информация содержится в English_level.zip)

Вывод:
1. Мы загрузили данные для проекта определения уровня языка, изучили и обработали.
2. Провели лемматризацию и стемминг для нормализации слов в датасете.
3. Провели оценку слов с помощью частотно-обратной частоты термина в документе.
4. Для данного проекта был выбран новый инструмент `CatBoostClassifier()` в рамках задачи мультиклассификации, показывающий лучшие результаты по сравнению с ранее изученными. Наилучший показатель ключевой метрики качетва `F1` достиг `68%`, что позволило получить наиболее высоки результаты по каждой категории языка. Однако, по категории A1-A2 показатель F1 не дотягивает даже до значения 0.5. Поэтому, для улучшения качества модели, как область для развития проекта, мы видим возможность рассмотреть другие подходы для лемматизации, оценки релевантности слов, а также более глубокого анализа при чистке субтитров.
5. Было проведено итоговое тестирование на дополнительных данных с помощью инструмента pipeline.



