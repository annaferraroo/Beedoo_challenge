# Descrição do Projeto 📜

<p>O projeto Beedoo QA Challenge é uma aplicação web com foco em gestão de cursos online. Esta plataforma simples e intuitiva permite que os professores cadastrem cursos, e também que os interessados visualizem uma lista de cursos disponíveis.</p>
<p>O objetivo principal é trazer a facilidade tanto para quem cadastra o curso, quanto para a visualização de quem está interessado em ingressar no curso.</p>

## Decisões Tomadas para as Histórias de Usuário 💡

<b>Identificação das Principais Funcionalidades:</b><br>
  <blockquote>Dividimos as histórias de usuário em duas funcionalidades principais: Cadastro de Curso e Listagem de Cursos, para focar nos requisitos específicos de cada uma.</blockquote><br>
<b>Definição de Campos Obrigatórios e Validação:</b><br>
  <blockquote>Especificamos que todos os campos obrigatórios devem ser validados e fornecer feedback apropriado ao usuário, garantindo a integridade dos dados e melhorando a experiência do usuário.</blockquote><br>
<b>Manutenção da Experiência do Usuário:</b> <br>
  <blockquote>Implementamos mensagens de confirmação para ações bem-sucedidas e mensagens de erro detalhadas para entradas inválidas, aumentando a usabilidade e a satisfação do usuário.</blockquote><br>
<b>Consideração para Casos de Erro Comuns:</b><br>
  <blockquote>Incluímos histórias de usuário que abordam cenários de erro comuns, como datas inválidas e URLs incorretas, para garantir que o sistema lide adequadamente com essas situações.</blockquote><br>
<b>Uso de Gherkin para Especificação de Testes:</b><br>
  <blockquote>Optamos por escrever casos de teste em Gherkin para facilitar a automação e a compreensão dos testes por todos os stakeholders.</blockquote>

## Histórias de Usuário 👩👨

<b>Funcionalidades Principais:</b> <br>
<blockquote><ul>
  <li>Listar Cursos: permite que os interessados visualizem todos os cursos cadastrados na plataforma.</li>
  <li>Cadastrar Curso: permite que os professores adicionem novos cursos, com os campos necessários para cadastro.</li>
</ul></blockquote>
<br>
<b>Usuários:</b><br>
<blockquote><ul>
  <li>Professor: quem irá cadastrar os cursos na plataforma.</li>
  <li>Interessado: quem irá visualizar a lista de cursos.</li>
</ul></blockquote>
<br>
<b>Definição do User Story</b><br>
<blockquote><ul>
  <li><b>Como</b> professor <b>eu quero</b> cadastrar cursos <b>para que</b> os interessados possam ver quais cursos oferecemos.</li>
  <li><b>Como</b> interessado <b>eu quero</b> ver os cursos disponíveis <b>para que</b> eu possa escolher em qual vou me cadastrar.</li>
</ul></blockquote><br>

