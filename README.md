Olá, meu nome é André Duarte e sou estudante de Ciência da Computação na Universidade Federal Fluminense (UFF). Tenho habilidades intermediárias em Python e R.  Atualmente estudando Machine Learning e Deep Learning com Python e R mais especificadamento com PyTorch e Keras. Além disso, possuo habilidades básicas em C, C++ e Bash, e sou um usuário avançado de Linux (Arch Linux btw). Também tenho experiência com tecnologias como Git, Hugging Face, Docker e Kubernets. Estou sempre buscando novos desafios e oportunidades para crescer e desenvolver minhas habilidades como programador.

Hello, my name is André Duarte and I'm a Computer Science student at Universidade Federal Fluminense (UFF). I have intermediate skills in Python and R. Currently, I'm studying Machine Learning and Deep Learning with Python and R, more specifically with PyTorch and Keras. Additionally, I have basic skills in C, C++, and Bash, and I'm an advanced Linux user (Arch Linux btw). I also have experience with technologies such as Git, Hugging Face, Docker, and Kubernetes. I'm always looking for new challenges and opportunities to grow and develop my skills as a programmer.

```python
import torch
import torch.nn as nn

class Model(nn.Module):
    def __init__(self):
        super(Model, self).__init__()
        self.fc1 = nn.Linear(3, 128)
        self.fc2 = nn.Linear(128, 64)
        self.fc3 = nn.Linear(64, 10)

    def forward(self, x):
        x = torch.relu(self.fc1(x))
        x = torch.relu(self.fc2(x))
        x = self.fc3(x)
        return x

model = Model()

print('Modelo:')
print(model)
```
```markdown
Modelo:
Model(
  (fc1): Linear(in_features=3, out_features=128, bias=True)
  (fc2): Linear(in_features=128, out_features=64, bias=True)
  (fc3): Linear(in_features=64, out_features=10, bias=True)
)

Resumo do modelo:
------------------------------------------------------------------------------------------
Layer (type:depth-idx)                   Output Shape              Param #
==========================================================================================
Model                                    --                        --
├─ I love Python: 1-1                       [1, 128]                  512
├─ I love Pytorch: 1-2                      [1, 64]                   8,256
├─ I love me: 1-3                           [1, 10]                   650
==========================================================================================
Total params: 9,418
Trainable params: 9,418
Non-trainable params: 0
------------------------------------------------------------------------------------------

```

```python
print('Resumo do modelo:')
summary = nn.Summary(model, input_size=(1, 3))
print(summary)

train_data =
val_data = 

optimizer = torch.optim.SGD(model.parameters(), lr=0.01)
loss_fn = nn.MSELoss()

for epoch in range(50):
    for inputs, targets in train_data:
        optimizer.zero_grad()
        outputs = model(inputs)
        loss = loss_fn(outputs, targets)
        loss.backward()
        optimizer.step()

    with torch.no_grad():
        for inputs, targets in val_data:
            outputs = model(inputs)
            val_loss = loss_fn(outputs, targets)

    print(f'Epoch {epoch+1}, Train Loss: {loss.item()}, Val Loss: {val_loss.item()}')
```
