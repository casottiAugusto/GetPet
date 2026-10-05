# GetPet

Plataforma para aproximar tutores, profissionais de pet shop e pessoas interessadas em adotar um pet. A proposta reúne, em um só lugar, a divulgação e o agendamento de serviços de banho e tosa e a consulta de animais disponíveis para adoção.

> **Status do projeto:** em desenvolvimento. Este README descreve a proposta e o escopo planejado. A estrutura atual contém as pastas `frontend/` e `backend/`, mas ainda não há código de aplicação, tecnologias ou comandos de execução definidos.

## Sumário

- [Sobre o projeto](#sobre-o-projeto)
- [Objetivos](#objetivos)
- [Público e perfis de acesso](#público-e-perfis-de-acesso)
- [Funcionalidades previstas](#funcionalidades-previstas)
- [Jornadas principais](#jornadas-principais)
- [Requisitos e regras de negócio](#requisitos-e-regras-de-negócio)
- [Estrutura do repositório](#estrutura-do-repositório)
- [Tecnologias e execução](#tecnologias-e-execução)
- [Privacidade e segurança](#privacidade-e-segurança)
- [Próximos passos](#próximos-passos)
- [Contribuição](#contribuição)

## Sobre o projeto

O GetPet é a ideia de um sistema voltado ao universo pet, com dois serviços centrais:

1. **Banho e tosa:** apresentar serviços oferecidos por um pet shop e permitir que tutores encontrem informações e solicitem ou agendem um atendimento.
2. **Adoção de pets:** divulgar animais que procuram um lar e facilitar o contato entre interessados e responsáveis pelo processo de adoção.

A plataforma pretende tornar essas informações mais acessíveis e organizadas. O fluxo exato de agendamento, contato e adoção deverá ser definido junto com as regras do negócio antes da implementação.

## Objetivos

- Reunir informações sobre serviços de banho e tosa em uma experiência simples.
- Facilitar a consulta de serviços, valores, horários e disponibilidade, quando essas informações forem cadastradas.
- Ajudar pessoas interessadas em adoção a conhecer os animais disponíveis.
- Dar visibilidade aos animais e às organizações ou responsáveis que os divulgam.
- Organizar solicitações de atendimento e manifestações de interesse em adoção.
- Oferecer uma experiência clara tanto para clientes quanto para quem administra os cadastros.

## Público e perfis de acesso

Os perfis abaixo são uma proposta inicial e poderão ser ajustados conforme as decisões do projeto:

### Visitante ou cliente

- Consulta os serviços oferecidos.
- Busca informações sobre banho e tosa.
- Visualiza os pets anunciados para adoção e seus detalhes.
- Envia uma solicitação de agendamento ou demonstra interesse em um pet, conforme os canais que forem definidos.

### Responsável pelo pet shop

- Mantém informações de serviços, preços e horários atualizadas.
- Consulta e acompanha solicitações de agendamento.
- Informa disponibilidade ou entra em contato com o cliente para confirmar o atendimento.

### Responsável por adoções

- Cadastra animais com informações e fotos.
- Atualiza a situação de disponibilidade do animal.
- Analisa contatos e conduz o processo de adoção.

### Administrador

- Gerencia usuários, cadastros e conteúdo da plataforma.
- Modera anúncios e acompanha solicitações.
- Apoia a manutenção e a segurança do sistema.

> A existência de contas, permissões específicas e um painel administrativo depende da definição do escopo de implementação.

## Funcionalidades previstas

### Serviços de banho e tosa

- Catálogo com descrição dos serviços disponíveis.
- Informações de preço, duração e condições de atendimento, caso sejam fornecidas pelo estabelecimento.
- Dados úteis sobre o atendimento, como endereço e horários.
- Formulário para solicitar um horário, com informações do tutor e do pet.
- Consulta do estado da solicitação, se houver suporte a acompanhamento na plataforma.
- Confirmação de agendamento pelo estabelecimento, de acordo com a regra definida para disponibilidade.

### Adoção de pets

- Lista de animais disponíveis para adoção.
- Página ou ficha individual com fotos e informações fornecidas pelo responsável.
- Filtros de busca, se definidos para a primeira versão.
- Formulário ou canal de contato para demonstrar interesse.
- Atualização da situação do anúncio, por exemplo: disponível, em processo de adoção ou adotado.
- Orientações sobre as etapas e os critérios do processo de adoção.

### Conta e gerenciamento

Como possibilidade para versões futuras, o sistema poderá oferecer:

- Cadastro e autenticação de clientes e responsáveis.
- Área para revisar solicitações.
- Painel de gerenciamento dos serviços e dos anúncios de adoção.
- Notificações sobre alterações de status.
- Histórico de solicitações e atendimentos.

Esses recursos ainda não devem ser considerados implementados.

## Jornadas principais

### Solicitar banho e tosa

1. O cliente consulta os serviços e as informações do estabelecimento.
2. Escolhe o serviço desejado e informa os dados necessários do pet.
3. Indica uma preferência de data ou horário, caso esse recurso esteja disponível.
4. Envia a solicitação.
5. O estabelecimento verifica a disponibilidade e confirma ou propõe outra opção.

Uma solicitação não deve ser apresentada como agendamento confirmado até que o estabelecimento a confirme, salvo se a futura implementação oferecer disponibilidade em tempo real.

### Demonstrar interesse em adoção

1. A pessoa consulta os animais anunciados.
2. Abre a ficha de um pet para conhecer suas informações.
3. Entra em contato ou preenche a manifestação de interesse.
4. O responsável pela adoção analisa o contato e informa as próximas etapas.
5. O anúncio é atualizado quando a situação do animal mudar.

O cadastro de um animal não significa que a adoção esteja garantida. A decisão e as etapas ficam a cargo do responsável pelo processo.

## Requisitos e regras de negócio

As regras abaixo servem como orientação para a implementação e precisam ser confirmadas pelo responsável pelo produto:

- Serviços, preços, horários e disponibilidade devem ser apresentados com informações atualizadas.
- Solicitações de atendimento devem ter um estado compreensível, como pendente, confirmada, recusada ou cancelada, caso o sistema implemente acompanhamento.
- O pet shop deve validar a disponibilidade antes de confirmar um horário.
- Anúncios de adoção devem identificar um responsável e apresentar somente informações autorizadas.
- A disponibilidade de cada pet deve ser atualizada quando o processo avançar ou terminar.
- Dados pessoais devem ser solicitados apenas quando necessários para a finalidade informada.
- Formulários devem orientar a pessoa sobre quais dados são obrigatórios e como serão usados.
- Conteúdos, critérios de adoção e regras de atendimento devem ser definidos pelos responsáveis envolvidos.

## Estrutura do repositório

Estrutura identificada neste momento:

```text
GetPet/
├── backend/   # Espaço previsto para a aplicação e os serviços de servidor
├── frontend/  # Espaço previsto para a interface da plataforma
└── README.md  # Apresentação, escopo e orientações do projeto
```

As pastas `backend/` e `frontend/` ainda não possuem arquivos de aplicação. A organização interna será documentada quando as tecnologias e os módulos forem definidos.

## Tecnologias e execução

As tecnologias ainda não foram definidas. Por isso, não há neste momento instruções verificadas para instalar dependências, configurar variáveis de ambiente ou executar o sistema.

Quando a implementação estiver disponível, esta seção deverá incluir:

- versões necessárias de linguagens e ferramentas;
- instalação das dependências do frontend e do backend;
- configuração de variáveis de ambiente, com um arquivo de exemplo sem credenciais;
- inicialização de banco de dados e outros serviços necessários;
- comandos para desenvolvimento, testes e build;
- endereço local para acessar a aplicação.

Não inclua senhas, tokens ou outras credenciais reais no repositório. Utilize variáveis de ambiente e mantenha arquivos locais de configuração fora do controle de versão.

## Privacidade e segurança

Como a plataforma poderá lidar com dados de contato e informações sobre animais, a implementação deve:

- coletar somente os dados necessários para o atendimento ou contato de adoção;
- explicar a finalidade da coleta e restringir o acesso aos dados;
- validar os dados recebidos em formulários;
- proteger credenciais e informações pessoais;
- permitir a correção ou remoção de dados conforme as regras aplicáveis;
- evitar publicar dados pessoais sem autorização.

As medidas técnicas e os avisos legais deverão ser definidos antes de disponibilizar o sistema ao público.

## Próximos passos

1. Definir o escopo da primeira versão (MVP) e os perfis que poderão acessar o sistema.
2. Escolher tecnologias para frontend, backend e armazenamento de dados.
3. Detalhar campos, estados e regras do agendamento.
4. Definir como serão cadastrados e moderados os anúncios de adoção.
5. Implementar os fluxos prioritários e seus critérios de aceite.
6. Documentar configuração, execução e testes após a criação da aplicação.

## Contribuição

O projeto está em fase inicial. Antes de contribuir com código, alinhe as mudanças ao escopo do produto e às tecnologias que forem escolhidas. Ao implementar novas funcionalidades, atualize também a documentação correspondente e inclua testes quando aplicável.
