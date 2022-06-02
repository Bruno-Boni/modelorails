                                                          Modelo Rails
	*Como utilizar o Modelo Rails?

	1) Os arquivos Javascript de toda a aplicação estão na pasta app/javascript separados por pastas.
	2)Os arquivos CSS estão na pasta app/stylesheets separados por pastas.
	3)Este arquivo é munido de Bootstrap e utiliza o importmap para separar os arquivos Javascript em pastas diferentes.
	4)Na pasta app/views/layouts estão os arquivos _footer.html.erb e _header.html.erb que são respectivamente o footer e o header da página inicial da aplicação, também conhecida como home.
	5)o arquivo HTML central que fica entre o header e o footer da página inicial está em app/views/application/index.html.erb.
	6)O footer e o header serão os mesmos para todas as páginas do site.
	7)Para criar uma pasta onde terão todos os arquivos javascript usados em uma página específica, faça:
	1-Crie uma pasta em app/javascript e coloque todos os arquivos .js lá.
	2-Vá em app/javascript/application.js e importe a pasta com os respectivos arquivos .js que você criou lá. Por exemplo, se você criou uma pasta para home com os arquivos header.js e footer.js, você deverá escrever neste arquivo application.js as seguintes coisas: import "home/header", import "home/footer".
	8)Para criar uma pasta onde terão todos os arquivos CSS usados em uma página específica, faça:
	1-Crie uma pasta em app/assets/stylesheets e coloque todos os arquivos .css lá.
	2-Vá em app/config/manifest.js o comando para referenciar os seus arquivos .css lá. Por exemplo, você criou uma pasta chamada home, então, neste arquivo manifest.js, você irá escrever: 
	//= link_directory ../stylesheets/home .css
	9)Você precisa modificar o arquivo database.yml com a sua senha e o seu usuário do PostgreSQL para que a sua aplicação conecte corretamente com o banco de dados. Neste arquivo database.yml em config/database.yml basta substituir os nomes seuusuarioposgresql e suasenhapostgresql pelos valores corretos.
	10)Este arquivo funciona perfeitamente com Heroku.
	
	Conforme eu for aprendendo coisas novas e eu julgar que elas sejam úteis, eu vou atualizar o arquivo.
