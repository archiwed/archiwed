Olá, meu nome é André Duarte e sou estudante de Ciência da Computação na Universidade Federal Fluminense (UFF). Tenho habilidades intermediárias em Python e estou atualmente estudando Machine Learning e Deep Learning com Python e R. Além disso, possuo habilidades básicas em C, C++ e Bash, e sou um usuário avançado de Linux. Também tenho experiência com tecnologias como Jupyter Notebook, Miniconda, Docker e Kubernets. Estou sempre buscando novos desafios e oportunidades para crescer e desenvolver minhas habilidades como programador.

Hello, my name is André Duarte and I am a Computer Science student at the Federal Fluminense University (UFF). I have intermediate skills in Python and am currently studying Machine Learning and Deep Learning with Python and R. Additionally, I have basic skills in C, C++ and Bash, and am an advanced Linux user. I also have experience with technologies such as Jupyter Notebook, Miniconda, Docker and Kubernets. I am always seeking new challenges and opportunities to grow and develop my skills as a programmer.

```bash
kubectl exec -it profileandre -- /bin/bash
```


```python

#!/usr/bin/env python
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense

model = Sequential()
model.add(Dense(128, input_shape=(3,), name='nome'))
model.add(Dense(64, name='hobby'))
model.add(Dense(10, name='hobby_2'))

print('Modelo:')
model.summary()
```

```markdown

Modelo:
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
André Duarte (Dense)         (None, 128)               512       
_________________________________________________________________
I love Python (Dense)        (None, 64)                8256      
_________________________________________________________________
I love Keras (Dense)         (None, 10)                650       
=================================================================
Total params: 9,418
Trainable params: 9,418
Non-trainable params: 0
```

```python
model.fit(train_profileandre , epochs=50, validation_data=val_ds)
```
