# Exercicios1
Administrador@Note-Paulo MINGW64 /c/git (main)
$ echo 01 > arquivo.txt

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git status
Na filial principal
Seu branch está atualizado com 'origin/main'.

Arquivos não rastreados:
 (use "git add <file>..." para incluir no que será comprometido)
        arquivo.txt

nada adicionado ao commit, mas arquivos não rastreados presentes (use "git add" para rastrear)

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git add .
aviso: LF será substituído por CRLF em arquivo.txt.
O arquivo terá suas terminações de linha originais em seu diretório de trabalho

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git status
Na filial principal
Seu branch está atualizado com 'origin/main'.

Alterações a serem confirmadas:
 (use "git restore --staged <file>..." para desencenar)
 Novo arquivo: arquivo.txt

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git commit -m "git add exemplo - arquivo.txt"
[main 790ea9e] git add exemplo - arquivo.txt
 1 arquivo alterado, 1 inserção(+)
 modo de criação 100644 arquivo.txt

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git diff arquivo.txt
aviso: LF será substituído por CRLF em arquivo.txt.
O arquivo terá suas terminações de linha originais em seu diretório de trabalho
diff --git a/arquivo.txt b/arquivo.txt
Índice 8A0F05E.. 9e22bcb 100644
--- arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git adicionar arquivo.txt
aviso: LF será substituído por CRLF em arquivo.txt.
O arquivo terá suas terminações de linha originais em seu diretório de trabalho

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git status
Na filial principal
Seu branch está à frente de 'origin/main' por 1 commit.
 (use "git push" para publicar seus commits locais)

Alterações a serem confirmadas:
 (use "git restore --staged <file>..." para desencenar)
 Modificado: arquivo.txt

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git diff --arquivo.txt preparado
diff --git a/arquivo.txt b/arquivo.txt
Índice 8A0F05E.. 9e22bcb 100644
--- arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git diff arquivo.txt
aviso: LF será substituído por CRLF em arquivo.txt.
O arquivo terá suas terminações de linha originais em seu diretório de trabalho
diff --git a/arquivo.txt b/arquivo.txt
índice 9e22bcb.. 75016EA 100644
--- arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git restore --staged arquivo.txt

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git commit -m "Adds restored arquivo.txt file from staging"
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git log --oneline
790ea9e (HEAD -> main) git add example - arquivo.txt
377e2ab (origin/main, origin/HEAD) Initial commit

Administrador@Note-Paulo MINGW64 /c/git (main)
$ echo "*.txt" > .gitignore

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

no changes added to commit (use "git add" and/or "git commit -a")

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git add .gitignore
warning: LF will be replaced by CRLF in .gitignore.
The file will have its original line endings in your working directory

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git commit -m "Adds .gitignore to ignore .txt files"
[main cacbc25] Adds .gitignore to ignore .txt files
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore

Administrador@Note-Paulo MINGW64 /c/git (main)
$ echo "Step M new file" > novo.txt

Administrador@Note-Paulo MINGW64 /c/git (main)
$ git status
Na filial principal
Seu branch está à frente de 'origin/main' por 2 commits.
 (use "git push" para publicar seus commits locais)

Alterações não preparadas para confirmação:
 (use "git add <file>..." para atualizar o que será confirmado)
 (use "git restore <arquivo>..." para descartar alterações no diretório de trabalho)
 Modificado: arquivo.txt

nenhuma alteração adicionada ao commit (use "git add" e/ou "git commit -a")
