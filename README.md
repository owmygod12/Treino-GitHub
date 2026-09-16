# Comandos DevOps e Inicialização do Projeto

Guia de referência rápida para criação de ambiente virtual, instalação e execução do Django, além do passo a passo completo com os comandos Git para versionamento e publicação no GitHub.

---

## 1. Ambiente Virtual (Bash / Git Bash)

### Criar o ambiente virtual
```bash
python -m venv venv
```

### Ativar o ambiente virtual

- **No Bash / Git Bash:**
  ```bash
  source venv/Scripts/activate
  ```

- *(Opcional)* **No Windows PowerShell:**
  ```powershell
  .\venv\Scripts\Activate.ps1
  ```

- *(Opcional)* **No CMD (Prompt de Comando):**
  ```cmd
  venv\Scripts\activate.bat
  ```

---

## 2. Configurando o Django no Ambiente Virtual

### Instalar o Django
```bash
pip install django
```

### Listar pacotes instalados
```bash
pip freeze
```

### Salvar dependências no arquivo requirements.txt
```bash
pip freeze > requirements.txt
```

### Instalar dependências a partir do requirements.txt
```bash
pip install -r requirements.txt
```

---

## 3. Comandos Django

### Criar o projeto Django no diretório atual
```bash
django-admin startproject core .
```

### Rodar e verificar o servidor local
```bash
python manage.py runserver
```

---

## 4. Comandos Git para Subir no GitHub

### Configurar a branch padrão global para `main`
```bash
git config --global init.defaultbranch main
```

### Passo a passo completo para o primeiro envio:

1. **Inicializar o repositório local** *(se ainda não tiver iniciado)*:
   ```bash
   git init
   ```

2. **Verificar o status dos arquivos**:
   ```bash
   git status
   ```

3. **Adicionar os arquivos à área de stage**:
   ```bash
   git add .
   ```

4. **Criar o primeiro commit**:
   ```bash
   git commit -m "feat: configuracao inicial do projeto django"
   ```

5. **Garantir que a branch atual se chame `main`**:
   ```bash
   git branch -M main
   ```

6. **Vincular ao repositório remoto do GitHub**:
   ```bash
   git remote add origin https://github.com/<seu-usuario>/<seu-repositorio>.git
   ```

7. **Enviar os arquivos para o GitHub** (criando o upstream na branch `main`):
   ```bash
   git push -u origin main
   ```

---

### Comandos Git para atualizações futuras:

```bash
# Adicionar alterações
git add .

# Gravar commit
git commit -m "mensagem descritiva da alteracao"

# Enviar para o GitHub
git push
```