```markdown

## História de Usuário 1: Cadastro de Curso

**Como** professor,  
**Eu quero** cadastrar um novo curso,  
**Para que** ele esteja disponível para os alunos no sistema.

### Critérios de Aceitação:
1. Todos os campos obrigatórios devem ser preenchidos corretamente.
2. O campo "Data de início" deve ser anterior ao campo "Data de fim".
3. A URL da imagem de capa deve ser válida.
4. O número de vagas deve ser um valor positivo.
5. Após o cadastro bem-sucedido, uma mensagem de confirmação "Curso cadastrado com sucesso" deve ser exibida.
6. Em caso de erro, mensagens de erro apropriadas devem ser exibidas.

## História de Usuário 2: Listar Cursos

**Como** interessado,  
**Eu quero** visualizar uma lista de cursos disponíveis,  
**Para que** eu possa escolher um curso para me inscrever.

### Critérios de Aceitação:
1. A página inicial deve listar todos os cursos disponíveis.
2. Cada curso listado deve mostrar pelo menos o nome do curso e a descrição.
3. Ao clicar no nome de um curso, os detalhes completos do curso devem ser exibidos.

## História de Usuário 3: Validação de Campos no Cadastro de Curso

**Como** professor,  
**Eu quero** que o sistema valide os campos do formulário de cadastro de curso,  
**Para que** eu não consiga submeter dados incorretos ou incompletos.

### Critérios de Aceitação:
1. O campo "Nome do Curso" é obrigatório.
2. O campo "Descrição do Curso" é obrigatório.
3. O campo "Instrutor" é obrigatório.
4. O campo "URL da imagem de capa" deve ser uma URL válida.
5. O campo "Data de início" é obrigatório.
6. O campo "Data de fim" é obrigatório e deve ser posterior à data de início.
7. O campo "Número de vagas" é obrigatório e deve ser um número positivo.
8. O campo "Tipo de curso" é obrigatório.

## História de Usuário 4: Feedback de Erro no Cadastro de Curso

**Como** professor,  
**Eu quero** receber mensagens de erro claras quando tento cadastrar um curso com dados inválidos,  
**Para que** eu saiba exatamente o que precisa ser corrigido.

### Critérios de Aceitação:
1. Mensagens de erro devem ser exibidas próximo ao campo com erro.
2. A mensagem deve descrever claramente o problema (por exemplo, "O campo Nome do Curso é obrigatório").
3. Mensagens de erro devem ser exibidas para todos os campos obrigatórios não preenchidos ou preenchidos incorretamente.

## História de Usuário 5: Confirmação de Sucesso no Cadastro de Curso

**Como** professor,  
**Eu quero** receber uma mensagem de confirmação quando eu cadastrar um curso com sucesso,  
**Para que** eu saiba que o curso foi adicionado ao sistema.

### Critérios de Aceitação:
1. Uma mensagem "Curso cadastrado com sucesso" deve ser exibida após o cadastro bem-sucedido.
2. A mensagem deve ser clara e visível.

## História de Usuário 6: Exclusão de Curso

**Como** professor,
**Eu quero** poder excluir um curso
**Para que** caso cadastre errado ou o curso não esteja mais disponível, eu possa excluí-lo

### Critérios de Aceitação:
1. Uma mensagem "Curso excluído com sucesso" deve ser exibida após a exclusão do curso.
2. O curso não deve mais ser exibido na lista de cursos.

```

## Cenários de Teste 🖥

<b>Cadastrar curso</b><br>
<em>Cenários de Sucesso:</em><br>
<blockquote><ol>
  <li>Cadastro de curso com todos os campos preenchidos corretamente</li>
  <li>Cadastro de curso com data de início e fim corretas</li>
  <li>Cadastro de curso com URL de imagem válida</li>
  <li>Cadastro de curso com endereço preenchido, caso tipo de teste seja presencial</li>
  <li>Cadastro de curso com link de inscrição preenchido, caso tipo de teste seja online</li>
</ol></blockquote>
<br>
<em>Cenários de Erro:</em><br>
<blockquote><ol>
  <li>Falha no cadastro de curso com campo obrigtório vazio</li>
  <li>Falha no cadastro de curso com data de fim anterior à data de início</li>
  <li>Falha no cadastro de curso com URL de imagem inválida</li>
  <li>Falha no cadastro de curso com número de vagas negativo</li>
  <li>Falha no cadastro de curso sem endereço preenchido, caso o tipo de curso seja presencial</li>
  <li>Falaha no cadastro de curso sem link de inscrição preenchido, caso o tipo de curso seja online</li>
</ol><br></blockquote>
<b>Listar cursos</b><br>
<em>Cenários de Sucesso:</em><br>
<blockquote><ol>
  <li>Listar todos os cursos disponíveis</li>
</ol></blockquote>
<br>
<em>Cenários de Erro:</em><br>
<blockquote><ol>
  <li>Falha na atualização de novos cursos</li>
</ol></blockquote>

## Casos de Teste

<b>Casos de Teste - Cadastrar Curso</b>

CT001.001 - Cadastro de Curso com todos os campos preenchidos corretamente.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero cadastrar um curso preenchendo todos os campos corretamente<br>
  Para que o curso seja registrado no sistema<br>
