graph LR
  
    A(Início: Recebimento do Pedido) --> B{Produto em Estoque?}
    B -->|Sim| C[Separar Picking]
    B -->|Não| D[Comprar/Produzir]
    D --> C
    C --> E[Embalagem]
    E --> F[Planejar Rota]
    F --> G[Transporte e Entrega]
    G --> H{Entregue?}
    H -->|Sim| I(Fim: Confirmação)
    H -->|Não| J[Reagendar]
    J --> G
    
    %% Estilização para facilitar a leitura no GitHub
    style A fill:#f9f,stroke:#333,stroke-width:2px
    style I fill:#9f9,stroke:#333,stroke-width:2px
    style B fill:#fff4dd,stroke:#d4a017,stroke-width:2px
    style H fill:#fff4dd,stroke:#d4a017,stroke-width:2px

