# Lab. 002 – Auditoria e Investigação Digital

Este repositório documenta o progresso em comandos avançados de Terminal Linux voltados para Cybersecurity e Auditoria.

---

### Tarefas

#### 1. Estrutura de Auditoria
**Objetivo:** Crie a seguinte estrutura de diretórios de uma única vez: `Auditoria_Seguranca/Logs/Servidor_01`.

* **Comando sugerido:**
    ```bash
    mkdir -p Cybersecurity/Projetos/Investigacao_002/Auditoria_Seguranca/Logs/Servidor_01
    ```
* **Explicação:** O comando `mkdir` seguido da flag `-p` indica que o sistema deve criar um diretório no caminho informado, ainda que as pastas não existam. No caso de pastas inexistentes, o sistema irá criá-las até que chegue à última pasta do caminho informado.

#### 2. Criação de Arquivos
**Objetivo:** Dentro da pasta `Servidor_01`, crie três arquivos vazios: `auth.log`, `system.log` e `web.log`.

* **Comando sugerido:**
    ```bash
    cd Cybersecurity/Projetos/Investigacao_002/Auditoria_Seguranca/Logs/Servidor_01/ && touch auth.log system.log web.log
    ```
* **Explicação:** Nesta etapa, utilizei uma saída alternativa, um pouco mais trabalhosa, mas não lembrava em parte e não tinha conhecimento de outra forma de fazer.
* **Sugestão:** Uma alternativa mais rápida e eficiente para resolver este problema seria a utilização do comando: `touch Cybersecurity/Projetos/Investigacao_002/Auditoria_Seguranca/Logs/Servidor_01/{auth.log,system.log,web.log}`, criando todos os arquivos com um único comando e reduzindo os riscos de erro. Além disso, seria possível, na parte final do comando, substituir `{auth.log,system.log,web.log}` por `{auth,system,web}.log`. Desta forma, o sistema entenderia que todos os arquivos inseridos nas chaves teriam terminações ‘.log’ e geraria otimização dos recursos.

#### 3. Injeção de Dados (auth.log)
**Objetivo:** Adicione as seguintes linhas ao arquivo `auth.log` (sem abrir editores de texto):
- 18:00 - User: admin - Status: SUCCESS
- 18:05 - User: guest - Status: FAILED
- 18:10 - User: root - Status: FAILED
- 18:15 - User: admin - Status: SUCCESS
- 18:20 - User: unknown - Status: FAILED

* **Comando sugerido:**
    ```bash
    echo -e "18:00 - User: admin - Status: SUCCESS\n18:05 - User: guest - Status: FAILED\n18:10 - User: root - Status: FAILED\n18:15 - User: admin - Status: SUCCESS\n18:20 - User: unknow - Status: FAILED" > auth.log
    ```
* **Explicação:** A solução sugerida traz a utilização do comando ‘echo’ adicionado à flag ‘-e’ (enable scapes). Desta forma, ao utilizarmos a instrução `\n`, indicamos ao sistema que haverá uma quebra de linha no texto. A solução ‘echo -e’ é utilizada em função do contexto de aprendizado inicial. No entanto, ao buscar uma solução ativa para esta etapa do exercício, ocorreu o primeiro contato com o comando ‘printf’, que seria uma alternativa para resolver o mesmo problema. Além disso, utilizei o operador `>` para garantir que o arquivo, que até então não continha nenhum dado, recebesse as linhas propostas como conteúdo inicial.

#### 4. Injeção de Dados (web.log)
**Objetivo:** Adicione esta linha ao arquivo `web.log`:
`18:25 - GET /login - IP: 192.168.1.50 - 404 Not Found`

* **Comando sugerido:**
    ```bash
    echo "18:25 - GET /login – IP: 192.168.1.50 - 404 Not Found" >> web.log
    ```
* **Explicação:** O comando `echo` é utilizado para incluir o texto solicitado dentro do arquivo determinado. Por tratar-se de um arquivo em branco, seria possível utilizar tanto o operador ‘>’ quanto o operador ‘>>’ (append). Caso houvesse algum outro dado que se desejasse preservar, o mais adequado seria utilizar o ‘>>’, uma vez que é considerado uma boa prática de segurança por evitar a perda acidental de eventos anteriores.

#### 5. Investigação de Alvos
**Objetivo:** Execute uma busca que retorne apenas as linhas que contenham o usuário `root` no arquivo `auth.log`.

* **Comando sugerido:**
    ```bash
    grep 'root' auth.log
    ```
* **Explicação:** Para solucionar esta etapa do processo, utilizamos o comando “grep” para buscar uma expressão dentro do arquivo. O arquivo buscará o termo desejado e retornará a linha completa onde o termo está presente.

#### 6. Filtro de Ruído
**Objetivo:** Execute um comando que mostre tudo o que aconteceu no `auth.log`, exceto as linhas que tiveram `SUCCESS`.

* **Comando sugerido:**
    ```bash
    grep -v 'SUCCESS' auth.log
    ```
* **Saída Esperada:**
    ```text
    18:05 - User: guest - Status: FAILED
    18:10 - User: root - Status: FAILED
    18:20 - User: unknown - Status: FAILED
    ```
* **Explicação:** O comando `grep`, quando utilizado em conjunto com a flag ‘-v’ (invert) fará uma busca reversa no arquivo desejado. Ao pedir que ele procure por “SUCCESS”, eu estou, basicamente, pedindo que ele ignore este termo em sua pesquisa.

#### 7. Contagem de Danos
**Objetivo:** Utilize uma flag do `grep` para contar quantas vezes a palavra `FAILED` aparece no arquivo `auth.log`.

* **Comando sugerido:**
    ```bash
    grep -c 'FAILED' auth.log
    ```
* **Saída Esperada:** `3`
* **Explicação:** O comando `grep`, ao ser utilizado em conjunto com a flag ‘-c’ (count) tem a função de contar o número de ocorrências do termo desejado.