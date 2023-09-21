Um aplicativo de página única carrega apenas um único documento HTML na primeira solicitação. Em seguida, ele atualiza parte do conteúdo ou corpo específico da página da web que precisa ser atualizado usando [[JavaScript]].

Esse padrão é conhecido como roteamento do lado do cliente porque o cliente não precisa recarregar a página inteira para obter uma nova página cada vez que um usuário faz uma nova requisição. Em vez disso, o é interceptada a requisição e altera as seções que precisam ser alteradas, sem precisar acionar o carregamento completo da página. Essa abordagem resulta em melhor desempenho e uma experiência de usuário mais dinâmica.

![[Pasted image 20230910111523.png]]