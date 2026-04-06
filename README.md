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
