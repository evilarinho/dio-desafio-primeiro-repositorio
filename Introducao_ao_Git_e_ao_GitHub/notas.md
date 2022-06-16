>>> Introdução ao Git e ao GitHub
- [x] Entendedo o que git  e sua importância
- [x] Navegação via command line interface e instalação
>>> Comandos básicos para um bom desempenho no terminal
ls
cd 
cd / (ir para o dir raiz do volume principal do computador)
cd .. (retroceder um nível)
clear ou CTRL + L
TAB = autocompletar na digitação
mkdir = criar uma pasta
echo hello > hello.txt
rm -rf workspace/ (com parâmetros para r=recursivo e f=para não solicitar confirmações)
- [ ] Entendendo como o git funciona por baixo dos panos
 - SHA1
openssl sha1 hello.txt
SHA1(hello.txt)= f572d396fae9206628714fb2ce00f72e94f2258f

 - Objetos fundamentais
Blobs
        echo 'conteudo'  | git hash-object --stdin
        fc31e91b26cf85a55e072476de7f263c89260eb1
        echo -e 'blob 9\0conteudo' | openssl sha1
        (stdin)= fc31e91b26cf85a55e072476de7f263c89260eb1

Trees
        \o
        blob

Commits
        tree
        parente (aponta para último commit realizado antes dele)
        autor
        mensagem
        timestamp (carimbo de tempo - data e hora de quando foi criado)

 - Sistema distribuído
 - Segurança

Chave SSH e Token

Primeiros comandos com Git
- [x] Iniciando o Git e criando um commit
editor para markdown: Typora
arquivo markdown = strogonoff.md
git init
git add
git commit
git *  <<==>> git .

Ciclo de vida dos arquivos no Git
- [x] Passo a passo do ciclo de vida
git status
mkdir
mv

Introdução ao GitHub
- [x] Trabalhando com o GitHub
git config --list
git config --global --unset user.email
git config --global --unset user.nickname
git config --global user.email "ed.vilarinho"gmail.com"
git config --global user.nickname "edilson@Acer-E5-473"
git push -u origin master
git remote add origin git@github.com:evilarinho/livro-receitas.git
git push -u origin master
git push origin master
git remote -v

Resolvendo conflitos
- [x] Como os conflitos acontecem no GitHub e como resovê-los
Quando acontece edições na mesma linha do arquivo é que surgem a maioria dos conflitos de merge
git clone