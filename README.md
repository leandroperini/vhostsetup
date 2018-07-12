# vhostsetup
É um bash script, ele vai criar os ambientes com a url que desejar e disponibilizar a entrada para ser adicionada ao hosts.

# Para rodar: 

Descompacte o arquivo e coloque o script no seu servidor
Execute o seguinte comando bash vhost_setup

# Caso queiram rodar como um comando:

Coloque-o no diretório /usr/bin e marque-o como executável:

    sudo chmod +x /usr/bin/vhost_setup

# Para utilizar:

Abra uma conexão ssh através do putty ou semelhante.
Execute o comando vhost_setup.
Caso queira apenas criar um novo ambiente para desenvolver, escolha a opção 2.
Digite o nome do usuário utilizado no login.
Em seguida escolha a opção "N" para criar uma url de teste diferente da default.
Digite uma URL de teste e pressione enter.

Copie a linha e coloque no seu arquivo de hosts:

    %SystemRoot%\System32\drivers\etc\hosts

Caso precise modificar a pasta webroot saia do multi_setup e digite: 
    
    sudo nano /etc/apache2/sites-enabled/{url-escolhida}.conf
    
Altere o caminho em "<Directory" e em "DocumentRoot".
Digite Ctrl+O, enter, em seguida Ctrl+X (salvando e fechando o arquivo).
Digite service apache2 reload e a alteração deverá funcionar.
