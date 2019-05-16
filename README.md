<h1 align="center">VsCodeSettings4Django</h1>

<h2>Instalação</h2>
<p>Entre dentro da raiz do seu projeto django e cole a pasta.</p>
  
  ``` 
  my_project/.vscode/  
  ```

<h2>Quer entender as configurações? Então leia as instruções você mesmo!</h2>

<p>O arquivo .vscode/settings.json dentro do seu projeto define suas configurações do ambiente de desenvolvimento, de forma que estas configurações serão utilizadas apenas neste ambiente.</p>

<ul list-style="circle">

<li>
<h4>Ambiente virtual</h4>
<p>Todo projeto Django é construído dentro de um ambiente virtual que configuramos em nossas máquinas para que tenhamos um        maior controle das dependências. O vscode necessita deste caminho para habilitar diversos recursos. Esta configuração é          feita da seguinte forma:
</p>
       
 ``` 
 "python.pythonPath": "path-to-your-env", 
 ```
 
 <strong>Ex:</strong><br/>
 
 ``` 
  "python.pythonPath": "env/bin/python", 
 ```
 
<p>
Perceba o parâmetro recebido é o caminho para a instância do python dentro do ambiente virtual.   
</p>
</li>


<li>

<h4>Lint</h4>

<p>Ferramentas de <a href="https://www.google.com/search?ei=eu_dXPn5FZud5OUPh6easAc&q=what+is+lint+in+the+code&oq=what+is+lint+in+the+code&gs_l=psy-ab.3..0i71l8.6662.10026..10130...0.0..0.0.0.......0....1..gws-wiz.hmW_HKZPUkY" target+"_blank">lint</a> nos ajudam a manter nosso código limpo e padronizado. Elas nos avisam quando tem algo suspeito ou        quando cometemos um leve deslize.  
</p>

<p>Instale o seguinte dentro do seu ambiente virtual:</p>
  
<strong>utilizando pipenv</strong><br/>
```
$ pipenv install -dev pep8, pylint, autopep8
```

 <strong>sem pipenv</strong><br/>
```
(env)~ $ pip install pep8, pylint, autopep8
```

<p>O <a href="https://www.pylint.org/" target="_blank">pylint</a> será nosso linter e o <a href="https://pypi.org/project/pep8/" target="_blank">pep8</a> (pacote) irá ajudar a escrever um código seguindo as regras da própria <a href="https://www.python.org/dev/peps/pep-0008/">pep8</a>. E por fim, o <a href="https://pypi.org/project/autopep8/0.8/" target="__blank">autopep8</a> é uma ferramenta que formata o código automaticamente seguindo as regras da pep8. Aqui vão as configurações dos três:
</p>

<p>Primeiro falamos para o vscode que queremos utilizar tanto pylint quanto o pep8 para "lintar" nosso código.
```
"python.linting.pep8Enabled": true,
"python.linting.pylintEnabled": true,
```
<p>Às vezes salvamos um arquivo e algum errinho acaba passando despercebido. Para impedir isso, podemos dizer para o vscode para ele formatar nosso código quando o salvarmos. É aqui que o autopep8 se encaixa. Ele será a ferramenta que utilizaremos para isso. </p>

```
"python.formatting.provider": "autopep8",
  
"[python]": {
  "editor.formatOnSave": true,
  "editor.rulers": [79, 120],
},
```
<p>Agora, note que colocamos algumas configurações dentro da propriedade <i>[python]</i>. Isso define comportamentos do editor que funcionarão apenas em arquivos com a extensão da linguagem colocanda entre colchetes, no nosso caso o python. Aqui dizemos para o vscode formatar os arquivos ao salvar e definimos linhas guias laterais.
</li

</ul>
