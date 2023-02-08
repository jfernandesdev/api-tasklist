# API Tasklist

Desafio 01 desenvolvido para o Ignite Trilha Back-end (Nodejs). O desafio trata-se de API para realizar o CRUD de tarefas (tasks)

## Funcionalidades ✅
- [x] Criação de uma task (`id`, `title`, `description`, `completed_at`, `created_at`, `updated_at`);
- [x] Listagem de todas as tasks;
- [x] Atualização de uma task pelo `id`;
- [x] Remover uma task pelo `id`;
- [x] Marcar pelo `id` uma task como completa;
- [x] Importação de tasks em massa por um arquivo CSV.

## Tecnologias utilizadas: 🚀
- Node | 18.12.0
- Javascript
- CSV-parse | ^5.3.4

## Rotas 🧭

- <b>POST</b> - `/tasks`
    - Criar uma task no banco de dados, enviando os campos `title` e `description` por meio do `body` da requisição. Os campos: `id`,`created_at`, `updated_at` e `completed_at` são preenchidos automaticamente. 
- <b>GET</b> - `/tasks`
    -  Listar todas as tasks salvas no banco de dados. Também é possível realizar uma busca, filtrano as tasks pelo `title` e `description`.
- <b>PUT</b> - `/tasks/id`
    - Atualizar uma task pelo `id`. No `body` da requisição é recebido o `title` e/ou `description` para serem atualizados. Se for enviado somente o `title`, significa que o `description` não pode ser atualizado e vice-versa.
- <b>PATCH</b> - `/tasks/:id/complete`
    - Marcar a task como completa
- <b>DELETE</b> - `/tasks/:id`
    - Remoção de uma task pelo `id`.

## Rodando a aplicação localmente ⚙

```
// Clone o projeto e acesse a pasta:
$ git clone https://github.com/jfernandesdev/api-tasklist.git && cd api-tasklist

// Instale as dependências:
$ npm install

// Rode o servidor (http://localhost:3333)
$ npm run dev

// Para rodar a importação do CSV: 
$ node stream/import-csv.js
```

<br>

<img src="https://i.ibb.co/Yckq764/footer-signature.png" alt="footer-signature" border="0"  width='400px' />


