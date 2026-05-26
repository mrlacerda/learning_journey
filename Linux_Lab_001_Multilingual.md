# Linux Fundamentals Lab 001 - Digital Investigation
This repository contains a basic Linux command laboratory focused on Cybersecurity and Digital Investigation structures.

---

## 🇺🇸 English Version

### Lab 001 – Basic Linux Commands
**Step 01**

**Objectives** (To be executed via Terminal only)

#### 1. Root Structure
**Task:** Create a folder structure in a single command called `CyberSecurity/Projetos/Investigacao_001`.
- **Suggested Command:** `mkdir -p CyberSecurity/Projetos/Investigacao_001`
- **Explanation:** The `mkdir` command creates new directories. By using the `-p` flag, it creates a directory from a path that does not yet exist, thus creating both parent and child folders.

#### 2. Work Subfolders
**Task:** Inside `Investigacao_001`, create three folders: `Evidencias`, `Logs`, and `Relatorios`.
- **Suggested Command:** `mkdir -p Cybersecurity/Projetos/Investigacao_001/{Evidencias,Logs,Relatorios}`
- **Explanation:** Using curly braces `{}` within the destination folder tells the system we want to create multiple new folders at that location, saving time and effort.

#### 3. Data Collection
**Task:** Without entering the `Logs` folder, create a file named `acessos.log` inside it, containing the following line: `2026-05-24 10:00:00 - IP 192.168.1.100 - LOGIN_SUCCESS`.
- **Suggested Command:** `echo "2026-05-24 10:00:00 - IP 192.168.1.100 - LOGIN_SUCCESS" >> Logs/acessos.log`
- **Explanation:** The `echo` command can be used to insert data into an existing file, create a new file, or overwrite an existing one. We use the `>>` operator to append content, whereas the `>` operator is used to create or overwrite a file.

#### 4. Data Update
**Task:** Add a second line to the same `acessos.log` file without deleting the first one: `2026-05-24 10:05:00 - IP 10.0.0.5 - LOGIN_FAILED`.
- **Suggested Command:** `echo "2026-05-24 10:05:00 - IP 10.0.0.5 - LOGIN_DENIED" >> acessos.log`
- **Explanation:** As previously explained, the `echo` command followed by the `>>` operator is used to add text to an existing file.

#### 5. Direct Navigation
**Task:** Go directly to the `Relatorios` folder in a single command from your current location.
- **Suggested Command:** `cd ~/Cybersecurity/Projetos/Investigacao_001/Relatorios/`
- **Explanation:** Using the `cd` (change directory) command with the full path allows you to switch folders quickly.

#### 6. Progress Logging
**Task:** Inside `Relatorios`, create an empty file named `status_inicial.txt`.
- **Suggested Command:** `touch status_inicial.txt`
- **Explanation:** The `touch` command is used to create empty files.

#### 7. Verification
**Task:** Check the full path of your current location and then move up two levels in the directory tree.
- **Suggested Command:** `pwd` (to show current location) and `cd ../..` (to go up two levels).
- **Explanation:** `pwd` confirms the navigation was successful, and `..` represents the parent directory. Using `../../` is a shortcut to move up multiple levels without typing `cd` multiple times.

---

## 🇫🇷 Version Française

### Lab 001 – Premières Commandes Linux
**Étape 01**

**Objectifs** (À exécuter uniquement via le Terminal)

#### 1. Structure Racine
**Tâche :** Créez une structure de dossiers en une seule fois nommée `CyberSecurity/Projetos/Investigacao_001`.
- **Commande suggérée :** `mkdir -p CyberSecurity/Projetos/Investigacao_001`
- **Explication :** La commande `mkdir` crée de nouveaux répertoires. En utilisant l'option `-p`, elle crée un répertoire à partir d'un chemin qui n'existe pas encore, créant ainsi les dossiers parents et enfants.

#### 2. Sous-dossiers de Travail
**Tâche :** Dans `Investigacao_001`, créez trois dossiers : `Evidencias`, `Logs` et `Relatorios`.
- **Commande suggérée :** `mkdir -p Cybersecurity/Projetos/Investigacao_001/{Evidencias,Logs,Relatorios}`
- **Explication :** L'utilisation des accolades `{}` dans le dossier de destination indique au système que nous voulons créer plusieurs nouveaux dossiers à cet endroit, ce qui permet d'économiser du temps et des efforts.

#### 3. Collecte de Données
**Tâche :** Sans entrer dans le dossier `Logs`, créez un fichier nommé `acessos.log` à l'intérieur, contenant la ligne suivante : `2026-05-24 10:00:00 - IP 192.168.1.100 - LOGIN_SUCCESS`.
- **Commande suggérée :** `echo "2026-05-24 10:00:00 - IP 192.168.1.100 - LOGIN_SUCCESS" >> Logs/acessos.log`
- **Explication :** La commande `echo` peut être utilisée pour insérer des données dans un fichier existant, créer un nouveau fichier ou écraser un fichier existant. Nous utilisons l'opérateur `>>` pour ajouter du contenu, tandis que l'opérateur `>` est utilisé pour créer ou écraser un fichier.

