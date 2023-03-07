# Teste de conhecimento

# Teste de conhecimento
Desenvolva uma aplicação de registro de tickets de suporte. O objetivo deste teste é avaliar sua capacidade de implementar soluções utilizando o Laravel e o Vue.js. 

## Requisitos
Usuários têm as seguintes permissões:
- Cadastrar novos tickets
- Editar informações de tickets já registrados
- Excluir tickets
- Respondê-los
- Somente vão visualizar seus próprios tickets

Já usuários administradores possuem todas as permissões de usuários normais, além de:
- Encerrar tickets
- Visualizar qualquer ticket registrado no sistema.

A listagem de tickets deve ter a opção de filtragem pelo status (aberto ou fechado) para facilitar a visualização e gerenciamento dos tickets. 

Quando um ticket é fechado, a data e o usuário administrador responsável pelo encerramento são registrados.

### Banco de dados
Utilize o exemplo fornecido para criar e atualizar as migrações, criando os relacionamentos e utilizando os mesmos tipos de dados.
> Os tipos de dados que possuem “?” não são campos obrigatórios.

![Diagrama de esquema de dados](/database_schema_diagram.png)

### FrontEnd
Utilizando os exemplos disponibilizados [aqui](https://drive.google.com/drive/folders/11H9pm_Vpuy1e1FU9yilre_b4Iy2meXSo?usp=sharing), desenvolva uma as interfaces de Login, Cadastro de Usuário, Lista de Tickets e Criação/Edição/Conversação de Ticket segindo as orientações a seguir:
- Deve ser utilizado o framework [TailwindCSS](https://tailwindcss.com/) para gerar as folhas de estilo e o framework [VueJs](https://vuejs.org/) para gerar as páginas;
- As famílias de [cores](https://tailwindcss.com/docs/customizing-colors) a serem utilizadas são:
  - Backgrounds: `slate-100 dark:slate-900`;
  - Buttons: `sky-700`;
  - Inputs: `dark:border-sky-700 dark:bg-slate-700 border-gray-300 bg-white`;
  - Não é requerido darkmode para as páginas, porém foram disponibilizados os exemplos e as famílias de cores, seria um adicional interessante se implementado;
> Alguns opcionais foram colocados apenas nos exemplos disponibilizados para o frontend, porém necessitam de mudanças simples na estrutura de banco de dados apresentada;
- **Requeridos:**
  - Páginas desktop e responsivo para tamanhos de tela que variem desde a largura de 1536px até 320px utilizando as classes do TailwindCSS para [modo responsivo](https://tailwindcss.com/docs/responsive-design);
  - Página de Lista de Tickets deve conter um layout em Grid e outro em Table;
  - Páginas necessárias: Login, Cadastro, Lista de tickets(inicial), Cadastro/Edição/Conversação de Ticket;

## Para rodar a aplicação

```bash
#Para copiar o arquivo de configurações de ambiente
cp .env.example .env

#Para instalar as dependências do composer
composer update;

#Para instalar as dependências do node
npm install;

#Para rodar as migrações do banco de dados
php artisan migrate;

#Para gerar a chave da aplicação
php artisan key:generate;

#Para inicializar a aplicação
npm run dev;
php artisan serve;
```
