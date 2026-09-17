# Metodologia cascata

### **Objetivo do projeto**

O projeto **EsTuDoList** tem como objetivo desenvolver uma plataforma para organização de tarefas, que possa ser utilizada para gerenciar atividades domésticas, compromissos, rotina diária e tarefas escolares, com foco principal em estudantes.

### **Requisitos funcionais (RF)**

#### **RF01 — Cadastrar tarefa**

Para cadastrar uma tarefa, a pessoa usuária deve adicionar um bloco de anotação na lista, clicando no botão **“+”**. Em seguida, deve selecionar **“Escrever”** para inserir um texto (lembrete, objetivo ou descrição).

Devem ser informados os seguintes dados: **nome**, **objetivo/descrição** e **função**.

**Função:** caso o bloco represente uma tarefa, selecione **“Tarefa”** (opção exibida acima do bloco). Se o item for recorrente e precisar aparecer diariamente, selecione **“Rotina”**. Se for apenas um registro informativo, selecione **“Nota”**.

#### **RF02 — Editar tarefa**

Para editar uma tarefa, a pessoa usuária deve clicar no item desejado e, em seguida, selecionar o ícone de **caneta**, exibido no canto inferior direito do bloco.

#### **RF03 — Excluir tarefa**

Para excluir uma tarefa, a pessoa usuária deve clicar no item desejado e selecionar o ícone de **lixeira**, exibido no canto inferior esquerdo do bloco. Após isso, deve confirmar a exclusão.

#### **RF04 — Marcar tarefa como concluída**

Para marcar uma tarefa como concluída, a pessoa usuária deve clicar no botão de **check** localizado na parte superior do bloco. O item será movido para a seção **“Tarefas concluídas”** e poderá ser desmarcado posteriormente, caso necessário.

#### **RF05 — Pesquisar/filtrar tarefas**

A pesquisa e/ou filtragem de tarefas deve permitir consultas por:

- **Nome**
- **Status** (concluída / não concluída)
- **Função** (tarefa / rotina / nota)

### **Requisitos não funcionais (RNF)**

1. **Desempenho:** o tempo de resposta do aplicativo deve ser inferior a **2 segundos**.
2. **Disponibilidade:** o aplicativo deve poder ser acessado e utilizado a qualquer momento.
3. **Responsividade:** o aplicativo deve se adaptar a diferentes tamanhos de tela, como **computadores** e **tablets**.

### **Fora de escopo**

Os itens a seguir não serão contemplados nesta versão do projeto:

- **Uso offline com sincronização posterior:** permitir que o sistema funcione sem internet e sincronize quando houver conexão.
- **Cores para indicar urgência:** uso de cores para destacar prioridade/urgência das tarefas.
- **Lembretes programados:** notificações diárias para rotinas ou alertas para tarefas próximas do prazo (depende de programação de horários e/ou integração com outros serviços).
- **Pesquisa pela data de registro da tarefa:** armazenar e filtrar tarefas pela data de criação.

## Metodologia cascata

- 📋 **Requisitos**: Mapear o que o sistema deve fazer.
- 🎨 **Análise e Projeto**: Desenhar as telas e planejar a estrutura dos dados.
- 💻 **Desenvolvimento**: Escrever o código da aplicação.
- 🧪 **Testes**: Encontrar falhas e validar se tudo funciona como esperado.
- 🚀 **Implantação e Manutenção**: Colocar o site no ar e corrigir problemas do uso real.

| REQUISITOS | ANÁLISE E PROJETO | DESENVOLVIMENTO | TESTES | IMPLANTAÇÃO E MANUTENÇÃO |
| --- | --- | --- | --- | --- |
| Escrever o Documento de Escopo com todas as funcionalidades. | Desenhar as telas do aplicativo no Figma. | Escrever o código HTML da página principal. | Verificar se o aplicativo funciona corretamente nos navegadores Chrome e Firefox. | Publicar a versão final do site em um servidor online para que todos possam usar. |
| Entrevistar alunos para entender como eles organizam suas tarefas hoje. | Definir a paleta de cores e a fonte que serão usadas no site. | Programar a função em JavaScript que salva uma nova tarefa no navegador. | Tentar "quebrar" o campo de data, inserindo um texto em vez de um número. | Corrigir um bug reportado por um usuário uma semana após o lançamento. |
| Levantar requisitos com usuários: aplicar um mini questionário com estudantes para descobrir quais funções são mais importantes (ex.: rotina diária, notas rápidas, filtros). | Criar o fluxograma do sistema: desenhar o passo a passo de “Cadastrar tarefa” (clicar + → escolher tipo → digitar → salvar → aparecer na lista). | Implementar salvamento e carregamento: salvar as tarefas no navegador (ex.: LocalStorage) e recarregar automaticamente quando abrir o site. | Teste de validação de entrada: tentar cadastrar tarefa sem nome (ou com nome muito grande) e verificar se o sistema bloqueia ou avisa corretamente. | Publicar e testar em ambiente real: colocar no GitHub Pages/Netlify/Vercel e testar em celular e computador para ver se a responsividade está ok. |
| Definir regras de negócio: especificar o que acontece quando uma tarefa é marcada como concluída (vai para “tarefas concluídas”, pode voltar, mantém descrição, etc.). | Modelar os dados (estrutura): definir quais campos uma tarefa terá e como guardar (ex.: id, nome, descricao, tipo, concluida, dataCriação). | Implementar edição e exclusão: criar as funções para editar uma tarefa existente e remover uma tarefa (com confirmação). | Teste de filtro/pesquisa: verificar se buscar por “Rotina” mostra só itens de rotina e se “Concluída/Não concluída” funciona sem misturar resultados. | Coletar feedback e corrigir melhorias: depois que colegas usarem, ajustar problemas comuns (ex.: botão pequeno demais no celular, filtro confuso, ordem das tarefas). |
| Determinar canais de contato para dúvidas/erros e tempo máximo de resposta. | Avaliar o custo e o tempo para alterar algo que já foi implementado. | Escrever código para corrigir erros urgentemente reportados em produção. | Testar se as correções de bugs não *quebraram* funcionalidades antigas que já funcionavam. | Atualizar bibliotecas, otimizar código antigo e fazer backups dos dados dos usuários. |

# Matriz de risco

![image.png](image.png)

🟢Aceitar - Risco é baixo e não exige uma ação específica.

🟨Observar - O risco ainda não preocupa, mas merece atenção

❗Monitorar - Risco relevante

🔥 Mitigar

| Risco (Descrição) | Probabilidade (Baixo/Alto) | Impacto (Baixo/Alto) | Plano de ação (o que faremos para prevenir ou remediar?) |
| --- | --- | --- | --- |
| E se todo o código desenvolvido em uma aula fosse perdido porque ninguém fez commit ou enviou o projeto para o GitHub. | Baixo | Alto | Conversar com todos sobre o risco e criar uma rotina e um hábito de salvar os trabalhos de forma segura. Colocar lembretes para não esquecer. |
| Internet indisponível no momento da entrega/apresentação. | Baixo | Alto | Salvar de forma off-line ou rotear internet do próprio celular. |
| Durante o desenvolvimento do EsTuDoList, os alunos que testaram o sistema gostaram da ideia e começaram a pedir um chat para conversar sobre as tarefas. | Alta | Alto | Falaria para eles que, devido ao nível de avanço do projeto, seria mais difícil e demorado de fazer, e perguntaria se seria totalmente necessário. |