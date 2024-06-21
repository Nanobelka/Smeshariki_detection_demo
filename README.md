# [Детекция героев мультсериала "Смешарики" на изображениях](https://smeshariki-detection.streamlit.app/)
[Веб-приложение](https://smeshariki-detection.streamlit.app/) на базе модели детекции объектов

---

### Постановка задачи

Необходимо определить, есть ли на изображении объекты, подлежащие лицензированию.


### Данные

Количество изображений в датасете: **978**.
![Распределение меток](https://github.com/Nanobelka/Smeshariki_detection_demo/blob/main/images/labels.png)


### Обучение модели

Модель: **yolov8m** из семейства YOLO.  
Данные для обучения, валидации, тестирования: **60%, 20%, 20%** от исходных данных соответственно.  
Количество эпох обучения: **40**.  
Количество классов: **11**.  
Названия классов: `Barash`, `Bibi`, `Ezhik`, `Karych`, `Kopatych`, `Krosh`, `Losiash`, `Nusha`, `Pandi`, `Pin`, `Sovunia`, `logo`.

![Лосс и метрики во время обучения](https://github.com/Nanobelka/Smeshariki_detection_demo/blob/main/images/results.png)


### Тестирование модели

Метрики на тестовых данных:

|   Class  | Images | Instances | Precision | Recall | mAP_50 | mAP_50-95 |
|:---------|--------|-----------|-----------|--------|:------:|----------:|
| all      | 196    | 453       | 0.951     | 0.913  | 0.953  | 0.843     |
| Barash   | 196    | 53        | 0.978     | 0.837  | 0.905  | 0.810     |
| Bibi     | 196    | 13        | 0.982     | 0.923  | 0.939  | 0.861     |
| Ezhik    | 196    | 62        | 0.962     | 0.952  | 0.978  | 0.880     |
| Karych   | 196    | 34        | 0.977     | 0.971  | 0.978  | 0.880     |
| Kopatych | 196    | 30        | 1.000     | 0.914  | 0.943  | 0.864     |
| Krosh    | 196    | 75        | 0.916     | 0.920  | 0.921  | 0.803     |
| Losiash  | 196    | 42        | 0.967     | 0.929  | 0.974  | 0.870     |
| Nusha    | 196    | 47        | 0.912     | 0.872  | 0.911  | 0.815     |
| Pandi    | 196    | 12        | 0.890     | 0.917  | 0.975  | 0.810     |
| Pin      | 196    | 28        | 1.000     | 0.941  | 0.995  | 0.827     |
| Sovunia  | 196    | 36        | 0.969     | 0.864  | 0.968  | 0.820     |
| logo     | 196    | 21        | 0.865     | 0.915  | 0.954  | 0.879     |

![Нормализованная Confusion Matrix](https://github.com/Nanobelka/Smeshariki_detection_demo/blob/main/images/confusion_matrix_normalized.png)

![Кривая F1~Confidence](https://github.com/Nanobelka/Smeshariki_detection_demo/blob/main/images/F1_curve.png)

![Кривая Precision~Confidence](https://github.com/Nanobelka/Smeshariki_detection_demo/blob/main/images/P_curve.png)

![Кривая Recall~Confidence](https://github.com/Nanobelka/Smeshariki_detection_demo/blob/main/images/R_curve.png)

![Кривая Precision~Recall](https://github.com/Nanobelka/Smeshariki_detection_demo/blob/main/images/PR_curve.png)
