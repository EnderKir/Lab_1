# Lab_1

В первой лабораторной работе мы реализовали полносвязную нейронную сеть из 5 слоёв.
Сначала добавляем Flatten-слой, разворачивающий нашу матрицу изображений в одномерную для дальнейшего поступления на Dense-слой.
Dense: 2 слоя на 128 нейронов, еще 2 слоя на 64 нейрона и слой на 10 нейронов.

Функции активации relu, на выходе softmax.

В цикле обучения используются:
* оптимизатор 'adam'
* функция потерь 'sparse_categorical_crossentropy'
* метрика 'accuracy'

How does ReLU compare:
ReLU is linear (identity) for all positive values, and zero for all negative values. This means that:

- It’s cheap to compute as there is no complicated math. The model can therefore take less time to train or run.
- It converges faster. Linearity means that the slope doesn’t plateau, or “saturate,” when x gets large. It doesn’t have the vanishing gradient problem suffered by other activation functions like sigmoid or tanh.
- It’s sparsely activated. Since ReLU is zero for all negative inputs, it’s likely for any given unit to not activate at all. This is often desirable (see below).

Softmax function, a wonderful activation function that turns numbers aka logits into probabilities that sum to one. Softmax function outputs a vector that represents the probability distributions of a list of potential outcomes.

При обучении нейронной сети происходит за 50 эпох


Разреженная категориальная перекрестная энтропия /
sparse categorical crossentropy: 
![sparse](https://i.ibb.co/fYV0f5L/photo-2020-04-07-17-02-26.jpg)

loss: 1.4366 - acc: 0.4827 - val_loss: 1.5164 - val_acc: 0.4581

## Графики метрики точности и функции потерь:

![acc](https://i.ibb.co/Bjys3VJ/acc.jpg)

## Графики метрики точности и функции потерь на валидационной выборке:

![val_acc](https://i.ibb.co/hcwYYkS/val-acc.jpg)
