# Датасет эмотивной разметки from_RNC_with_love

В создании датасета использовались материалы корпуса [Русской классики НКРЯ](https://ruscorpora.ru/search?search=CgQyAggV). Датасет включает в себя 2716 примеров реплик, ярко выражающих одну из следующих эмоций:

- neutral
- joy
- surprise
- fear
- sadness
- disgust
- anger

Распределение классов в датасете: [img](classes_distribution.jpg)

Датасет состоит из следующих колонок:

- id_replic (int): id реплики
- replic (str): реплика без прямой речи
- html_text (str): реплика с прямой речью, речь автора <i>в тэге</i>
- sentiment (str): эмотивный класс

На материале датасета и на базе [этой модели](https://huggingface.co/cointegrated/rubert-tiny2-cedr-emotion-detection) была дообучена multiclass classification модель. (Ссылка на huggingface)[https://huggingface.co/kplro/rubert-tiny2-cedr-rnc-emotion-detection]. Процесс дообучения представлен в emotive_detection_model.ipynb


