# aluguel_de_ferramentas
API de aluguel de ferramentas

Esta é uma plataforma de aluguel de itens de utilidade esporádica (como furadeiras, lavadoras de alta pressão, equipamentos de camping e ferramentas de jardinagem).
Como Funciona
Cadastro: Usuários cadastram ferramentas ou objetos que ficam parados em casa.
Busca: Quem precisa de um item para um uso único busca por geolocalização.
Reserva: O sistema agenda os dias de uso e calcula a taxa de aluguel e caução.
Avaliação: Ambas as partes avaliam a experiência e o estado do objeto na devolução.
Vantagens do Negócio
Economia compartilhada: 
Ajuda a reduzir o consumo desnecessário e o desperdício.
Renda extra: Donos de ferramentas ganham dinheiro com o que está parado.
Baixo custo inicial: O foco é apenas no desenvolvimento do marketplace digital.



Estrutura das Tabelas
Cada usuário cadastrado no sistema terá os seus dados divididos em duas entidades principais para garantir a organização e o histórico do sistema:  
  ┌────────────────────────┐                                         ┌────────────────────────┐
  │      1. USUÁRIOS       │                                         │   2. MEU_INVENTÁRIO    │
  ├────────────────────────┤                                         ├────────────────────────┤
  │ id_usuario (PK)        │────────────────────────────────────────<│ id_item (PK)           │
  │ nome, email, senha..   │                                         │ id_usuario (FK)        │
  └────────────────────────┘                                         │ nome_item, preco...    │
               │                                                     └────────────────────────┘
               │
               │                                                  ┌────────────────────────┐
               │                                                  │  3. MEUS_ALUGUEIS      │
               └────────────────────────<│├───────────────────────┤
                                                                  │ id_aluguel (PK)        │
                                                                  │ id_usuario (FK)        │
                                                                  │ id_item (FK), datas... │
                                                                  └────────────────────────┘
