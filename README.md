# 🚀 Full Stack Challenge — Vue 3 + Quasar + TypeScript

# 📌 Objetivo
Este desafio tem como objetivo avaliar suas habilidades como desenvolvedor(a) Full Stack, com foco em:

- Arquitetura de projeto
- Boas práticas de front-end e back-end
- Organização de código
- Integração entre camadas
- Experiência do usuário (UX/UI)
- Estruturação de API
- Tratamento de erros e validações

# 🧠 Cenário

Você deverá desenvolver um pequeno Sistema de Gestão de Veículos, contendo autenticação e um CRUD.
A aplicação deve demonstrar domínio técnico tanto no front-end quanto no back-end.

# 🔐 Autenticação

Implemente:
- Tela de Login
- Validação de campos (e-mail válido, senha obrigatória)
- Feedback de erro amigável
- Controle de sessão (JWT ou similar)
- Proteção de rotas privadas
- Logout funcional

# Diferenciais
- Refresh token
- Persistência de sessão
- Tratamento de token expirado
- Interceptors para requisições
- Testes automatizados com Jest (unitários ou e2e)

# 🚗 CRUD de Veículos

A aplicação deve permitir:

➕ Criar Veículo

Campos sugeridos:
- Marca
- Modelo
- Ano
- Placa (com máscara)
- Cor
- Valor (com máscara monetária)
- Tipo (carro, moto, caminhão)
- Status (disponível, vendido, reservado)

Com:
- Validações obrigatórias
- Regras de negócio
- Feedback visual

📄 Listar Veículos
- Tabela ou cards
- Paginação
- Busca por marca/modelo
- Ordenação
- Estado vazio
- Tratamento de erro

✏️ Editar Veículo
- Formulário pré-preenchido
- Validações
- Feedback de sucesso/erro

🗑️ Excluir Veículo
- Confirmação antes de excluir
- Feedback visual

📤 Upload de Fotos
- Ao criar ou editar um veículo, deve ser possível:
- Adicionar uma ou múltiplas fotos
- Visualizar preview antes de salvar
- Remover imagens antes do envio

Validar:
- Tipo de arquivo (JPG, PNG, WEBP) (Tamanho máximo (ex: 5MB por imagem))

Requisitos técnicos:

- Upload via formulário (multipart/form-data)
- Armazenamento das imagens no backend
- Associação das imagens ao veículo no banco de dados
-Tratamento de erro em caso de falha no upload
- Feedback visual de loading

# 🗂️ Página de Listagem com Cards de Veículos

Além da listagem em tabela (caso implementada), deverá existir uma página de listagem em formato de cards, simulando um catálogo de veículos.


Exemplo de rota:

<pre> /vehicles</pre>

# 🧱 Estrutura dos Cards

Cada veículo deve ser exibido em formato de card, contendo no mínimo:
- Foto principal do veículo
- Marca e modelo
- Ano
- Valor formatado
- Status (disponível, vendido, reservado)
- Botão para visualizar detalhes
- Botão para editar
- Botão para excluir (caso tenha permissão)

# 🎨 Requisitos de UX

Esperamos:
- Layout responsivo (grid adaptável para mobile, tablet e desktop)
- Uso adequado de componentes do Quasar (ex: QCard, QImg, QBadge)
- Feedback visual de loading (ex: QSkeleton)
- Estado vazio amigável quando não houver veículos cadastrados
- Tratamento visual para erro de carregamento
- Indicador visual de status (ex: badge colorida)

# 🔍 Funcionalidades adicionais na listagem

A página deve conter:
- Campo de busca (marca/modelo)
- Filtro por status
- Ordenação (ex: por valor ou ano)
- Paginação (client-side ou server-side)

Diferenciais:
- Busca com debounce
- Paginação server-side
- Skeleton loading
- Animação suave ao carregar cards

# 🧠 Avaliaremos nesta etapa

- Organização da UI
- Componentização (ex: VehicleCard.vue)
- Reatividade e filtros
- Estruturação de estado (Pinia)
- Performance na renderização da lista

Responsividade real

# 📄 Página de Detalhes do Veículo
Deve existir uma rota específica para visualização individual do veículo.

Exemplo:
<pre>/vehicles/:id</pre>

Essa página deve conter:

📌 Informações do veículo

- Marca
- Modelo
- Ano
- Placa
- Cor
- Valor formatado
- Tipo
- Status

🖼️ Galeria de Fotos

A página deve exibir:

- Galeria com imagem principal
- Miniaturas clicáveis
- Alternância entre imagens
- Layout responsivo
- Estado vazio caso não existam fotos

Diferenciais:
- Modal para visualizar imagem ampliada
- Carrossel (ex: QCarousel do Quasar)
- Skeleton loading para imagens
- Lazy loading
- Zoom na imagem

# 🖥️ Requisitos Técnicos — Front-End

Obrigatório utilizar:
- Vue 3
- Quasar Framework
- TypeScript
- Vue Router
- Pinia (ou outro gerenciador de estado)
  
Esperamos:
- Componentização adequada
- Separação de responsabilidades
- Código limpo e organizado
- Reutilização de componentes
- Responsividade (mobile e desktop)
- Máscaras corretas (placa e valor)
- Validações no formulário
- Estados visuais (loading, erro, sucesso)

# Requisitos Técnicos — Back-End

Obrigatório utilizar:
- Node
- Nestjs
- MySQL
- Prisma

Diferenciais
- Docker
- Redis
  
Esperamos:
- Estrutura organizada
- Separação de camadas (controller, service, repository)
- Validação de dados no backend
- Autenticação
- Tratamento de erros
- Persistência de dados com MySQL via Prisma


# 🌐 Integração com API Pública (Opcional)
Você pode integrar com alguma API pública para enriquecer o projeto (ex: API de marcas de veículos), mas não é obrigatório.

# 📁 Estrutura do Projeto

Estrutura do Front-End

Exemplo esperado:
<pre> src/
 ├─ pages/
 ├─ components/
 ├─ layouts/
 ├─ stores/
 ├─ services/
 ├─ router/
</pre>

Estrutura do Back-End

Seguir padrão de separação adotado pelo Nestjs.
<pre>
  src/
├─ modules/
│  ├─ users/
│  │  ├─ dtos/
│  │  │  └─ create-user.dto.ts
│  │  ├- users.controller.ts
│  │  ├- users.service.ts
│  │  ├- users.repository.ts
│  │  └─ users.module.ts
│  └─ auth/
│     ├─ strategies/
│     ├─ dtos/
│     ├─ auth.controller.ts
│     ├─ auth.service.ts
│     ├─ auth.repository.ts
│     └─ auth.module.ts
│
├─ utils/
│  ├─ decorators/
│  ├─ guards/
│  ├─ filters/
│  ├─ interceptors/
│  ├─ pipes/
│  └─ functions/
│
├─ config/
│  └─ app.config.ts
│
├─ middlewares/
│  └─ logger.middleware.ts
│
├─ main.ts
└─ app.module.ts
</pre>
# 📦 Entrega

No repositório, inclua:
- Código fonte completo

README com:
- Tecnologias utilizadas
- Como rodar o projeto
- Decisões técnicas
- (Opcional) Link de deploy


# 💡 Observação Importante
O objetivo não é complexidade extrema, mas sim demonstrar:

✔ Organização
✔ Clareza
✔ Estrutura
✔ Domínio técnico
✔ Boas práticas


 Boa sorte 🚀
