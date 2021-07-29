<h1>Desafio final - programa Formação Tech Itaú</h1>
<span>Edição Pessoas com Deficiência</span>
<h2>Cadastro Pessoal - Atração</h2>
<h3>Autor</h3>
<h4>Wybson Santana dos santos</h4>
<h2>Desafio</h2>
<p>
Criar um formulário de cadastro para registrar dados pessoais.
<h2>Descrição</h2>
<p>
Este projeto foi desenvolvido com estrutura em HTML, estilização com CSS e funcionalidades aplicadas utilizando JavaScript, apresentando um formulário de cadastro subdividido com os seguintes grupos e campos:</p>
<h3>Dados pessoais</h3>
<ul>
<li>Nome;</li>
<li>Sobrenome;</li>
<li>CPF;</li>
<li>RG;</li>
<li>Sexo.</li>
</ul>
<h3>Informações de contato</h3>
<ul>
<li>E-mail;</li>
<li>Telefone celular;</li>
<li>Telefone fixo.</li>
</ul>
<h3>Endereço</h3>
<ul>
<li>CEP;</li>
<li>Logradouro;</li>
<li>Nº;</li>
<li>Complemento;</li>
<li>Bairro;</li>
<li>Cidade;</li>
<li>Estado.</li>
</ul>
<h2>Organização</h2>
<p>
Na construção do corpo da página foram utilizadas tags para definição do idioma, codificação, descrição, palavras-chave, autor, título etc. Já a separação do conteúdo foi realizada com as tags `header`, `main` e `footer`, não somente para garantir a semântica do HTML5, bem como para a manutenção de uma boa navegabilidade para usuários que utilizam leitores de tela.</p>
<p>
No cabeçalho foi adicionado um logotipo com um atributo `alt`, que informa aos usuários de leitores de tela o que aquela imagem representa, e uma `navbar` contendo o título principal da página envolto por uma tag `h1`.</p>
<p>
Na parte principal foi adicionada uma tag `h2` com uma <em>call to action</em> para a realização do cadastro e logo abaixo foi disponibilizado o formulário, que está subdividido nos grupos já informados acima; onde cada grupo definido com a tag `fieldset` recebe uma tag `legend` com marcação `h3` para definir o título do grupo e cada campo de preenchimento recebe uma tag `label` com marcação `h4` para definir o título do campo. No formulário ainda temos uma checkbox de privacidade e os botões para realizar o cadastro ou limpar os campos já preenchidos.</p>
<p>
No rodapé temos o nome do autor do projeto e uma lista de links que levam para as páginas do Programa Formação Tech Itaú, da Gama Academy e dos perfis do Linkedin e GitHub do desenvolvedor.</p>
<p>
A estilização do conteúdo foi feita utilizando folhas de estilo com propriedades como a `FlexBox` para alinhar e posicionar os elementos do HTML e outras propriedades como `background`, `font`, `color`, `margin`, `padding`, `border` etc, para alterar cores de preenchimento, fonte, espaçamento, margem, bordas entre outros atributos.</p>
<h2>Funcionalidades com JavaScript</h2>
<h3>checkbox de privacidade</h3>
<p>
Aqui, o botão de cadastro, que inicialmente é carregado como desativado, somente deve receber a condição de ativado caso o usuário marque a checkbox de privacidade concordando com o compartilhamento dos seus dados através do formulário; Um `querySelector` captura o status da checkbox e condiciona o botão de submit a ele.</p>
<h3>Limpeza dos campos do formulário</h3>
<p>
A limpeza de todos os campos do formulário poderá acontecer de três maneiras diferentes durante a navegação. A primeira delas é clicando no botão "Limpar campos", onde todos os dados preenchidos são excluídos, a checkbox de privacidade é desmarcada e uma função força o retorno do status desativado ao botão "Cadastrar". Uma outra maneira é realizando o recarregamento da página, pois uma função acionada `onload` na tag `body` realiza as mesmas ações anteriores. E, o formulário também é limpo com os mesmos parâmetros quando uma submissão é bem sucedida.</p>
<h3>Verificação do preenchimento dos campos obrigatórios</h3>
<p>
Sempre que o botão "Cadastrar" estiver ativo e for clicado pelo usuário, uma função fará a verificação do preenchimento dos campos obrigatórios e retornará uma mensagem de alerta contendo quais campos não foram preenchidos. Um array se encarrega de receber e armazenar esses dados e um alerta os exibe de acordo com duas condições diferentes:</p>
<p>
<ol>
<li>Se um único campo não foi preenchido, a mensagem é formatada no singular;</li>
<li>Caso dois ou mais campos não sejam preenchidos, a mensagem é formatada no plural exibindo todos os campos não preenchidos e separando o penúltimo campo e o último pela conjunção "e".</li></ol></p>
<h3>Validação do CPF</h3>
<p>
O campo do CPF aciona uma função assim que o foco do cursor sai do input e essa verifica se o número informado é ou não um número de CPF válido; caso não seja, um alerta é emitido na tela informando que o CPF é inválido. Obs: essa validação apenas verifica se o número atende a lógica que classifica como válido ou inválido e não faz referência a situação cadastral na Receita Federal.</p>
<h3>Validação do CEP</h3>
<p>
O campo do CEP aciona uma função ao cursor perder o foco do input e essa faz a verificação do número digitado através do banco de dados do ViaCEP. Caso o número informado não seja um CEP válido, um alerta é emitido na tela informando essa condição; caso retorne uma resposta positiva na verificação, um script carregado preenche até quatro campos do endereço: logradouro, bairro, cidade e estado.</p>
<h3>Máscaras para campos numéricos</h3>
<p>
Os campos de CPF, telefone celular, telefone fixo, CEP e número do endereço acionam funções que inibem a digitação de caractéres não numéricos nesses campos e ainda retornam o valor digitado já formatado para o padrão de cada um deles: o CPF retorna no padrão xxx.xxx.xxx-xx, o de telefone celular retorna o padrão (xx) xxxxx-xxxx, o de telefone fixo (xx) xxxx-xxxx, o de CEP xxxxx-xxx e o número do endereço adiciona o separador de milhar quando 4, 5 ou 6 dígitos são informados.</p>
<h3>Fetch API enviando dados para WebHook</h3>
<p>
Caso todos os campos obrigatórios do formulário sejam preenchidos, ao clicar no botão "Cadastrar", uma Fetch API envia os dados para o WebHook.site através de um JSON com método POST e um alerta de cadastro bem sucedido é emitido na tela personalizado com o nome que foi preenchido no formulário.</p>
<h2>Referências</h2>
<p>
<ul>
<li>Mentorias realizadas pelo prof. Douglas Morais e conteúdos disponibilizados pela Gama Academy durante a trilha preparatória do Programa Formação Tech Itaú;</li>
<li>Tutoriais disponíveis nos sites W3Schools e Free Code Camp;</li>
<li>Outros materiais encontrados em fóruns, blogs e apostilas.</li></p>