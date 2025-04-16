### 🧶 Dicionário de Dados – Banco de Dados da AMG Confecções

A **AMG Confecções** é uma fábrica têxtil especializada na produção de roupas em larga escala, atendendo clientes finais e empresas parceiras. Para apoiar suas operações, foi criado um banco de dados relacional robusto, que gerencia desde o cadastro de clientes e fornecedores até o controle detalhado de insumos e pedidos.

Este documento visa descrever a lógica usada na criação das tabelas, os relacionamentos entre elas e as regras de integridade adotadas para garantir a consistência dos dados.

---

### 🧍‍♂️ Tabela `cliente`

Essa tabela armazena os dados dos **clientes finais e empresas contratantes**. Cada cliente é identificado por um ID único e possui informações como nome, CPF ou CNPJ, e-mail, telefone e endereço.

- **Por que foi criada?** Para registrar quem realiza pedidos à fábrica.
    
- **Restrições:** O CPF/CNPJ e o e-mail são únicos, evitando duplicidades no cadastro.
    
- **Relacionamentos:** Um cliente pode fazer vários pedidos. Por isso, há uma relação com a tabela `pedido`, com `ON DELETE CASCADE`, garantindo que ao excluir um cliente, seus pedidos sejam também removidos automaticamente.
    

---

### 🏭 Tabela `fornecedor`

Essa tabela representa os **parceiros comerciais que fornecem insumos**, como tecidos, linhas e aviamentos.

- **Por que foi criada?** Para controlar a origem dos insumos usados na produção.
    
- **Campos importantes:** Nome fantasia, razão social, CNPJ, e-mail e endereço.
    
- **Relacionamentos:** Um fornecedor pode estar vinculado a vários insumos e produtos. Foi adotado `ON DELETE SET NULL`, pois caso um fornecedor seja excluído, os produtos e insumos devem ser mantidos para fins históricos.
    

---

### 🧵 Tabela `insumo`

Os insumos são os **materiais básicos utilizados na confecção**, como tecido de algodão, elástico, botão, etc.

- **Por que foi criada?** Para cadastrar os recursos utilizados na composição dos produtos.
    
- **Relacionamentos:** Cada insumo pode estar vinculado a um fornecedor (`id_fornecedor`) e pode compor diversos produtos (`produto_insumo`). A exclusão do fornecedor define `NULL` no insumo, e a exclusão do insumo impacta produtos com `ON DELETE CASCADE`.
    

---

### 👕 Tabela `produto`

Os produtos são os **itens finais confeccionados**, como camisetas, bermudas, calças ou uniformes.

- **Por que foi criada?** Para cadastrar o portfólio de produtos da fábrica, com preço, estoque e unidade de medida.
    
- **Relacionamentos:** Relaciona-se com insumos (via `produto_insumo`) e com pedidos (via `pedido_produto`). Ao excluir um produto, suas ligações com pedidos e insumos também são excluídas com `ON DELETE CASCADE`.
    

---

### 📦 Tabela `pedido`

Cada pedido representa uma **solicitação de produção ou compra feita por um cliente**.

- **Por que foi criada?** Para registrar os pedidos com data de entrega, valor total e status.
    
- **Campos com restrições:** O status é limitado a valores como 'Em andamento', 'Entregue', 'Cancelado', ou 'Aguardando pagamento', garantindo controle do processo de produção.
    
- **Relacionamentos:** Ligado diretamente ao cliente e aos produtos pedidos (`pedido_produto`), com `ON DELETE CASCADE` garantindo a limpeza automática de dados relacionados.
    

---

### 🧬 Tabela `produto_insumo`

Essa tabela realiza o mapeamento de quais insumos compõem um determinado produto, junto com as quantidades e o preço unitário do insumo na época.

- **Por que foi criada?** Para permitir a montagem e análise de fichas técnicas dos produtos.
    
- **Relacionamentos:** Relaciona-se com produto e insumo. Exclusões em qualquer lado resultam em exclusão em cascata, mantendo o banco consistente.
    

---

### 🛒 Tabela `pedido_produto`

Representa a lista de produtos em cada pedido, incluindo **quantidade e preço unitário acordado**.

- **Por que foi criada?** Para viabilizar pedidos com múltiplos produtos e detalhamento de venda.
    
- **Relacionamentos:** Cada entrada liga um pedido a um produto. Com `ON DELETE CASCADE`, pedidos e produtos apagados têm suas linhas relacionadas removidas automaticamente.
    

---

### 🔐 Regras de Integridade e Segurança

- **Chaves primárias** garantem unicidade em cada tabela.
    
- **Chaves estrangeiras** com `CASCADE` ou `SET NULL` mantêm a integridade referencial.
    
- **CHECK constraints** controlam valores lógicos como preços não negativos, quantidades maiores que zero, e status válidos.
    
- **UNIQUE** foi usado em dados sensíveis como e-mail, CPF/CNPJ, evitando duplicidade.
    

