<h1 align="center">VsCodeSettings4Django</h1>

<h2>Instalação</h2>
<p>Entre dentro da raiz do seu projeto django e cole a pasta.</p>
  
  ``` my_project/.vscode/  ```

<h2>Quer entender as configurações? Então leia as instruções você mesmo!</h2>

<p>O arquivo .vscode/settings.json dentro do seu projeto define as configurações do ambiente de desenvolvimento para aquele projeto. Sendo assim, as configurações setadas neste arquivo serão usadas apenas no ambiente deste projeto.</p>

<ul list-style="circle">

<li>
<h4>Ambiente virtual</h4>
<p>Todo projeto Django é construído dentro de um ambiente virtual que configuramos em nossas máquinas para que tenhamos um        maior controle das dependências e o vscode necessita do caminho para habilitar diversos recursos. Esta configuração é          feita por meio do seguinte parâmetro:
</p>
       
 ``` "python.pythonPath": "path-to-your-env", ```
 
 <strong>Ex:</strong><br/>
 
 ``` "python.pythonPath": "env/bin/python", ```
 
<p>
Perceba o parâmetro recebido é o caminho para a instância do python dentro do ambiente virtual.   
</p>
</li>

</ul>
