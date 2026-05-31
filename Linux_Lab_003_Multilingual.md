# Lab. 3.5 – Caso do Arquivo Suspeito / Suspect File Case / Cas du Fichier Suspect

## 🇺🇸 English: Investigation and Quarantine

### Investigation Tasks

1. **Threat Location**
   - **Objective:** Locate `hack.sh` within `~/Cybersecurity`.
   - **Command:** `find ~/Cybersecurity -name hack.sh`
   - **Explanation:** `find` searches based on criteria. We use `-name` for the exact filename.

2. **Quick Analysis**
   - **Objective:** View the first 3 lines without executing.
   - **Command:** `head -n 3 hack.sh`
   - **Explanation:** `head` displays the file header. `-n 3` limits the output.

3. **Security Lock**
   - **Objective:** Make the file "read-only" (Integrity).
   - **Command:** `chmod 444 hack.sh` (or `chmod a=r hack.sh`)
   - **Explanation:** `444` sets read permission for owner, group, and others, preventing accidental edits.

4. **Quarantine**
   - **Objective:** Move to isolation in a single flow.
   - **Command:** `mkdir -p ~/Cybersecurity/Projetos/Investigacao_002/Quarentena && mv hack.sh $_`
   - **Explanation:** `mkdir -p` creates the path; `&&` links the commands; `$_` reuses the last argument.

---

## 🇫🇷 Français : Enquête et Quarantaine

### Tâches d'Enquête

1. **Localização de la Menace**
   - **Objectif :** Localiser `hack.sh` dans `~/Cybersecurity`.
   - **Commande :** `find ~/Cybersecurity -name hack.sh`
   - **Explication :** `find` recherche selon des critères. On utilise `-name` pour le nom exact.

2. **Analyse Rapide**
   - **Objectif :** Voir les 3 premières lignes sans exécuter.
   - **Commande :** `head -n 3 hack.sh`
   - **Explication :** `head` affiche l'en-tête. `-n 3` limite la sortie.

3. **Verrouillage de Sécurité**
   - **Objectif :** Mettre en "lecture seule" (Intégrité).
   - **Commande :** `chmod 444 hack.sh` (ou `chmod a=r hack.sh`)
   - **Explication :** La valeur `444` définit la lecture pour tous, empêchant toute modification.

4. **Quarantaine**
   - **Objectif :** Déplacer vers l'isolation en un seul flux.
   - **Commande :** `mkdir -p ~/Cybersecurity/Projetos/Investigacao_002/Quarentena && mv hack.sh $_`
   - **Explication :** `mkdir -p` crée le dossier ; `&&` assure la suite ; `$_` reprend le chemin.

---

### Verificação / Verification / Vérification
`ls -l ~/Cybersecurity/Projetos/Investigacao_002/Quarentena/hack.sh`

---

## 🇵🇹 Português: Investigação e Quarentena

### Tarefas de Investigação

1. **Localização de Ameaça**
   - **Objetivo:** Localizar `hack.sh` em `~/Cybersecurity`.
   - **Comando:** `find ~/Cybersecurity -name hack.sh`
   - **Explicação:** O `find` busca arquivos por critérios. Usamos `-name` para o nome exato.

2. **Análise Rápida**
   - **Objetivo:** Ver as 3 primeiras linhas sem executar o código.
   - **Comando:** `head -n 3 hack.sh`
   - **Explicação:** `head` exibe o início do arquivo. `-n 3` limita a saída.
   

3. **Bloqueio de Segurança**
   - **Objetivo:** Tornar o arquivo "somente leitura" (Integridade).
   - **Comando:** `chmod 444 hack.sh` (ou `chmod a=r hack.sh`)
   - **Explicação:** O valor `444` define leitura para dono, grupo e outros, impedindo alterações.
   

4. **Quarentena**
   - **Objetivo:** Mover para isolamento em um fluxo único.
   - **Comando:** `mkdir -p ~/Cybersecurity/Projetos/Investigacao_002/Quarentena && mv hack.sh $_`
   - **Explicação:** `mkdir -p` cria a pasta; `&&` executa o próximo se houver sucesso; `$_` repete o caminho criado.

---
