# dew_repositorie
Repositório da disciplina de Desenvolvimento Web (dew)

# Atividade Prática - Realizando primeiro commit do repositório

# Configurando Git

Ao abrir o terminal GitBash execute os seguintes comandos:
```
git config --global user.name "Seu Nome"
git config --global user.email "seuemaildoGitHub@gmail.com"
```

# Criando repositório no GitHub

Crie uma conta e faça login no GitHub. Clique no seu perfil e acesse `Repositories`. Clique em `New`, nomeie o seu repositório, configure a `Choose visibility` como `public` para que tenha acesso público. Clique no botão `Create repository`.

# Configurando chave SSH

Abra o terminal GitBash e execute o seguinte comando para gerar um novo par de chaves SSH:
```
ssh-keygen -t ed25519 -C "seu-email@exemplo.com"
```
 Pressione `Enter` para aceitar o local padrão de salvamento do arquivo. Digite uma senha (passphrase) caso queira segurança extra, ou então aperte `Enter` para deixar vazio.

Para iniciar o agente SSH e adicionar a chave, ainda no GitBash execute os seguintes comandos:
```
eval "$(ssh-agent -s)"
```

Adicione sua chave privada ao agente:
```
eval "$(ssh-agent -s)"
```

Para exibir e copiar sua chave pública, execute o seguinte comando:
```
cat ~/.ssh/id_ed25519.pub
```

### Por fim, acesse sua conta no GitHub, cique na sua foto de perfil (canto superior direito) e vá em `Settings` (Configurações). Na barra lateral esquerda, clique em `SSH and GPG keys`. Clique em `New SSH Key` (Nova Chave SSH), adicione um título identificável para o seu computador. Cole o conteúdo da chave pública no campo `Key` e clique em `Add SSH key`. Feito isso, teste a conexão no terminal do GitBash com o seguinte comando: 
```
ssh -T git@github.com
```
Se for solicitado a confirmação da conexão, digite `yes`, você receberá uma mensagem de boas vindas com o seu usuário.

# Passo a Passo para clonar repositório
 - **Copiar link do repositório (via SSH ou HTTPS)**
 - **Abrir GitBash e executar os seguintes comandos:**
 ```
 cd pasta_criada
 git clone link do repositorio
 cd nome_do_repositorio
 code .
 ```

