---
hide:
  - toc
---

## Introdução

Este documento apresenta as histórias de usuário do sistema **Sexto Andar**, uma plataforma para gerenciamento de imóveis que conecta usuários interessados em alugar ou comprar imóveis com proprietários que desejam disponibilizá-los.

O sistema possui três tipos de usuários principais: **Usuários Comuns** (interessados em imóveis), **Proprietários** (donos de imóveis) e **Administradores** (gestores da plataforma). Cada perfil possui funcionalidades específicas que atendem às suas necessidades no processo de locação e venda de imóveis.

As histórias foram organizadas por perfil de usuário para facilitar o entendimento dos requisitos funcionais e servir como base para o desenvolvimento do sistema.


### **Usuário Comum**

1. Como usuário, quero me cadastrar como "Usuário" para poder acessar imóveis, favoritar, agendar visitas e fazer propostas.
2. Como usuário, quero fazer login como "Usuário" para acessar minhas funcionalidades específicas.
3. Como usuário, quero editar meus dados pessoais (nome, celular, email, senha) para manter minhas informações atualizadas.
4. Como usuário, quero visualizar uma lista de imóveis disponíveis para encontrar opções que me interessem.
5. Como usuário, quero favoritar imóveis para salvá-los em minha lista de interesse.
6. Como usuário, quero **desfavoritar** imóveis que não me interessam mais.
7. Como usuário, quero visualizar meus imóveis favoritos e realizar ações rápidas (visita, proposta) sobre eles.
8. Como usuário, quero ver a **quantidade de imóveis favoritados** no meu perfil.
9. Como usuário, quero agendar visitas a imóveis informando a data desejada.
10. Como usuário, quero enviar propostas para imóveis informando o valor oferecido.
11. Como usuário, quero deslogar ou sair do sistema a qualquer momento.

### **Proprietário**

12. Como proprietário, quero me cadastrar como "Proprietário" para poder cadastrar e gerenciar meus imóveis.
13. Como proprietário, quero fazer login como "Proprietário" para acessar minhas funcionalidades específicas.
14. Como proprietário, quero editar meus dados pessoais (nome, celular, email, senha) para manter minhas informações atualizadas.
15. Como proprietário, quero cadastrar **casas** informando: endereço, tamanho, descrição, valor, tipo de venda (aluguel/venda), preço do terreno e se é casa única no terreno.
16. Como proprietário, quero cadastrar **apartamentos** informando: endereço, tamanho, descrição, valor, tipo de venda, preço do condomínio, área de convivência, andar e se permite pets.
17. Como proprietário, quero visualizar meus imóveis cadastrados para acompanhar meu portfólio.
18. Como proprietário, quero ver a **quantidade de imóveis cadastrados** no meu perfil.
19. Como proprietário, quero **remover imóveis** cadastrados quando necessário.
20. Como proprietário, quero visualizar **todas as propostas recebidas** para meus imóveis com detalhes do usuário interessado.
21. Como proprietário, quero visualizar **todas as visitas agendadas** para meus imóveis com detalhes do usuário interessado.
22. Como proprietário, quero ver o **status das visitas** (realizada ou não).
23. Como proprietário, quero deslogar ou sair do sistema a qualquer momento.

### **Administrador**

24. Como administrador, quero acessar o sistema sem necessidade de cadastro prévio.
25. Como administrador, quero visualizar **todos os usuários cadastrados** (com paginação de 15 em 15).
26. Como administrador, quero **editar dados** de qualquer usuário (nome, celular, email, senha).
27. Como administrador, quero **excluir contas** de usuários quando necessário.
28. Como administrador, quero visualizar **todos os proprietários cadastrados** (com paginação de 15 em 15).
29. Como administrador, quero **editar dados** de qualquer proprietário (nome, celular, email, senha).
30. Como administrador, quero **excluir contas** de proprietários quando necessário.
31. Como administrador, quero visualizar **todos os imóveis cadastrados** no sistema (com embaralhamento e paginação).
32. Como administrador, quero **excluir imóveis** cadastrados por proprietários quando necessário.
33. Como administrador, quero buscar usuários e proprietários **por email** para edição/exclusão.

### **Sistema e Funcionalidades Técnicas**

34. Como usuário do sistema, quero que os imóveis sejam exibidos com **filtros por tipo** (casa/apartamento) e **tipo de venda** (aluguel/venda).
35. Como usuário do sistema, quero que os imóveis sejam mostrados de forma **embaralhada** para variedade.
36. Como usuário do sistema, quero que as listas tenham **paginação** (15 itens por página) para melhor navegação.
37. Como usuário do sistema, quero ver **diferenciação entre aluguel e venda** nos valores dos imóveis.
38. Como usuário do sistema, quero que as **propostas e visitas tenham IDs únicos** para rastreamento.
39. Como proprietário, quero que o sistema **calcule automaticamente o valor total** dos imoveis com todas as taxas.
