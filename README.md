# Curso Next.js by Vercel

Curso Next.js App Router! Neste curso, aprenderemos os principais recursos avançados do Next.js criando um aplicativo da web full-stack.


## 🌊 O Projeto 🌊

Para este curso, construiremos uma versão simplificada de um painel financeiro que possui:

- 📦 Uma página inicial pública.
- 📦 Uma página de login.
- 📦 Páginas do painel protegidas por autenticação.
- 📦 A capacidade dos usuários de adicionar, editar e excluir faturas.
  
O painel também terá um banco de dados que o acompanhará, que você configurará em um capítulo posterior .

Ao final do curso, você terá as habilidades essenciais necessárias para começar a construir aplicativos Next.js full-stack.

## Visão geral

- **🟢 Estilo**: as diferentes maneiras de estilizar seu aplicativo em Next.js.
- **🔗 Otimizações**: como otimizar imagens, links e fontes.
- **🐳 Roteamento**: como criar layouts e páginas aninhadas usando roteamento do sistema de arquivos.
- **🐦 Busca de dados**: como configurar um banco de dados no Vercel e práticas recomendadas para busca e streaming.
- **📦 Pesquisa e paginação**: como implementar pesquisa e paginação usando parâmetros de pesquisa de URL.
- **📦 Mutação de dados**: como alterar dados usando React Server Actions e revalidar o cache Next.js.
- **📦 Tratamento de erros**: como lidar com 404erros gerais e não encontrados.
- **📦 Validação e acessibilidade de formulários**: como fazer a validação de formulários no servidor e dicas para melhorar a acessibilidade.
- **📦 Autenticação**: como adicionar autenticação ao seu aplicativo usandoNextAuth.jse Middleware.
- **📦 Metadados**: como adicionar metadados e preparar seu aplicativo para compartilhamento social.

## 🗂 Requisitos de sistemas

- **🟢 Node.js**: 18.17.0 ou posterior instalado
- **🔗 Sistemas operacionais**: macOS, Windows (incluindo WSL) ou Linux.

## 🗂 Criando um novo projeto

Para criar um aplicativo Next.js, abra seu terminal,na pasta que você deseja manter seu projeto e execute o seguinte comando:


```bash
npx create-next-app@latest nextjs-dashboard --use-npm --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example"
```

Este comando usa create-next-appuma ferramenta Command Line Interface (CLI) que configura um aplicativo Next.js para você. No comando acima, você também está usando o --examplesinalizador com o exemplo inicialpara este curso.

```bash
cd nextjs-dashboard
```

## Estrutura de pastas

- **/app:** contém todas as rotas, componentes e lógica do seu aplicativo, é aqui que você trabalhará principalmente.
- **/app/lib:** contém funções usadas em seu aplicativo, como funções utilitárias reutilizáveis ​​e funções de busca de dados.
- **/app/ui:** contém todos os componentes de UI do seu aplicativo, como cartões, tabelas e formulários. Para economizar tempo, pré-estilizamos esses componentes para você.
- **/public:** contém todos os ativos estáticos do seu aplicativo, como imagens.
- **/scripts:** contém um script de propagação que você usará para preencher seu banco de dados em um capítulo posterior.


## Dados Iniciais

Ao criar interfaces de usuário, é útil ter alguns dados de espaço reservado. Se um banco de dados ou API ainda não estiver disponível, você poderá:

- Use dados de espaço reservado no formato JSON ou como objetos JavaScript.
- Use um serviço de terceiros como mockAPI.
  
Para este projeto, fornecemos alguns dados de espaço reservado em formato app/lib/placeholder-data.js. Cada objeto JavaScript no arquivo representa uma tabela no seu banco de dados. Por exemplo, para a tabela de faturas:


   ```js
  // /app/lib/placeholder-data.js
  const invoices = [
  {
    customer_id: customers[0].id,
    amount: 15795,
    status: 'pending',
    date: '2022-12-06',
  },
  {
    customer_id: customers[1].id,
    amount: 20348,
    status: 'pending',
    date: '2022-11-14',
  },
  // ...
];
   ```

No capítulo sobre como configurar seu banco de dados , você usará esses dados para propagar seu banco de dados (preenchê-lo com alguns dados iniciais).


## TypeScript

Você também pode notar que a maioria dos arquivos tem um sufixo .tsou .tsx. Isso ocorre porque o projeto está escrito em TypeScript. Queríamos criar um curso que refletisse o cenário moderno da web.

Não há problema se você não conhece TypeScript - forneceremos os trechos de código TypeScript quando necessário.

Por enquanto, dê uma olhada no ```/app/lib/definitions.ts``` arquivo. Aqui definimos manualmente os tipos que serão retornados do banco de dados. Por exemplo, a tabela de faturas possui os seguintes tipos:

## 🤝 Contribuição

Contribuições são muito bem-vindas! Se deseja ajudar, faça um fork do repositório, crie uma branch com suas
modificações, e envie um pull request.

Sua ajuda é crucial para apoiar a comunidade afetada pelas enchentes no Rio Grande do Sul!