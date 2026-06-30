# Meet & Eat

Projeto de TCC de um restaurante fictício com foco em experiência premium, visual escuro e integração entre frontend, API e banco de dados.

## Camadas do projeto

- `meeteat-web`: frontend em ReactJS + Vite
- `meeteat-api`: API REST em Spring Boot + Java 17
- `meeteat-mobile`: app mobile em React Native + Expo
- `meeteat-api/sql/01-criar-banco-meeteat.sql`: script completo do SQL Server

## Estrutura

```text
Meet E Eat/
  README.md
  meeteat-web/
  meeteat-api/
  meeteat-mobile/
```

## Identidade visual

- Fundo: `#1a1a1a`
- Destaque: `#e8c87a`
- Texto claro: `#f5f0e8`
- Superfície: `#242424`

## O que já existe

- Banco SQL Server com tabelas, relacionamentos e dados iniciais
- API com entidades, repositórios, serviços, controllers e tratamento de erros
- Frontend com Home, Cardápio, Reservas, Galeria, Sobre e Contato

## Como executar

### Banco de dados

1. Abra o arquivo `meeteat-api/sql/01-criar-banco-meeteat.sql`.
2. Execute no SQL Server Management Studio.
3. Verifique se o banco `MeetEat` foi criado.

### API Spring Boot

1. Abra a pasta `meeteat-api`.
2. Ajuste `src/main/resources/application.properties` com sua senha do SQL Server.
3. Execute com Maven:

```bash
mvn spring-boot:run
```

4. A API deve subir em `http://localhost:8080`.

### Frontend React

1. Abra a pasta `meeteat-web`.
2. Instale as dependências:

```bash
npm install
```

3. Inicie o projeto:

```bash
npm run dev
```

4. O site deve abrir em `http://localhost:5173`.

## Endpoints principais

- `GET /pratos`
- `GET /pratos/{id}`
- `GET /pratos?categoriaId={id}`
- `POST /pratos`
- `PUT /pratos/{id}`
- `DELETE /pratos/{id}`
- `GET /categorias`
- `POST /categorias`
- `POST /reservas`
- `GET /reservas`
- `GET /reservas/disponibilidade?data=YYYY-MM-DD`
- `PATCH /reservas/{id}/status`

## Próximas melhorias

1. Criar painel administrativo.
2. Integrar melhor os dados da Home com o banco.
3. Começar o app mobile com Expo.
4. Adicionar testes e documentação Swagger.
