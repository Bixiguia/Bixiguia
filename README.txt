Instala��o do projeto no MAC OS X

1) Acessar o site http://www.github.com
2) Cadastrar-se ou utilizar login j� existente
3) No Finder, abrir o aplicativo Terminal (Aplicativos -> Utilit�rios -> Terminal)
4) Caso j� tenha o Git configurado no computador, v� para o pr�ximo passo. Caso contr�rio:
	1. Acesse http://git-scm.com e fa�a o download da �ltima vers�o do Git
	2. No Terminal, verifique por chaves SSH j� existentes:
		cd ~/.ssh
	Caso j� possua chaves:
		mkdir key_backup
		cp id_rsa* key_backup
		rm id_rsa*
	Caso tenha feito o backup das chaves, ou n�o possua nenhuma chave:
		ssh-keygen -t rsa -C �seu email�
		Aperte enter quando perguntado em qual arquivo salvar a chave
		Coloque uma senha e a confirme-a
5) No site do GitHub, v� at� Account Settings, clique em �SSH Public Keys� e clique em �Add another public key�
6) No Terminal, abra o arquivo id_rsa.pub com um editor de texto (sugest�o: No Finder, aperte Shift + Command + G e digite a pasta ~/.ssh para achar o arquivo)
7) Copie a chave do documento, sem deletar espa�os ou novas linhas, e cole no site do GitHub no campo �Key�, clicando em �Add Key� para adicionar a chave
8) No Terminal, digite ssh -T git@github.com
9) Aperte enter. Provavelmente uma mensagem dir� que a autenticidade do host n�o p�de ser estabelecida. Responda yes.
10) V�, no site do GitHub, at� Account Settings -> Account Admin e copie o token dado a voc�
11) Finalmente, para configurar sua conex�o, no Terminal, digite
	1. git config --global user.name �SeuPrimeiroNome SeuUltimoNome�
	2. git config --global user.email �Seu Email�
	3. git config --global github.user nomeDeUsuario
	4. git config --global github.token seuToken
12) No diret�rio do seu usu�rio (cd ~), execute o comando git clone git@github.com:Bixiguia/bixiguia.git
13) Rode o script install_macosx_en.sh caso o idioma de seu OS X seja o Ingl�s ou rode o script install_macosx_ptbr.sh caso o idioma de seu OS X seja o Portugu�s. Os dois scripts est�o localizados na pasta bixiguia/scripts.