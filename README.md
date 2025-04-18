# Вероятностная обработка коллизий

Данная работа посвящена вероятностной обработке коллизий между игровыми объектами. Для этой работы был создан датасет, содержащий 640 000 строк с информацией о коллизиях двух определенных объектов (BigShip и SmallShip). Для предсказания коллизий на основе данных были выбраны следующие алгоритмы:  
- **Логистическая регрессия**  
- **Метод K ближайших соседей (KNN)**  
- **Наивный Байес**  
- **Метод опорных векторов (SVC)**  

В процессе работы данные были разделены и отбалансированы. Модели были обучены после подбора гиперпараметров. Также были измерены скорость работы алгоритмов и использованные ресурсы.

---
# Сводная таблица результатов

| Алгоритм                | Fit Time | Predict Time | Memory After Run | Memory Peak | Accuracy | F1 Score (0) | F1 Score (1) |
|-------------------------|----------|--------------|------------------|-------------|----------|--------------|--------------|
| **KNN**                 | 1.5 s    | 1.6 s        | 82 MB            | 100 MB      | 0.99     | 1.00         | 0.90         |
| **Логистическая регрессия** | 1.5 s    | 1.6 s        | 82 MB            | 100 MB      | 0.51     | 0.66         | 0.09         |
| **Наивный Байес**       | 0.2 s    | <0.1 s       | 1 MB             | 36 MB       | 0.85     | 0.91         | 0.35         |
| **SVC**                 |223 m          |60 m              |                  |             |          |0.85              |0.85              |

---
# Итоги

Лучшую точность предсказания показали алгоритмы KNN и SVC. С другой стороны, алгоритм KNN потребовал для работы много памяти, а обучение и использование алгоритма SVC заняло очень много времени.
