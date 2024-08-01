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

## Histórias do Usuário 👩👨

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

## História de Usuário 6: Visualizar Detalhes do Curso

**Como** interessado,  
**Eu quero** clicar no nome de um curso na lista de cursos,  
**Para que** eu possa ver os detalhes completos do curso.

### Critérios de Aceitação:
1. Ao clicar no nome de um curso na lista de cursos, deve-se abrir uma página com os detalhes do curso.
2. A página de detalhes deve incluir nome do curso, descrição, instrutor, URL da imagem de capa, datas de início e fim, número de vagas, e tipo de curso.

```

## Cenários e Casos de Teste 🖥

<b>Cadastrar curso</b><br>
<em>Cenários de Sucesso:</em><br>
<blockquote><ol>
  <li>Cadastro de curso com todos os campos preenchidos corretamente</li>
  <li>Cadastro de curso com data de início e fim corretas</li>
  <li>Cadastro de curso com URL de imagem válida</li>
</ol></blockquote>
<br>
<em>Cenários de Erro:</em><br>
<blockquote><ol>
  <li>Falha no cadastro de curso com campo obrigtório vazio</li>
  <li>Falha no cadastro de curso com data de fim anterior à data de início</li>
  <li>Falha no cadastro de curso com URL de imagem inválida</li>
  <li>Falha no cadastro de curso com número de vagas negativo</li>
</ol><br></blockquote>
<b>Listar cursos</b><br>
<em>Cenários de Sucesso:</em><br>
<blockquote><ol>
  <li>Listar todos os cursos disponíveis</li>
  <li>Visualizar detalhes de um curso</li>
</ol></blockquote>
<br>
<em>Cenários de Erro:</em><br>
<blockquote><ol>
  <li>Falha na atualização de novos cursos</li>
  <li>Falha na visualização dos cursos</li>
</ol></blockquote>


## Passo a passo para a execução dos testes 📑

<b>Preparação do Ambiente</b><br>
  <blockquote><i>Acesse o Site:</i> Abra o navegador e acesse o site fornecido para o desafio: Beedoo AI Learning.<br>
  <i>Certifique-se de que os dados necessários estão disponíveis:</i> Garanta que você tenha acesso a todas as informações e permissões necessárias para realizar o cadastro e listar cursos.<br><br></blockquote>
<b>Execução dos Casos de Teste</b><br>
  <i>Cadastro de Curso</i><br>
    <blockquote>Acessar a Página de Cadastro de Curso:<br>
    Clique na opção "Cadastrar Curso" no canto superior direito.<br><br></blockquote>
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
  <i>Visualizar Detalhes do Curso:</i><br>
    <blockquote>Clique no nome de um curso listado.<br>
    Confirme se a página de detalhes do curso exibe todas as informações corretamente (nome, descrição, instrutor, URL da imagem de capa, datas de início e fim, número de vagas, e tipo de curso).</blockquote>

## Links 🔗

[Planilha](https://docs.google.com/spreadsheets/d/19Dex-_tBeaeDBHPwLD0uBl-XhqSXhnAHVD4q49DShLU/edit?usp=sharing) <br>
[Evidências](https://drive.google.com/drive/folders/1qpJP1V3aqK9uEojMvoir4tLXjFckOInq?usp=drive_link)

## Autora ✨

Anna Ferraro - [(Linkedin)](https://www.linkedin.com/in/anna-ferraro-339266136/)

