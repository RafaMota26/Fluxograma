graph LR
    A(Recebimento) --> B{Estoque?}
    B -->|Sim| C[Picking]
    B -->|Não| D[Produzir]
    D --> C
    C --> E[Embalagem]
    E --> F[Rota]
    F --> G[Entrega]
    G --> H{Entregue?}
    H -->|Sim| I(Fim)
    H -->|Não| J[Reagendar]
    J --> G
