O módulo matemático que fornece classes de  [[Vetor]] de duas e três dimensões, Vector2 e Vector3, respectivamente.

as coordenadas de um Vector podem ser recuperadas da seguintes maneiras
```python
v = pygame.Vector3()

v.x = 5
v[1] = 2 * v.x
print(v[1]) # 10

v.x == v[0]
v.y == v[1]
v.z == v[2]

v = pygame.Vector2()
v.xy = 1, 2
v[:] = 1, 2
```

## Métodos 
##### Normalize
retorna um vetor com a mesma direção mas o comprimento de 1
