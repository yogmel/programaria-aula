# Resumo da aula de formulários
Formulários são elementos de HTML que são utilizados para capturar dados dos usuários, através de campos de digitação. 

## Anatomia básica de formulário
```html
<form action="obrigada.html" method="GET">
    <input type="email" placeholder="Seu email">
    <input type="submit" value="Inscrever-se na Newsletter">
</form>
```

Na tag form, o atributo **action** define o que será feito após a submissão bem sucedida do formulário. A URL definida pode ser uma tela de agradecimento ou um script de execução para gravação de dados no backend. Se não há action, após submissão, a mesma página será carregada.
Além disso, o atributo **method** define qual o método de envio dos dados para o servidor. O outro tipo é o POST.

Dentro do formulário, podem haver várias tags de captura de dados do usuário. As mais comuns são:
### input email
```html
<input type="email" name="email" placeholder="Seu email">
```
Captura o email do usuário. Quando se define o type="email", o próprio navegador faz uma verificação simples do input do dado.
O atributo placeholder permite a adição de um texto explicativo sobre qual tipo de dado deve ser inserido no campo.

> O atributo **name** está presente em todos os campos de inserção de dados do usuário e **não** devem ser esquecidos. Ele é uma informação fundamental para o envio de dados para o servidor.


### input text
```html
<input type="text" name="nome" placeholder="Seu nome">
```
Os inputs de tipo "text" aceitam todo tipo de textos curtos dentro deles. Portanto, pode-se capturar nome, sobrenome, profissão etc do usuário.


### select
 ```html
<select name="assunto">
    <option value="contato">Contato</option>
    <option value="sugestao">Sugestão</option>
    <option value="critica">Crítica</option>
</select>
```
O select permite a apresentação de opções de dados a serem escolhidos pelo usuário. Dentro da tag select, deve-se determinar as opções através de tags option.
O atributo value nas tags option define o valor que é enviado para o backend.


### textarea
```html
<textarea name="mensagem" cols="30" rows="10"></textarea>
```
Textarea é uma tag que permite a digitação de um texto maior por parte do usuário. Os atributos cols e rows são opcionais e definem o tamanho padrão da caixa de texto.


### input submit
```html
<input type="submit" value="Enviar Mensagem">
```
Tag necessária para que haja submissão do formulário. Trata-se de um botão que o usuário pode clicar para efetuar o ato de envio de form. O value, nesse caso, age como 'placeholder';


### label
É também importante acompanhar as tags de input por outra tag que se chama label. Ela serve como auxiliar para informar ao usuário que tipo de dado é esperado dele.
```html
<label for="name">Name</label>
<input type="text" name="name" placeholder="Seu nome">
```
O atributo 'for' no label deve ter o mesmo valor do name do input correspondente.


> Para a estrutura de HTML de um formulário simples, veja a pasta 'exercicio-form'