#### 4. Mise à jour des Données
**Tâche :** Ajoutez une deuxième ligne au même fichier `acessos.log`, sans effacer la première : `2026-05-24 10:05:00 - IP 10.0.0.5 - LOGIN_FAILED`.
- **Commande suggérée :** `echo "2026-05-24 10:05:00 - IP 10.0.0.5 - LOGIN_DENIED" >> acessos.log`
- **Explication :** Comme expliqué précédemment, la commande `echo` suivie de l'opérateur `>>` est utilisée pour ajouter du texte à un fichier existant.

#### 5. Navigation Directe
**Tâche :** Allez directement au dossier `Relatorios` en une seule commande, à partir de votre dossier actuel.
- **Commande suggérée :** `cd ~/Cybersecurity/Projetos/Investigacao_001/Relatorios/`
- **Explication :** L'utilisation de la commande `cd` (change directory) avec le chemin complet permet de changer de dossier avec agilité.

#### 6. Enregistrement de la Progression
**Tâche :** Dans `Relatorios`, créez un fichier vide nommé `status_inicial.txt`.
- **Commande suggérée :** `touch status_inicial.txt`
- **Explication :** La commande `touch` est utilisée pour créer des fichiers vides.

#### 7. Vérification
**Tâche :** Vérifiez le chemin complet de l'endroit où vous vous trouvez actuellement, puis remontez de deux niveaux dans l'arborescence des répertoires.
- **Commande suggérée :** `pwd` (pour afficher l'emplacement actuel) et `cd ../..` (pour remonter de deux niveaux).
- **Explication :** `pwd` confirme que la navigation a réussi, et `..` représente le répertoire parent. L'utilisation de `../../` est un raccourci pour monter de plusieurs niveaux sans avoir à taper `cd` plusieurs fois.

---

## 🇧🇷 Versão em Português

### Lab. 001 – Primeiros Comandos Linux
**Step 01**

**Objetivos** (Executar apenas via Terminal)

#### 1. Estrutura Raiz
**Tarefa:** Crie uma estrutura de pastas de uma única vez chamada `CyberSecurity/Projetos/Investigacao_001`.
- **Comando sugerido:** `mkdir -p CyberSecurity/Projetos/Investigacao_001`
- **Explicação:** O comando `mkdir` cria novos diretórios. Ao utilizarmos com a flag `-p`, ele criará um diretório a partir de um caminho que ainda não existe, criando assim, pastas e subpastas.

#### 2. Subpastas de Trabalho
**Tarefa:** Dentro de `Investigacao_001`, crie três pastas: `Evidencias`, `Logs` e `Relatorios`.
- **Comando sugerido:** `mkdir -p Cybersecurity/Projetos/Investigacao_001/{Evidencias,Logs,Relatorios}`
- **Explicação:** Ao utilizarmos as chaves dentro da pasta destino do diretório, informamos ao sistema que queremos criar diversas novas pastas naquele local, poupando tempo e esforço.

#### 3. Coleta de Dados
**Tarefa:** Sem entrar na pasta `Logs`, crie um arquivo chamado `acessos.log` dentro dela, contendo a seguinte linha: `2026-05-24 10:00:00 - IP 192.168.1.100 - LOGIN_SUCCESS`.
- **Comando sugerido:** `echo "2026-05-24 10:00:00 - IP 192.168.1.100 - LOGIN_SUCCESS" >> Logs/acessos.log`
- **Explicação:** O comando `echo` pode ser utilizado para inserir dados em um arquivo que já exista, criar um arquivo que não exista ou ainda sobrescrever um arquivo que já tenha algum conteúdo. Usamos `>>` para adicionar e `>` para sobrescrever.

#### 4. Atualização de Dados
**Tarefa:** Adicione uma segunda linha ao mesmo arquivo `acessos.log`, sem apagar a primeira: `2026-05-24 10:05:00 - IP 10.0.0.5 - LOGIN_FAILED`.
- **Comando sugerido:** `echo "2026-05-24 10:05:00 - IP 10.0.0.5 - LOGIN_DENIED" >> acessos.log`
- **Explicação:** Como explicado anteriormente, o comando ‘echo’ seguido do operador ‘>>’ é utilizado para adicionar texto a um arquivo já existente.

#### 5. Navegação Direta
**Tarefa:** Vá direto para a pasta `Relatorios` em um único comando, partindo da sua pasta atual.
- **Comando sugerido:** `cd ~/Cybersecurity/Projetos/Investigacao_001/Relatorios/`
- **Explicação:** Ao utilizar o comando ‘cd’ (change directory) e descrever o caminho completo, é possível trocar de pastas com agilidade.

#### 6. Registro de Progresso
**Tarefa:** Dentro de `Relatorios`, crie um arquivo vazio chamado `status_inicial.txt`.
- **Comando sugerido:** `touch status_inicial.txt`
- **Explicação:** O comando ‘touch’ é utilizado para criar arquivos em branco.

#### 7. Verificação
**Tarefa:** Verifique o caminho completo de onde você está agora e depois volte dois níveis na árvore de diretórios.
- **Comando sugerido:** `pwd` (print work directory) para mostrar o local que estou e `cd ../..` para voltar dois níveis na árvore de diretórios.
- **Explicação:** O `pwd` confirma se a navegação foi bem-sucedida, e o `..` representa o diretório pai. Usar `../../` é um atalho para subir múltiplos níveis sem precisar digitar o comando `cd` várias vezes.
