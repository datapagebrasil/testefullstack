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
Inclua no repositório:

Estrutura do Front-End
Exemplo esperado:
<pre> src/
 ├─ pages/
 ├─ components/
 ├─ layouts/
 ├─ stores/
 ├─ services/
 ├─ router/
 ├─ composables/
</pre>

Estrutura do Back-End
Separação clara de:
<pre> src/
 ├─ controllers/
 ├─ services/
 ├─ repositories/
 ├─ middlewares/
 ├─ routes/
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
