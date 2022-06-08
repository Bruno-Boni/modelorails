<h1 align="center"> Modelo Rails </h1>
  
 <hr/>
                                                           
<h2 align="center"> Como utilizador o Modelo Rails? <h2>
	
---
	
# O que é o Modelo Rails?
	
Eu já tive muitos problemas na hora de tentar criar um ambiente para desenvolver minhas aplicações Rails, então eu decidi criar este arquivo que servirá como modelo para projetos futuros já que ele possui todas as funcionalidades básicas e essenciais que eu precisarei futuramente.

---
	
## Configurando o Javascript
   1. Os arquivos Javascript de toda a aplicação estão na pasta app/javascript separados por pastas. </br> </br>
   2. Para criar uma pasta onde terão todos os arquivos javascript usados em uma página específica, faça: 
   * Crie uma pasta em app/javascript e coloque todos os arquivos .js com as suas pastas lá. </br>
   * Vá em app/javascript/application.js e importe as pastas com os respectivos arquivos .js que você criou.  </br>
     Por exemplo, se você criou uma pasta para 
     home com os arquivos header.js e footer.js, você deverá escrever neste arquivo application.js as seguintes coisas: import "./home/header", import "./home/footer".

<hr/>


## Configurando o CSS e o SASS

1. Os arquivos CSS e SASS estão na pasta app/assets/stylesheets separados por pastas. </br> </br>
2. Para criar uma pasta onde terão todos os arquivos CSS usados em uma página específica, faça: </br>
* Crie uma pasta em app/assets/stylesheets/CSS e coloque todos os arquivos .css com as suas respectivas pastas. 
* Vá em app/config/manifest.js e use o comando para referenciar a pasta onde estão os arquivos .css.
Por exemplo, você criou uma pasta chamada home, então, neste arquivo manifest.js, você irá escrever: 
//= link_directory ../stylesheets/CSS/home .css. </br>
* Vá em app/assets/stylesheets/CSS e no arquivo estilos.css importe todos os seus arquivos .css usando @import url  </br>
3. Para adicionar arquivos SASS na sua aplicação, coloque todos os arquivos SASS na pasta app/assets/stylesheets/SASS e no arquivo estilos.scss importe os seus arquivos usando @import.
4. Os arquivos .css compilados do SASS estão em SASS/compilacoes.
5. Se por algum acaso algum seletor do CSS não funcionar corretamente, é por causa da interferência do Bootstrap, basta escrever !important na frente da propriedade antes do ;
---

## Configurando o banco de dados

1. Esta aplicação utiliza o PostgreSQL.
2. Você precisa modificar o arquivo database.yml com a sua senha e o seu usuário do PostgreSQL para que a sua aplicação conecte corretamente com o banco de dados. <br/> 
3. No arquivo database.yml em config/database.yml basta substituir os nomes seuusuarioposgresql e suasenhapostgresql pelos valores corretos.

---

## Footer e Header

1. Na pasta app/views/layouts estão os arquivos _footer.html.erb e _header.html.erb que são respectivamente o footer e o header da página inicial da aplicação, também conhecida como home.
2. O footer e o header serão os mesmos para todas as páginas do site.
3. O arquivo HTML com o código que fica entre o header e o footer da página inicial está em app/views/application/index.html.erb.

---

## Compass 

Para ativar o Compass, digite compass watch no root da aplicação.

--- 

## Heroku

Esta aplicação funciona perfeita com Heroku

---

## Observações

Esta aplicação possui Bootstrap e utiliza o importmaps para separar os arquivos javascript em pastas diferentes

