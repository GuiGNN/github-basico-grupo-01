## Como criar um repositório no GitHub!

### Etapa 1: Acesse o GitHub e inicie a criação
Entre no site oficial do GitHub e faça login na sua conta. No canto superior direito da tela, clique no ícone de **`+`** e selecione a opção **`New repository`**.

![Repositório](imagens/Rep%201.png)

---

### Etapa 2: Defina o nome e a descrição do projeto
Preencha os campos básicos de identificação:
* **Repository name:** Digite o nome do seu projeto.
* **Description:** Escreva uma breve descrição opcional sobre o que o seu projeto faz.

![Repositório](imagens/Rep%202.png)

---

### Etapa 3: Escolha a visibilidade (Público ou Privado)
Selecione se o seu projeto será **Public** (visível para qualquer pessoa na internet) ou **Private** (visível apenas para você e colaboradores convidados).

![Repositório](imagens/Rep%203.png)

---

### Etapa 4: Configure os arquivos iniciais
Marque as caixas de seleção opcionais conforme a sua necessidade:
* **Add a README file:** Para criar um arquivo de apresentação.
* **Add .gitignore:** Para definir arquivos que devem ser ignorados.
* **Choose a license:** Para definir os termos de uso do código.

![Repositório](imagens/Rep%204.png)

---

### Etapa 5: Finalize o processo
Revise as configurações escolhidas na página e clique no botão verde **`Create repository`** localizado na parte inferior. Pronto, o seu repositório estará criado!
![Repositório](imagens/Rep%205.png)

## ! Dicas e Informações Importantes !

* **Planeje o nome com cuidado:** Escolha nomes claros e curtos para facilitar a identificação futura dos seus projetos.
* **Segurança em primeiro lugar:** Nunca publique senhas, tokens de acesso, chaves de API ou dados sensíveis, mesmo em repositórios privados. Utilize arquivos de configuração separados e proteja-os devidamente.
* **Personalize o README:** Aproveite o arquivo de apresentação gerado para documentar instruções de uso, tecnologias envolvidas e o propósito geral do seu trabalho.



# Principais Comandos Git

### 1. Git Config
Configura as opções globais ou locais do Git, como o seu nome de usuário e e-mail, que ficam associados aos seus commits.

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@exemplo.com"
```
Explicação: É um dos primeiros comandos que você executa ao instalar o Git. A flag --global aplica a configuração para todos os repositórios da sua máquina. Você também pode configurá-lo por projeto omitindo o --global dentro de uma pasta específica.


### 2. Git Clone
Cria uma cópia local de um repositório remoto existente (como do GitHub, GitLab ou Bitbucket).

```bash
git clone <url-do-repositorio>
```
Explicação: Baixa todo o histórico do projeto, configura a conexão remota automaticamente (chamada por padrão de origin) e cria uma cópia de trabalho na sua máquina pronta para uso.


### 3. Git Add
Adiciona arquivos modificados ou novos arquivos à área de preparação (staging area), preparando-os para serem salvos no próximo commit.

```bash
git add nome-do-arquivo.txt    # Adiciona um arquivo específico
git add .                     # Adiciona todas as alterações do diretório atual
```
Explicação: O Git não salva alterações automaticamente. Com o git add, você diz explicitamente quais arquivos quer incluir no próximo ponto de salvamento.


### 4. Git Commit
Salva permanentemente as alterações que estavam na área de preparação (staging area) no histórico do repositório local.

```bash
git commit -m "feat: adiciona tela de login"
```
Explicação: Cria um "ponto de verificação" (snapshot) do código naquele momento. Cada commit recebe um identificador único (hash) e precisa de uma mensagem descritiva (-m) explicando o que foi alterado.


### 5. Git Branch
Gerencia as ramificações (branches) do seu projeto, permitindo criar, listar ou excluir linhas de desenvolvimento independentes.

```bash
git branch                    # Lista todas as branches locais
git branch nova-funcionalidade # Cria uma nova branch
git branch -d nome-da-branch   # Deleta uma branch que já foi mesclada
```
Explicação: As branches permitem que você trabalhe em novas funcionalidades ou correções sem alterar o código principal (main ou master) até que tudo esteja testado e pronto.


### 6. Git Merge
Une o histórico de uma branch em outra.

```bash
git switch main               # Vai para a branch principal
git merge nova-funcionalidade # Traz o código da outra branch para a atual
```
Explicação: É o processo de juntar o trabalho feito em uma branch (por exemplo, uma nova funcionalidade) de volta na branch principal (main) ou em outra ramificação.


### 7. Git Pull
Baixa e integra as alterações mais recentes de um repositório remoto para o seu repositório local.

```bash
git pull origin main
```
Explicação: Na prática, o git pull executa dois comandos em sequência: ele busca as novidades da nuvem (git fetch) e logo em seguida as combina com o seu código atual (git merge). É essencial para atualizar seu projeto com o que outras pessoas enviaram.


### 8. Git Push
Envia os seus commits locais (já salvos na sua máquina) para o repositório remoto.

```bash
git push origin main
```
Explicação: É o comando que publica o seu trabalho na nuvem (no GitHub, por exemplo), permitindo que outras pessoas vejam suas alterações, façam revisões ou acessem o código atualizado.
