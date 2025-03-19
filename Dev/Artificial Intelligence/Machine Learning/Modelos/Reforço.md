###  O que é:

- Um **agente** interage com um **ambiente** e aprende a **tomar decisões** baseado em **recompensas ou punições**.
- O objetivo é **maximizar a recompensa ao longo do tempo**.

### Exemplo:

- Um robô aprendendo a andar
- Um algoritmo jogando xadrez ou videogame
- Um sistema de recomendação que ajusta o que mostra com base na interação do usuário

### Exemplo com o ambiente CartPole do Gym
```python
import gym

# Criar o ambiente
env = gym.make('CartPole-v1')
observation = env.reset()

for _ in range(1000):
    env.render()
    # Escolhe ação aleatória (exemplo simplificado)
    action = env.action_space.sample()
    observation, reward, done, _, _ = env.step(action)

    if done:
        observation = env.reset()

env.close()
```