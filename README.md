# IT Purple Hack. Team Feature_88
Конкурсное решение хакатона IT Purple Hack. Кейс: Решение бизнес-задач, связанных с CLTV Альфа банк.
(Многоклассовая классификация)

Само решение в ноутбуке [it_purple_hack_alpha_ctb_final.ipynb](https://github.com/andrecpc/it-purple-hack-team-feature-88/blob/main/it_purple_hack_alpha_ctb_final.ipynb).
Для запуска необходимо наличие GPU.

Лучший скор на публичной части лидерборда 0.89544. Достигается за счет предикта с помощью catboost; файл submission_ctb.csv.

Суть решения:
 - Обучаем первый классификатор (catboost) восстанавливать start_cluster и восстанавливаем отсутствующие значения в тесте.
 - Обучаем второй классификатор (catboost) предсказывать end_cluster и делаем предикт для теста.
 - Уже на этом этапе можно делать посылку на LB.

 - Обучаем другую модель классификации end_cluster -- Нейронная сеть на PyTorch и так же предсказываем end_cluster в тесте.
 - Усредняем предсказания нейронки и катбуста.

![LB](2.png)

 Решение запускалось в [Colab](https://colab.research.google.com/drive/1nfYU9eckDmaV4wvuilXEsyQ8-evqk_3z?usp=sharing) и на [Kaggle](https://www.kaggle.com/pan4sf/it-purple-hack-alpha-ctb).

Скриншот лидерборда
![LB](1.png)
 
-----------------------------------------------
На всякий случай, по [ссылке](https://drive.google.com/drive/folders/1DeiQ6rKnhTbnNGWClalKXGHkwcNK4DLK?usp=sharing) выходные файлы нашего решения.
А еще если бы было чуть больше времени)) то обучили бы нейронку на большем числе эпох, и тогда бы вообще был космический скор)

[Видео](https://drive.google.com/file/d/1V42kgR0MGhnaZFI_Ya0AhqlZs2CMhQsj/view) с защиты (таймлайн 21:40). [Презентация](https://docs.google.com/presentation/d/1NkBGah6xDasyyRX3c_J2MUYU2bxOCbpK6kisyMSLhxg/edit#slide=id.g28f09fd3858_3_10).