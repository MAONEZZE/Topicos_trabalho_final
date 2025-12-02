# 🛍️ Loja Online - React e Ant Design

Uma aplicação de e-commerce moderna construída com React, TypeScript, Ant Design e Tailwind CSS. Este projeto integra gerenciamento de produtos, gerenciamento de clientes e funcionalidades de carrinho de compras com um belo alternador de tema claro/escuro.

---

## ✨ Recursos

### 🏠 Página Inicial (HomePage)
- Exibe os 5 principais produtos da Fake Store API
- Cards de produtos responsivos com imagens e preços
- Navegação rápida para detalhes do produto

### 🛒 Página de Produtos
- Listagem completa de produtos com funcionalidade de busca
- Adicionar, editar e excluir produtos
- Cadastro de produto com validação de formulário
- Integração com carrinho de compras (Botão "Comprar")
- Persistência de dados usando LocalStorage
- Drawer (painel lateral) de edição para atualizar detalhes do produto
- Confirmação de exclusão com Popconfirm

### 👥 Página de Clientes
- Listagem de clientes com visualização em tabela
- Adicionar novos clientes via modal
- Editar clientes existentes com drawer
- Excluir clientes com confirmação
- Persistência no LocalStorage
- Validação de formulário

### 🛒 Carrinho de Compras
- Adicionar/remover produtos
- Visualizar quantidade e preço total
- Funcionalidade de limpar carrinho
- Processo de checkout com confirmação
- Dados do carrinho persistentes (LocalStorage)
- Badge no carrinho mostrando a contagem de itens

### 🎨 Suporte a Temas
- Alternância entre modo claro e escuro
- Tematização consistente em todas as páginas
- Integração Ant Design com tokens de tema personalizados
- Transições de tema suaves

---

## 🚀 Tecnologias

- **React 18** - Biblioteca de UI
- **TypeScript** - Segurança de tipos (Type safety)
- **Vite** - Ferramenta de build e servidor de desenvolvimento
- **Ant Design** - Biblioteca de componentes de UI
- **Tailwind CSS** - Framework CSS utility-first
- **shadcn/ui** - Componentes de UI adicionais
- **React Router** - Roteamento client-side
- **React Context API** - Gerenciamento de estado (Carrinho)
- **LocalStorage** - Persistência de dados
- **Fake Store API** - Fonte de dados de produtos

---

## 🏁 Começando

### Pré-requisitos

- Node.js (v16 ou superior)
- Gerenciador de pacotes npm ou yarn

### Instalação

1. **Clone o repositório**
   ```bash
   git clone [https://github.com/MAONEZZE/Topicos_trabalho_final.git](https://github.com/MAONEZZE/Topicos_trabalho_final.git)
   cd Topicos_trabalho_final
   ```

2. **Instale as dependências**
   ```bash
   npm install
   ```

3. **Inicie o servidor de desenvolvimento**
   ```bash
   npm run dev
   ```

4. **Abra seu navegador**
   ```
   Navegue para: http://localhost:8080
   ```

### Build para Produção

```bash
npm run build
```

Os arquivos prontos para produção estarão na pasta `dist`.

### Pré-visualizar Build de Produção

```bash
npm run preview
```

---

## 📁 Estrutura do Projeto

```
src/
├── components/
│   ├── Header.tsx              # Cabeçalho de navegação com carrinho e alternador de tema
│   ├── ProductCard.tsx         # Componente de card de produto reutilizável
│   └── ui/                     # Componentes shadcn/ui
├── contexts/
│   └── CartContext.tsx         # Gerenciamento de estado do carrinho de compras
├── pages/
│   ├── Index.tsx               # Página inicial (top 5 produtos)
│   ├── Products.tsx            # Página de gerenciamento de produtos
│   ├── Clients.tsx             # Página de gerenciamento de clientes
│   ├── Cart.tsx                # Página do carrinho de compras
│   ├── Account.tsx             # Página de conta do usuário
│   └── NotFound.tsx            # Página 404
├── lib/
│   └── utils.ts                # Funções utilitárias
├── App.tsx                     # Componente principal do app com roteamento
├── main.tsx                    # Ponto de entrada da aplicação
└── index.css                   # Estilos globais e variáveis de tema
```

---

## 🎯 Funcionalidades

### Gerenciamento de Produtos
- **Listar Produtos**: Ver todos os produtos em um grid responsivo
- **Adicionar Produto**: Registrar novos produtos com nome, preço, descrição, imagem
- **Editar Produto**: Atualizar detalhes de produtos existentes via drawer
- **Excluir Produto**: Remover produtos com diálogo de confirmação
- **Buscar Produtos**: Filtrar produtos por nome
- **Comprar Produto**: Adicionar produtos ao carrinho de compras

### Gerenciamento de Clientes
- **Listar Clientes**: Ver todos os clientes em uma tabela
- **Adicionar Cliente**: Registrar novos clientes com nome, email, telefone
- **Editar Cliente**: Atualizar informações do cliente via drawer
- **Excluir Cliente**: Remover clientes com confirmação

### Carrinho de Compras
- **Adicionar ao Carrinho**: Adicionar produtos a partir da listagem de produtos
- **Ver Carrinho**: Ver todos os itens com quantidades e preços
- **Remover Itens**: Excluir produtos individuais do carrinho
- **Limpar Carrinho**: Esvaziar o carrinho inteiro
- **Checkout**: Completar compra com modal de confirmação
- **Badge do Carrinho**: Contagem de itens em tempo real no cabeçalho

### Alternância de Tema
- **Modo Claro/Escuro**: Alternar entre temas
- **Tema Persistente**: Salva preferência no LocalStorage
- **Estilização Consistente**: Todos os componentes se adaptam ao tema

---

## 🌐 Integração com API

Este projeto usa a **Fake Store API** para dados de produtos:

- **Endpoint**: `https://fakestoreapi.com/products?limit=5`
- **Uso**: Busca os 5 principais produtos para a página inicial
- **Fallback**: Retorna dados mockados (simulados) se a API estiver indisponível

---

## 💾 Persistência de Dados

Todos os dados são armazenados no **LocalStorage**:

- `products` - Listagens de produtos
- `clients` - Informações de clientes
- `cart` - Itens do carrinho de compras
- `theme` - Preferência de tema (escuro/claro)

---