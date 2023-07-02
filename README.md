# Install_Ruby_and_Rails_with_rbenv
Tutorial de como instalar Ruby on Rails de Forma simples e rápida no Ubuntu para iniciar na programação


#1 - Comece atualizando o Ubunto e após instalando as dependências necessárias:
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

sudo apt update && sudo apt install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev software-properties-common libffi-dev nodejs yarn git

#2 - INSTALANDO e configurando o RBENV, "tive problemas com o RVM":
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
exec $SHELL

git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
exec $SHELL

source ~/.bashrc

#3 - Instalando o Ruby via rbenv
rbenv install 2.6.1

#4 - Setando qual versão do Ruby deseja
rbenv global 2.6.1

#5 - Atualizando o terminal
source ~/.bashrc

########## RUBY OK! ##########

########## BORA PARA O RAILS ##########
gem install rails -v 5.2.0 (Para adicionar uma versão específica)

gem install rails (Para a versão mais recente)

gem search '^rails$' --all (Para ver todas as versões disponíveis)
