# Foi criado um arquivo README.md com comando git >> README.md

PS C:\Users\felip\Impacta\exercicio01> git >> README.md
PS C:\Users\felip\Impacta\exercicio01> git add README.md
PS C:\Users\felip\Impacta\exercicio01> git add README.md
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

# Depois foi realizado comando git status para verificação de stag

PS C:\Users\felip\Impacta\exercicio01> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

# Foi criado um arquivo.txt com comando echo 01 > arquivo.txt
PS C:\Users\felip\Impacta\exercicio01> echo 01 > arquivo.txt

# Adicionado o arquivo no staged com git add

PS C:\Users\felip\Impacta\exercicio01> git add 01 - arquivo.txt     
PS C:\Users\felip\Impacta\exercicio01> git add arquivo.txt     
PS C:\Users\felip\Impacta\exercicio01> echo 02 > arquivo.txt
PS C:\Users\felip\Impacta\exercicio01> git stats 
git: 'stats' is not a git command. See 'git --help'.

The most similar command is
        status
PS C:\Users\felip\Impacta\exercicio01> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   arquivo.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

PS C:\Users\felip\Impacta\exercicio01> git diff arquivo.txt
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

PS C:\Users\felip\Impacta\exercicio01> git add arquivo.txt
PS C:\Users\felip\Impacta\exercicio01> git diff arquivo.txt
PS C:\Users\felip\Impacta\exercicio01> echo 03 > arquivo.txt

# Nessa fase, foi feito o comando diff para mostrar a modificação no arquivo.txt

PS C:\Users\felip\Impacta\exercicio01> git diff arquivo.txt 
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03

PS C:\Users\felip\Impacta\exercicio01> git add arquivo.txt
PS C:\Users\felip\Impacta\exercicio01> git diff arquivo.txt
PS C:\Users\felip\Impacta\exercicio01> echo 03 > arquivo.txt
PS C:\Users\felip\Impacta\exercicio01> git diff arquivo.txt
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03

PS C:\Users\felip\Impacta\exercicio01> git restore arquivo.txt
PS C:\Users\felip\Impacta\exercicio01> git commit -m "file: arquivo.txt"
[main (root-commit) 493aded] file: arquivo.txt
 2 files changed, 45 insertions(+)
 create mode 100644 README.md
 create mode 100644 arquivo.txt
PS C:\Users\felip\Impacta\exercicio01> git log
commit 493adedecfe93db364da9c19dce35d7bc9cd720e (HEAD -> main)
Author: Fededaher <felipequeiroz05@gmail.com>
Date:   Thu Aug 8 21:02:50 2024 -0300

    file: arquivo.txt
PS C:\Users\felip\Impacta\exercicio01> git add .gitignore 
fatal: pathspec '.gitignore' did not match any files
PS C:\Users\felip\Impacta\exercicio01> git >> .gitignore 
PS C:\Users\felip\Impacta\exercicio01> echo 01 > novo.txt
PS C:\Users\felip\Impacta\exercicio01> git status       
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

