# Sprint 3 – Modelagem do Sistema

## 1. Identificação da entrega

**Sprint:** 3  
**Título:** Modelagem do Sistema  
**Pontuação:** 4,0 pontos  
**Objetivo:** Representar a solução por meio de modelos que auxiliem a compreensão do sistema e apoiem as decisões de desenvolvimento.

---

## 2. Descrição do sistema de exemplo

Para orientar os grupos, este documento apresenta um exemplo de modelagem para uma **aplicação web de agendamento de atendimentos**.

### 2.1. Visão geral do sistema

O sistema permite que usuários realizem cadastro, façam login, consultem serviços disponíveis, visualizem horários livres e realizem agendamentos online. Além disso, administradores podem cadastrar serviços, organizar horários disponíveis e acompanhar a agenda geral.

### 2.2. Objetivo da solução

A proposta do sistema é facilitar o processo de agendamento, reduzir conflitos de horário e centralizar o gerenciamento dos atendimentos em uma aplicação web.

### 2.3. Perfis de usuário

- **Usuário:** realiza cadastro, autenticação, consulta serviços, agenda e cancela atendimentos.
- **Administrador:** gerencia serviços, horários disponíveis, usuários e acompanha a agenda geral.

---

## 3. Conteúdo esperado na Sprint 3

Nesta sprint, espera-se que o grupo apresente modelos compatíveis com a solução proposta, de forma a demonstrar:

- definição dos principais elementos do sistema;
- representação do comportamento e/ou da estrutura da solução;
- refinamento do escopo a partir da modelagem;
- alinhamento dos modelos com a proposta de aplicação web.

---

## 4. Artefatos a serem entregues

O grupo deverá entregar:

- diagramas ou modelos adequados à proposta do grupo;
- descrição textual complementar dos modelos;
- vínculo entre requisitos e modelos produzidos;
- backlog atualizado com base no refinamento obtido;
- registro de revisão da sprint;
- documentação dos modelos no GitHub;
- arquivo `docs/sprints/sprint-03.md`.

---

## 5. Exemplo de entregas da Sprint 3

Para este sistema web de exemplo, uma entrega adequada pode conter:

1. **Diagrama de Casos de Uso** para representar as funcionalidades principais.
2. **Diagrama de Componentes** para representar a estrutura da aplicação web.
3. **Modelo de Dados** para representar entidades e relacionamentos principais.
4. **Diagrama de Sequência** para representar um fluxo central do sistema.
5. **Texto explicativo** relacionando os modelos aos requisitos levantados.
6. **Atualização do backlog** com refinamentos identificados durante a modelagem.

---

## 6. Exemplo de requisitos relacionados

### Requisitos funcionais

- **RF01:** O usuário deve poder criar uma conta.
- **RF02:** O usuário deve poder realizar login.
- **RF03:** O usuário deve poder visualizar serviços disponíveis.
- **RF04:** O usuário deve poder consultar horários disponíveis.
- **RF05:** O usuário deve poder realizar agendamentos.
- **RF06:** O usuário deve poder cancelar agendamentos.
- **RF07:** O administrador deve poder gerenciar serviços.
- **RF08:** O administrador deve poder gerenciar horários disponíveis.

### Requisitos não funcionais

- **RNF01:** O sistema deve estar acessível via navegador web.
- **RNF02:** O sistema deve exigir autenticação para ações restritas.
- **RNF03:** O sistema deve persistir os dados de usuários, serviços e agendamentos.

---

## 7. Vínculo entre requisitos e modelos

| Requisito | Modelo relacionado | Justificativa |
|---|---|---|
| RF01 – Criar conta | Casos de Uso / Modelo de Dados | Representa cadastro e persistência do usuário |
| RF02 – Login | Casos de Uso / Componentes | Mostra autenticação e interação entre frontend e backend |
| RF03 – Visualizar serviços | Casos de Uso / Modelo de Dados | Relaciona consulta ao catálogo de serviços |
| RF04 – Consultar horários | Casos de Uso / Modelo de Dados / Sequência | Relaciona disponibilidade e fluxo da aplicação |
| RF05 – Realizar agendamento | Casos de Uso / Sequência / Modelo de Dados | Representa o principal fluxo de negócio |
| RF07 – Gerenciar serviços | Casos de Uso / Modelo de Dados | Representa manutenção administrativa |

---

## 8. Diagramas de exemplo em PlantUML

A seguir, apresentam-se exemplos de diagramas que poderiam compor a Sprint 3.

### 8.1. Diagrama de Casos de Uso

