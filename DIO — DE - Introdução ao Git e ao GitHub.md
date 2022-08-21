# Introdução ao Git e ao GitHub

- - -

> **Vantagens de usar GitHub:**
> 1. Controle de versão
> 2. Armazenamento em nuvem
> 3. Trabalho em equipe
> 4. Melhorar seu código
> 5. Reconhecimento

> **GUI:** Graphic User Interface
> **CLI:** Command Line Interface

> **Ccmandos via Terminal**

| Windows            | Unix                      | Comandos                              |
| ------------------ | ------------------------- | ------------------------------------- |
| cd                 | cd                        |                                       |
| dir                | ls                        | Listar arquivos e diretórios          |
| mkdir              | mkdir                     | Cria diretório                        |
| del / rmdir        | rm -rf [recursivo/Forece] | Remove diretório                      |
| cls                | clear                     | Limpar terminal                       |
| echo hello > h.txt | echo hello > h.txt        | Redireciona a mensagem para o "h.txt" | 


> **SHA1:** O git usa sha1 para verificar se houve ou não alteração em arquivos.
> `openssl sha1 [nome_do_arquivo]`: gera o sha1 de um arquivo.

> **Blobs**: (bolhas) Guarda o sha de um arquivo.
> `echo 'conteudo'| git hash-object --stdin`
> \> fc31e91b26cf85a55e072476de7f263c89260eb1
> 
> `echo -e 'conteudo'| openssl sha1`
> \> 65b0d0dda479cc03cce59528e28961e498155f5c

> **Trees:** (árvores) Armazena blobs. Guarda o nome do arquvio. Uma árvore pode apontar para outra árvore.
> Ex.: ![[tree.png]]

> **Commits:** Objeto que junta tudo. Aponta para uma árvore, para um parente — último commint realizado antes dele —, para um autor e para uma mensagem.
> Ex.: ![[commit.jpg]]

> **Chaves SSH:** Forma de estabelecer uma conexão segura e encriptada entre duas máquinas.
> Settings > SSH and GPG keys
> [Gerar uma nova chave SSH e adicioná-la ao ssh-agent](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

> **Tokens:** Usado no lugar da senha
> Settings > Developer Settings > Personal access tokens

## Primeiros comandos com git

> `git init`: Inicia o git e gera uma pasta `.git` no respositório atual.
> ![[git_01.png]]
> **Untracked:** Ainda nãoão listados pelo git. Use `git add` para dicionar o arquivo.
> **Unmodified:** O gito compara o sha1 dos arquivos para saber se ele foi modificado ou nãoão
> **Staged:** Arquivos preparados para fazer parte de um commit.
> 
> **Commit:** retorna todos os arquivos para Unmodified, porque todas as alterações já estão salvas dentro do commit.

> 
> ![[git_02.png]]

### Configurações iniciais:

> `git config --global user.email "robsonfvilela@gmail.com"`: configura seu e-mail
>
> `git config --global user.name robsonfvilela`: configura seu nickname
> `git config --global --unset user.email`: Reseta e-mail
> `git config --global --unset user.name`: Reseta seu nome

> `git config --list`: Lista as configurações do seu git

> `git add *`: 
> `git commit -m "commit inicial"`: 

> `git status`: 

> `git commit`: 

### Trabalhando com o Git

> `git remote add origin https://github.com/robsonfvilela/livro-receitas.git`: 
> O `origin` é apenas um apelido para o repositório. Pode ser qualquer outro nome

> `git remote -v`: Lista os repositórios remotos cadastrados

> `git push origin master`: Envia os arquivos do repositório local para o repositório remoto


### Resolvendo Conflitos

> error: filed to push some refs to '[endereço]'
> `git pull origin master`: O git puxa o conteúdo que está no servidor para sua máquina para resolver conflitos.








