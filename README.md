# Roteiro de teste
#### O presete documento tem por finalidade listar cenários e casos de testes para o sistema Nees, dessa forma descreverei a seguir alguns cenários e casos de testes, de modo geral tenho o intuito de descrever os cenários e casos de teste da maneira mais clara e objetva no qual acredito ser uma maneira eficiente e simples para compreesão

## Cenário 1: Login do professor no sistema
#### Descrição: Eu como um professor usuário do sistema desejo acessar a plataforma mobile.
 - ## Caso 1: Login com sucesso
     **Dado** Que sou um professor devidamente cadastrado no sistema possuindo email e senha
   
     **E** Acesso o app na sessão de login
   
     **E** Preencho os campos devidos de email e senha corretamente
   
     **Quando** Aciono o botão "Logar"
   
     **Então** Devo ser redirecionado para pagina inicial do app logado.

 - ## Caso 2: Login com usuário não cadastrado
      **Dado** Que sou um professor que não possuo cadastro no sistema
   
      **E** Acesso o app na sessão de login
   
      **E** Areencho os devidos campos de email e senha quaisquer
   
      **Quando** Aciono o botão "Logar"
   
      **Então** Devo ver a seguinte mensagem de alerta "Usuário/Senha não cadastrados"
      
 - ## Caso 3: Login com Email incorreto
      **Dado** Que sou um professor devidamente cadastrado no sistema possuindo email e senha
   
      **E** Acesso o app na sessão de login
   
      **E** Preencho os devidos campos de email com senha incorreta
   
      **Quando** Aciono o botão de logar
   
      **Então** Devo ver a seguinte mensagem de alerta "Email, tente novamente"

 - ## Caso 4: Login com senha incorreta
      **Dado** Que sou um professor devidamente cadastrado no sistema possuindo login e senha
   
      **E** Acesso o app na sessão de login
   
      **E** Preencho os devidos campos de login com senha incorreta
   
      **Quando** Aciono o botão de logar
   
      **Então** Devo ver a seguinte mensagem de alerta "Senha incorreta, tente novamente"

  - ## Caso 5: Login com dados em branco
      **Dado** Que sou um professor devidamente cadastrado no sistema
     
      **E** Acesso o app na sessão de login
     
      **E** Não preencho os campo de login e senha
     
      **Quando** Aciono o botão de logar
     
      **Então** Devo ver a seguinte mensagem nos devidos campos de login e senha "Preencha os campos corretamente".

  - ## Caso 6: Login com formato de email inválido
      **Dado** Que sou um professor devidamente cadastrado no sistema possuindo login e senha
       
      **E** Acesso o app na sessão de login
     
      **E** Preencho os devidos campos de email e senha com o email fora do formato adequando
     
      **Quando** Aciono o botão de logar
     
      **Então** Devo ver a seguinte mensagem de alerta "Email inválido, tente novamente"

## Cenário 2: Correção de atividade de um aluno
   #### Descrição: Eu como professor usuário da plataforma mobile desejo realizar a correção de uma atividade de um aluno
   - ## Caso 1: Envio de uma atividade para correção com sucesso.
      **Dado** Que sou um professor devidamente logado no sistema
     
      **E** Acesso a área para submissão de uma imagem de uma atividade para correção
     
      **E** Clico no campo "Envio de imagem"

      **E** Acesso minha camera do meu aparelho celular

      **E** Faço uma foto da atividade do aluno para correção

      **Quando** Aciono o botao "Enviar para correção"

      **Então** Devo poder visualizar na tela um documento contendo os acertos e erros desse aluno.

  - ## Caso 2: Envio de uma atividade para correção com campo de imagem vazio.
      **Dado** Que sou um professo devidamente logado no sistema

      **E** Acesso a área para submissão de uma imagem de uma atividade para correção

      **E** Não adiciono nenhuma imagem ao campo de envio de imagem

      **Quando** Aciono o botão "Enviar para correção"

      **Então** Devo receber a seguinte mensagem "Campos de imagem vazio, adicione uma imagem para correção".

 ## Cenário 3: Gerando atividades baseado no conteúdo e nível de dificildade.
   #### Descrição: Eu como professor usuário da plataforma mobile desejo gerar listas de atividades selecionando o conteúdo e niveis de dificuldade
   - ## Caso 1: Gerar lista de atividades por conteúdo e nível de difildade com sucesso.
       **Dado** Que sou um professor devidamente logado no sistema
     
       **E** Acesso a área de Atividades
       
       **E** Acesso Gerar atividades por nivel de dificuldade
     
       **E** Seleciono o conteúdo, nível de dificuldade e quantidade de questões

       **Quando** Aciono o botão "Gerar Atividade"

       **Então** Devo visualizar um arquivo contendo uma lista de atividade com a quantidade de questões selecionada e baseado no conteúdo e no nível de dificildade, sendo possível o download desse arquivo no formato pdf para impressão.

## Cenário 4: Listando grupo de alunos com a mesma dificildade
 #### Descrição: Eu como professor usuário da plataforma mobile, desejo gerar uma lista dos alunos que tem uma mesma dificuldade e assim poder gerar uma lista adequada para melhorias do desempenho desse grupo.
   - ## Caso 1: Gerando lista de alunos com a mesma dificuldade.

     **Dado** Que sou um professor devidamente logado no sistema.

     **E** Acesso a área de Relatórios
     
     **E** Seleciono Lista de Alunos com Dificildade

     **E** Seleciono a dificuldade que desejo obter a lista

     **Quando** Aciono o botão "Gerar Relatório"

     **Então** Devo obter um arquivo que me permita baixar um pdf para impressão, com a lista de alunos com a dificuldade selecionada.

   - ## Caso 2: Gerando lista de alunos com a mesma dificuldade com campos não preenchidos.
       **Dado** Que sou um professor devidamente logado no sistema.

       **E** Acesso a área de Relatórios

       **E** Seleciono Lista de Alunos com Dificildade

       **E** Deixo de selecionar os campos devidamente corretos

       **Quando** Aciono o botão "Gerar Relatório"

       **Então** Devo receber a seguinte mensagem "Campos devem ser preenchidos corretamente", os destacando campos não preenchidos.

- ## Caso 3: Gerando lista de alunos com a mesma dificuldade sem dados.
   **Dado** Que sou um professor devidamente logado no sistema.

   **E** Acesso a área de Relatórios

   **E** Seleciono Lista de Alunos com Dificildade

    **E** Seleciono a dificuldade que desejo obter a lista

    **Quando** Aciono o botão "Gerar Relatório"

    **Então** Devo receber a seguinte mensagem "Sem dados para essa seleção"