![Diagrama de Casos de Uso](https://drive.google.com/uc?export=view&id=1vHS_d9w0VhKuCz6WSaMqVWVC0HMtXJpA)

### 8.2. Diagrama de Componentes


![Diagrama de Casos de Uso](https://drive.google.com/uc?export=view&id=12Id2soPe29PqQyrVl81Lf87ybdieEI4D)

### 8.3. Modelo de Dados

![Diagrama de Casos de Uso](https://drive.google.com/uc?export=view&id=1yDz3XebjgLcCxi7Jd4BYLBfQInRHDC5n)


### 8.4. Diagrama de Sequência

![Diagrama de Casos de Uso](https://drive.google.com/uc?export=view&id=1YQhoyy4JeduEvxNDpCQ5uu7uP7ry_S3Q)

---

## 9. Descrição textual complementar dos modelos

### 9.1. Casos de uso
O diagrama de casos de uso apresenta os dois principais perfis do sistema: usuário e administrador. Ele mostra as funcionalidades centrais oferecidas pela aplicação e evidencia que algumas operações dependem de autenticação.

### 9.2. Componentes
O diagrama de componentes representa a estrutura geral da aplicação web, separando frontend, backend, serviços internos e banco de dados. Esse modelo ajuda a justificar decisões arquiteturais iniciais.

### 9.3. Modelo de dados
O modelo de dados mostra as entidades centrais do domínio e seus relacionamentos, servindo como apoio para a implementação do banco de dados e para a compreensão das regras de negócio.

### 9.4. Sequência
O diagrama de sequência detalha o fluxo de realização de agendamento, mostrando como o usuário interage com a interface e como a solicitação percorre backend e banco de dados.

---

## 10. Refinamento do backlog após a modelagem

A modelagem normalmente permite identificar melhorias e detalhamentos nas histórias do backlog. Exemplo:

### Antes do refinamento
- Como usuário, quero agendar atendimento.

### Após o refinamento
- Como usuário, quero visualizar horários disponíveis para escolher um atendimento.
- Como usuário, quero confirmar um agendamento online.
- Como sistema, devo impedir agendamentos em horários já ocupados.
- Como administrador, quero cadastrar novos serviços com duração definida.

### Exemplo de itens adicionados ao backlog
- Criar tela de listagem de serviços.
- Implementar endpoint de consulta de horários.
- Modelar tabela de agendamentos.
- Implementar regra de validação de conflito de horários.
- Criar tela “Meus agendamentos”.

---

## 11. Exemplo de revisão da sprint

### O que foi concluído
- Modelagem dos principais fluxos do sistema.
- Definição inicial da estrutura da aplicação web.
- Identificação das entidades principais do domínio.
- Refinamento de histórias de usuário do backlog.

### Principais decisões tomadas
- A solução será web com frontend e backend separados.
- O sistema exigirá autenticação para ações de agendamento e administração.
- O fluxo de agendamento será tratado como principal prioridade de implementação.

### Dificuldades encontradas
- Necessidade de detalhar melhor regras de disponibilidade.
- Ajustes no escopo para manter viabilidade dentro do semestre.

### Próximos passos
- Implementar as primeiras funcionalidades do backlog priorizado.
- Evoluir a arquitetura da solução.
- Definir testes iniciais para o fluxo de agendamento.

---

## 12. Exemplo de estrutura do arquivo `docs/sprints/sprint-03.md`

Os grupos podem usar a seguinte organização:

```markdown
# Sprint 3 – Modelagem do Sistema

## Objetivo
Representar a solução por meio de modelos que auxiliem a compreensão do sistema e apoiem as decisões de desenvolvimento.

## Modelos produzidos
- Diagrama de Casos de Uso
- Diagrama de Componentes
- Modelo de Dados
- Diagrama de Sequência

## Relação com os requisitos
[Listar requisitos e modelos correspondentes]

## Refinamentos realizados no backlog
[Descrever histórias atualizadas, criadas ou detalhadas]

## Revisão da sprint
[Registrar o que foi feito, decisões tomadas e próximos passos]
```

---

## 13. Observação importante aos alunos

Em projetos de aplicação web, **não é obrigatório apresentar diagrama de classes orientado a objetos**. Serão aceitos modelos compatíveis com a solução proposta, como:

- casos de uso;
- componentes;
- modelo de dados;
- sequência;
- atividades;
- navegação;
- wireframes;
- protótipos de interface.

O mais importante é que os modelos permitam compreender claramente:

- o que o sistema faz;
- como o usuário interage com ele;
- como os dados são organizados;
- como as partes da solução se conectam;
- como os principais fluxos acontecem.

---

## 14. Conclusão

Este exemplo mostra uma forma adequada de documentar a Sprint 3 em um projeto acadêmico com aplicação web. Os grupos podem adaptar o domínio do sistema, os requisitos e os diagramas de acordo com o problema escolhido, mantendo a coerência entre backlog, modelagem e proposta de solução.
