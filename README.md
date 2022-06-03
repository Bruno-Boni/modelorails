                                                    Modelo Rails
                                                            

  Como utilizar o Modelo Rails?
  
    1)Os arquivos Javascript de toda a aplicação estão na pasta app/javascript separados por pastas.
    2)Os arquivos CSS e SASS estão na pasta app/assets/stylesheets separados por pastas.
    3)O modelorails é munido de Bootstrap e utiliza o importmap para separar os arquivos Javascript em pastas diferentes.
    4)Na pasta app/views/layouts estão os arquivos _footer.html.erb e _header.html.erb que são respectivamente o footer e o header da página inicial da aplicação, também conhecida como home.
    5)o arquivo HTML com o código que fica entre o header e o footer da página inicial está em app/views/application/index.html.erb.
    6)O footer e o header serão os mesmos para todas as páginas do site.
    7)Para criar uma pasta onde terão todos os arquivos javascript usados em uma página específica, faça:
    1-Crie uma pasta em app/javascript e coloque todos os arquivos .js com as suas pastas lá.
    2-Vá em app/javascript/application.js e importe as pastas com os respectivos arquivos .js que você criou. Por exemplo, se você criou uma pasta para home com os arquivos header.js e footer.js, você deverá escrever neste arquivo application.js as seguintes coisas: import "./home/header", import "./home/footer".
    8)Para criar uma pasta onde terão todos os arquivos CSS usados em uma página específica, faça:
    1-Crie uma pasta em app/assets/stylesheets/CSS e coloque todos os arquivos .css com as suas respectivas pastas.
    2-Vá em app/config/manifest.js e use o comando para referenciar a pasta onde estão os arquivos .css. Por exemplo, você criou uma pasta chamada home, então, neste arquivo manifest.js, você irá escrever: 
    //= link_directory ../stylesheets/CSS/home .css
    3-Vá em app/assets/stylesheets/CSS e no arquivo estilos.css importe todos os seus arquivos .css usando @import url
    9)Você precisa modificar o arquivo database.yml com a sua senha e o seu usuário do PostgreSQL para que a sua aplicação conecte corretamente com o banco de dados. Neste arquivo database.yml em config/database.yml basta substituir os nomes seuusuarioposgresql e suasenhapostgresql pelos valores corretos.
    10)Para adicionar arquivos SASS na sua aplicação, coloque todos os arquivos SASS na pasta app/assets/stylesheets/SASS e no arquivo estilos.scss importe os seus arquivos usando @import.
    11)Este arquivo funciona perfeitamente com Heroku.
    12)No VSCode, coloque o local para os arquivos .css e .map gerados pelo seu compilador de SASS serem salvos na pasta Sass/compilacoes.
