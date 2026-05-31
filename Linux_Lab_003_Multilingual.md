# Lab. 3.5 – Caso do Arquivo Suspeito / Suspect File Case / Cas du Fichier Suspect

## 🇺🇸 English

### Step 1: Threat Location
**Task:** Use the search command to find the exact path of the `hack.sh` file.
- **Command:** `find ~/Cybersecurity -name hack.sh`
- **Explanation:** The `find` command will search for a file based on a determined criterion. In this case, I used the `-name` flag since I knew the filename, but it is also possible to search by size (`-size`) or type (`-type`), among other advanced search flags.

### Step 2: Quick Analysis
**Task:** Use the command that reads the beginning of the file to see only the first 3 lines.
- **Command:** `head -n 3 hack.sh`
- **Explanation:** The `head` command will search the file's header. By default, it searches the first 10 lines; however, by using the `-n` flag, it is possible to determine the desired number of lines.

### Step 3: Security Lock
**Task:** Use the `chmod` numeric mode to apply "read-only" permission for everyone.
- **Command:** `chmod 444 hack.sh`
- **Explanation:** The `chmod` (change mode) command is used to change the permissions that a user or a group of users, including the file creator, has over changes to this file. By using the octal syntax, I aim to save resources and optimize operation time. It would also be possible to perform the operation using the symbolic syntax `chmod a=r hack.sh`.

### Step 4: Quarantine
**Task:** Create the Quarantine folder and move the file there in a single command flow.
- **Command:** `mkdir -p ~/Cybersecurity/Projetos/Investigacao_002/Quarentena && mv hack.sh $_`
- **Explanation:** Using `mkdir` to create the requested folder followed by the `&&` operator to link the next action to the success of the first. Once the first command has worked correctly, it requests the relocation of the file to the new folder.

---

## 🇫🇷 Français

### Étape 1 : Localisation de la Menace
**Tâche :** Utilisez la commande de recherche pour trouver le chemin exact du fichier `hack.sh`.
- **Commande :** `find ~/Cybersecurity -name hack.sh`
- **Explication :** La commande `find` recherchera un fichier en fonction d'un critère déterminé. Dans ce cas, j'ai utilisé l'option `-name` car je connaissais le nom du fichier, mais il est également possible de rechercher par taille (`-size`) ou par type (`-type`), ainsi que d'autres options de recherche avancée.

### Étape 2 : Analyse Rapide
**Tâche :** Utilisez la commande qui lit le début du fichier pour voir seulement les 3 premières lignes.
- **Commande :** `head -n 3 hack.sh`
- **Explication :** La commande `head` recherchera l'en-tête du fichier. Par défaut, elle recherche les 10 premières lignes ; cependant, en utilisant l'option `-n`, il est possible de déterminer le nombre de lignes souhaité.

### Étape 3 : Verrouillage de Sécurité
**Tâche :** Utilisez le mode numérique de `chmod` pour appliquer la permission "lecture seule" pour tout le monde.
- **Commande :** `chmod 444 hack.sh`
- **Explication :** La commande `chmod` (change mode) est utilisée pour modifier les permissions qu'un utilisateur ou un groupe d'utilisateurs, y compris le créateur du fichier lui-même, possède sur les modifications de ce fichier. En utilisant la syntaxe octale, je vise à économiser des ressources et à optimiser le temps d'opération. Il serait possible d'effectuer l'opération via la syntaxe symbolique `chmod a=r hack.sh`.

### Étape 4 : Quarantaine
**Tâche :** Créez le dossier Quarantaine et déplacez o fichier là-bas en un seul flux de commandes.
- **Commande :** `mkdir -p ~/Cybersecurity/Projetos/Investigacao_002/Quarentena && mv hack.sh $_`
- **Explication :** Utilisation de `mkdir` pour créer le dossier demandé suivi de l'opérateur `&&` pour lier l'action suivante au succès de la première. Une fois que la première commande a fonctionné correctement, elle demande la relocalisation du fichier dans le nouveau dossier.

---

## 🇵🇹 Português

### Passo 1: Localização de Ameaça
**Sua tarefa:** Use o comando de busca para encontrar o caminho exato do arquivo `hack.sh`.
- **Comando:** `find ~/Cybersecurity -name hack.sh`
- **Explicação:** O comando `find` irá buscar um arquivo em função do critério determinado. No caso em tela, utilizei a flag `-name`, uma vez que tinha conhecimento do nome do arquivo, mas ainda é possível buscar por tamanho (`-size`) ou por tipo (`-type`), além de outras flags de pesquisa avançada.

### Passo 2: Análise Rápida
**Sua tarefa:** Use o comando que lê o início do arquivo para ver apenas as 3 primeiras linhas.
- **Comando:** `head -n 3 hack.sh`
- **Explicação:** O comando `head` irá pesquisar o cabeçalho do arquivo. Por padrão, ele irá buscar as 10 primeiras linhas, no entanto, ao utilizar a flag `-n` é possível determinar o número de linhas desejado.

### Passo 3: Bloqueio de Segurança
**Sua tarefa:** Use o modo numérico do `chmod` para aplicar a permissão de "apenas leitura" para todo mundo.
- **Comando:** `chmod 444 hack.sh`
- **Explicação:** O comando `chmod` (change mode) é utilizado para alterar as permissões que um usuário ou um grupo de usuários, entre eles o próprio criador do arquivo, tem sobre as alterações neste arquivo. Ao utilizar a sintaxe pelo modo octal, viso economizar recursos e otimizar o tempo de operação. Seria possível fazer a operação por meio da sintaxe simbólica `chmod a=r hack.sh`.

### Passo 4: Quarentena
**Sua tarefa:** Crie a pasta Quarentena e mova o arquivo para lá em um único fluxo de comandos.
- **Comando:** `mkdir -p ~/Cybersecurity/Projetos/Investigacao_002/Quarentena && mv hack.sh $_`
- **Explicação:** Utilização de `mkdir` para criar a pasta solicitada seguido do operador `&&` para vincular a ação seguinte ao sucesso da primeira. Uma vez que o primeiro comando tenha funcionado corretamente, solicita a realocação do arquivo na nova pasta.

---
