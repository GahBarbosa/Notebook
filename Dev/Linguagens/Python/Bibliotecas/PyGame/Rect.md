[[PyGame]] usa objetos Rect para armazenar e manipular áreas retangulares. Um Rect pode ser criado a partir de uma [[Surface]] que é combinação de valores de **esquerda**, **superior**, **largura** e **altura**.
```python
Rect(left, top, width, height)
```
Rects também podem ser criados a partir de objetos [[Python]] que já são um Rect ou possuem um atributo chamado "rect".
```python
self.image = pygame.Surface((32,64))
self.rect = self.image.get_rect(topleft = (x,y))
```
Qualquer função [[PyGame]] que requer um argumento Rect também aceita qualquer um desses valores para construir um Rect. 

As funções Rect que alteram a posição ou o tamanho de um Rect retornam uma nova cópia do Rect com as alterações afetadas. O Rect original não é modificado. Alguns métodos têm uma versão [[InPlace]] alternativa que retorna *None*, mas afeta o Rect original. 