<br>
Cenário: Cadastro de curso com todos os campos preenchidos<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo a mensagem "Curso cadastrado com sucesso"<br>
  E o curso é cadastrado e volta à tela inicial </blockquote>

CT001.002 - Cadastro de Curso com o campo "Nome do Curso" em branco.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando o campo "Nome do Curso" estiver em branco<br>
  Para que eu saiba que o campo é obrigatório<br>
<br>
Cenário: Campo "Nome do Curso" em branco<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente exceto "Nome do Curso"<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo Nome do Curso é obrigatório"<br>
  E o curso não é cadastrado </blockquote>

CT001.003 - Cadastro de Curso com o campo "Descrição do Curso" em branco.
<blockquote> Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando o campo "Descrição do Curso" estiver em branco<br>
  Para que eu saiba que o campo é obrigatório<br>
<br>
Cenário: Campo "Descrição do Curso" em branco<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente exceto "Descrição do Curso"<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo Descrição do Curso é obrigatório"<br>
  E o curso não é cadastrado </blockquote>

CT001.004 - Cadastro de Curso com o campo "Instrutor" em branco.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando o campo "Instrutor" estiver em branco<br>
  Para que eu saiba que o campo é obrigatório<br>
<br>
Cenário: Campo "Instrutor" em branco<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente exceto "Instrutor"<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo Instrutor é obrigatório"<br>
  E o curso não é cadastrado</blockquote>

CT001.005 - Cadastro de Curso com o campo "Data de Início" em branco.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando o campo "Data de Início" estiver em branco<br>
  Para que eu saiba que o campo é obrigatório<br>
<br>
Cenário: Campo "Data de Início" em branco<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente exceto "Data de Início"<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo Data de Início é obrigatório"<br>
  E o curso não é cadastrado</blockquote>

CT001.006 - Cadastro de Curso com o campo "Data de Fim" em branco.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando o campo "Data de Fim" estiver em branco<br>
  Para que eu saiba que o campo é obrigatório<br>
<br>
Cenário: Campo "Data de Fim" em branco<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente exceto "Data de Fim"<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo Data de Fim é obrigatório"<br>
  E o curso não é cadastrado</blockquote>

CT001.007 - Cadastro de Curso com o campo "URL da Imagem de Capa" em branco.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando o campo "URL da Imagem de Capa" estiver em branco<br>
  Para que eu saiba que o campo é obrigatório<br>
<br>
Cenário: Campo "URL da Imagem de Capa" em branco<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente exceto "URL da Imagem de Capa"<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo URL da Imagem de Capa é obrigatório"<br>
  E o curso não é cadastrado</blockquote>

CT001.008 - Cadastro de Curso com o campo "Número de Vagas" em branco.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando o campo "Número de Vagas" estiver em branco<br>
  Para que eu saiba que o campo é obrigatório<br>
<br>
Cenário: Campo "Número de Vagas" em branco<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente exceto "Número de Vagas"<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo Número de Vagas é obrigatório"<br>
  E o curso não é cadastrado</blockquote>

CT001.009 - Cadastro de Curso com o campo "Tipo de Curso" sem selecionar opção.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando o campo "Tipo de Curso" não tiver uma opção selecionada<br>
  Para que eu saiba que o campo é obrigatório<br>
<br>
Cenário: Campo "Tipo de Curso" sem selecionar opção<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente exceto "Tipo de Curso"<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo Tipo de Curso é obrigatório"<br>
  E o curso não é cadastrado</blockquote>

CT001.010 - Cadastro de Curso com o campo "Tipo de Curso" selecionado como "Presencial" sem preencher o Endereço.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando o campo "Tipo de Curso" estiver selecionado como "Presencial" sem preencher o endereço<br>
  Para que eu saiba que o campo é obrigatório<br>
<br>
Cenário: Tipo de Curso selecionado como "Presencial" sem endereço<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente<br>
  E seleciono a opção "Presencial" do campo "Tipo de Curso"<br>
  E deixo o campo "Endereço" em branco<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo Endereço é obrigatório"<br>
  E o curso não é cadastrado</blockquote>

