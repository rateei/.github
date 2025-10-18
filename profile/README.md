# Rateei 🛒

Sistema de rateios colaborativos para compras em lote, conectando comerciantes e compradores em grupos de compra.

## 📋 Sobre o Projeto

O **Rateei** é uma plataforma que facilita a organização de compras em grupo, permitindo que comerciantes criem rateios de itens em lote e compradores participem desses grupos para obter melhores preços e condições.

## 🎯 Funcionalidades Principais

### Para Comerciantes
- **Criação de Rateios**: Lance rateios de produtos em lote com preços especiais
- **Gestão de Grupos**: Controle sobre abertura e fechamento dos grupos de compra
- **Confirmação de Pagamentos**: Validação dos pagamentos recebidos
- **Controle de Retirada**: Gerenciamento da entrega individual dos produtos

### Para Compradores
- **Participação em Grupos**: Entre em rateios ativos de seu interesse
- **Pagamento Seguro**: Efetue pagamentos de forma segura na plataforma
- **Acompanhamento**: Monitore o status do seu rateio em tempo real
- **Retirada Individual**: Retire seus produtos após confirmação do comerciante

### Como Funciona

```mermaid
flowchart TD
    A[Cadastro do Vendedor CNPJ] --> B[Criação de Oferta e Rateio]
    
    B --> C1[Produto Retirada Imediata]
    B --> C2[Produto Precisa Preparo]
    
    C2 --> D[Vendedor marca Preparo Iniciado]
    D --> E[Preparo Concluído]
    E --> F[Usuários visualizam Oferta]
    
    C1 --> F
    
    F --> G[Usuário cria ou entra em Grupo]
    G --> H[Pagamento via Escrow]
    H --> I{Grupo atinge mínimo}
    
    I -->|Não| J[Aguarda]
    I -->|Sim| K[Grupo Fechado]
    
    K --> L[Janela de Cancelamento]
    L --> M[Retirada do Produto]
    
    M --> N1[Comprador Retira]
    M --> N2[Não Retira]
    
    N1 --> O1[Liberação de Pagamento]
    N2 --> O2[Pagamento Bloqueado até Prazo Final]
    
    O1 --> P[Concluído]
    O2 --> P
```

## 🚀 Começando

### Para Usuários

- **Vendedores:** Cadastre-se com CNPJ e comece a criar ofertas com rateio
- **Compradores:** Encontre ofertas, forme grupos e economize nas compras

## 🛡️ Segurança e Pagamentos

- Sistema de **escrow** para proteção de pagamentos
- Validação de CNPJ para vendedores
- Janela de cancelamento para proteção do consumidor
- Políticas de reembolso automatizadas

---

**Rateei** - Transformando a forma como economizamos