CT001.011 - Cadastro de Curso com o campo "Tipo de Curso" selecionado como "Online" sem preencher o Link de Inscrição.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando o campo "Tipo de Curso" estiver selecionado como "Online" sem preencher o link de inscrição<br>
  Para que eu saiba que o campo é obrigatório<br>
<br>
Cenário: Tipo de Curso selecionado como "Online" sem link de inscrição<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente<br>
  E seleciono a opção "Online" do campo "Tipo de Curso"<br>
  E deixo o campo "Link de Inscrição" em branco<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo Link de Inscrição é obrigatório"<br>
  E o curso não é cadastrado</blockquote>

CT001.012 - Cadastro de Curso com o campo "Data de Fim" anterior a "Data de Início".
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando a "Data de Fim" for anterior à "Data de Início"<br>
  Para que eu saiba que as datas estão corretas<br>
<br>
Cenário: Data de Fim anterior à Data de Início<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente<br>
  E preencho a "Data de Fim" com uma data anterior à "Data de Início"<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo Data de Fim não pode ter data anterior ao campo Data de Início"<br>
  E o curso não é cadastrado</blockquote>

CT001.013 - Cadastro de Curso com o campo "URL da Imagem de Capa" com uma URL inválida.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando a "URL da Imagem de Capa" for inválida<br>
  Para que eu saiba que o campo está correto<br>
<br>
Cenário: URL da Imagem de Capa inválida<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente<br>
  E preencho o campo "URL da Imagem de Capa" com uma URL inválida<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo URL de Imagem de Capa deve conter uma URL válida"<br>
  E o curso não é cadastrado</blockquote>

CT001.014 - Cadastro de Curso com o campo "Número de Vagas" negativo.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando o "Número de Vagas" for negativo<br>
  Para que eu saiba que o campo está correto<br>
<br>
Cenário: Número de Vagas negativo<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu preencho todos os campos corretamente<br>
  E preencho o campo "Número de Vagas" com um número negativo<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "O campo Número de Vagas não pode ser menor que 1"<br>
  E o curso não é cadastrado</blockquote>

CT001.015 - Cadastro de Curso com todos os campo em branco.
<blockquote>Funcionalidade: Cadastro de Curso<br>
  Como professor<br>
  Eu quero ver uma mensagem de erro quando todos os campos estiverem em branco<br>
  Para que eu saiba que os campos obrigatórios foram preenchidos<br>
<br>
Cenário: Todos os campos em branco<br>
  Dado que eu estou na página de cadastro de curso<br>
  Quando eu deixo todos os campos em branco<br>
  E clico no botão "Cadastrar Curso"<br>
  Então eu vejo uma mensagem de erro "Mais de um campo obrigatório em branco"<br>
  E o curso não é cadastrado</blockquote>

<b>Casos de Teste - Listar Cursos</b>

CT002.001 - Visualizar lista de cursos
<blockquote>Funcionalidade: Lista de Cursos<br>
  Como interessado<br>
  Eu quero visualizar a lista de cursos disponíveis<br>
  Para que eu possa ver quais cursos estão disponíveis<br>
<br>
Cenário: Visualizar lista de cursos<br>
  Dado que eu estou na página "Listar Cursos"<br>
  Quando eu visualizo a página<br>
  Então eu vejo a lista de cursos</blockquote>

CT002.002 - Exclusão de curso
<blockquote>Funcionalidade: Lista de Cursos<br>
  Como professor<br>
  Eu quero excluir um curso da lista<br>
  Para que o curso não esteja mais disponível<br>
<br>
Cenário: Excluir curso<br>
  Dado que eu estou na página "Listar Cursos"<br>
  E eu encontro o curso que desejo excluir<br>
  Quando eu clico em "Excluir Curso"<br>
  Então eu vejo a mensagem "Curso excluído com sucesso"<br>
  E o curso não aparece mais na lista</blockquote>


## Passo a passo para a execução dos testes 📑

<b>Preparação do Ambiente</b><br>
  <blockquote><i>Acesse o Site:</i> Abra o navegador e acesse o site fornecido para o desafio: Beedoo AI Learning.<br>
  <i>Certifique-se de que os dados necessários estão disponíveis:</i> Garanta que você tenha acesso a todas as informações e permissões necessárias para realizar o cadastro e listar cursos.<br><br></blockquote>
<b>Execução dos Casos de Teste</b><br>
  <i>Cadastro de Curso</i><br>
    <blockquote>Acessar a Página de Cadastro de Curso:<br>
    Clique na seunda opção "Cadastrar Curso" no canto superior direito.<br><br></blockquote>
  <i>Preencher o Formulário de Cadastro:</i><br>
    <blockquote>Nome do Curso: Insira um nome válido.<br>
    Descrição do Curso: Insira uma descrição válida.<br>
    Instrutor: Insira o nome do instrutor.<br>
    URL da imagem de capa: Insira uma URL válida de uma imagem.<br>
    Data de início: Selecione uma data no formato correto.<br>
    Data de fim: Selecione uma data posterior à data de início.<br>
    Número de vagas: Insira um número inteiro positivo.<br>
    Tipo de curso: Selecione uma opção válida no menu suspenso.<br><br></blockquote>
  <i>Submeter o Formulário:</i><br>
    <blockquote>Clique no botão de "Salvar" ou "Cadastrar".<br><br></blockquote>
  <i>Verificar Mensagem de Sucesso:</i><br>
    <blockquote>Confirme se a mensagem de sucesso "Curso cadastrado com sucesso" é exibida.<br><br></blockquote>
  <i>Verificar Mensagens de Erro (se aplicável):</i><br>
    <blockquote>Submeta o formulário com dados inválidos e verifique se as mensagens de erro apropriadas são exibidas.<br>
    Listagem de Cursos<br><br></blockquote>
  <i>Acessar a Página Inicial:</i><br>
    <blockquote>Clique na opção "Listar Cursos" no canto superior direito.<br><br></blockquote>
  <i>Verificar Listagem de Cursos:</i><br>
    <blockquote>Confirme se todos os cursos cadastrados estão listados.<br>
    Verifique se cada curso listado mostra pelo menos o nome e a descrição.<br><br></blockquote>
  <i>Excluir Curso</i><br>
    <blockquote>Acessar a Página Lista de Curso:<br>
    Clique na primeira opção "Listar Curso" no canto superior direito.<br><br></blockquote>
  <i>Encontrar o curso desejado:</i><br>
    <blockquote>Na Lista de Cursos, ache o curso desejado para excluí-lo<br><br></blockquote>
  <i>Excluir o curso:</i><br>
    <blockquote>Clique no botão de "Excluir Curso" no curso desejado.<br><br></blockquote>
  <i>Verificar Mensagem de Sucesso:</i><br>
    <blockquote>Confirme se a mensagem de sucesso "Curso excluído com sucesso" é exibida.<br><br></blockquote>

## Falhas 🚩

<ul>
  <li>Não existe login para diferenciar quem pode cadastrar um curso(professor) e quem pode apenas visualizar os cursos disponíveis(interessado). </li>
  <li>Não existe validação nos campos de cadastro</li>
  <li>Ao voltar a página mostrar erro 404</li>
  <li>Após aparecer o erro 404, se clicar em "Back to our site" dá erro 404 novamente</li>
  <li>Alguns cursos não retornaram a imaagem de capa, mesmo sendo uma URL válida</li>
</ul>

## Links 🔗

[Planilha](https://docs.google.com/spreadsheets/d/19Dex-_tBeaeDBHPwLD0uBl-XhqSXhnAHVD4q49DShLU/edit?usp=sharing) <br>
[Evidências](https://drive.google.com/drive/folders/1qpJP1V3aqK9uEojMvoir4tLXjFckOInq?usp=drive_link)

## Autora ✨

Anna Ferraro - [(Linkedin)](https://www.linkedin.com/in/anna-ferraro-339266136/)

