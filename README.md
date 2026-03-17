# Gestão de Rotinas

Aplicação oficial para gerenciar tarefas com **notificações pop-up** nos horários definidos. **Acesso liberado para colaboradores Mercado Livre.**

## Funcionalidades

- ✅ Cadastrar tarefas com nome, horário e descrição
- ✅ Repetição: uma vez, diariamente, dias úteis ou fins de semana
- ✅ Notificações do sistema (pop-up) nos horários programados
- ✅ Dados salvos localmente (persistem ao fechar)
- ✅ Interface responsiva (celular, tablet, desktop)
- ✅ Aplicação oficial – acesso liberado

## Como usar

### 1. Iniciar o servidor

**Opção A – Acesso local:**
- Execute `iniciar.bat` (duplo clique)

**Opção A2 – Acesso na rede (múltiplos usuários):**
- Execute `iniciar-rede.bat` para permitir acesso de outros dispositivos na rede

**Opção B – Terminal:**
```bash
cd rotinas
python -m http.server 8080
```

**Opção C – Node.js:**
```bash
npx serve -p 8080
```

### 2. Abrir no navegador

**Acesso local:** http://localhost:8080

**Instalar no Google Chrome (PWA):**
1. Acesse a página no Chrome
2. Clique no ícone de instalação na barra de endereço (⊕) ou em ⋮ → "Instalar Gestão de Rotinas"
3. Confirme "Instalar" – o app abrirá em janela própria, como aplicativo

**Acesso na rede (outros usuários):** Para permitir que outros dispositivos na mesma rede acessem, use o IP da máquina:
- Windows: `ipconfig` para ver o IPv4
- Acesse: **http://SEU_IP:8080** (ex: http://192.168.1.100:8080)

### 3. Ativar notificações

1. Clique em **"Ativar Notificações"**
2. Aceite a permissão quando o navegador solicitar

### 4. Adicionar tarefas

1. Digite o nome da tarefa
2. Defina o horário
3. Escolha a repetição (uma vez, diário, etc.)
4. Clique em **Adicionar Tarefa**

## Compartilhar link

- Use o campo **"Link para compartilhar"** no topo da página
- Clique em **"Copiar"** e envie o link por e-mail, Teams, WhatsApp etc.
- **Rede local:** Use `iniciar-rede.bat` e compartilhe o IP (ex: http://192.168.1.100:8080)
- **Internet:** Para link público, faça deploy no GitHub Pages (veja seção abaixo)

## Importante

- **Mantenha a aba aberta** para receber as notificações
- As notificações usam a API do navegador (pop-up do sistema)
- Os dados ficam salvos no seu computador (localStorage)

## Link público (GitHub Pages)

Para compartilhar com qualquer pessoa na internet, siga o guia completo em **[DEPLOY.md](DEPLOY.md)**.

**Importante:** O endereço `seu-usuario.github.io` é um **exemplo**. Substitua pelo seu usuário real do GitHub. O erro 404 ocorre quando o repositório ainda não existe ou o deploy não foi feito.

## Estrutura

```
rotinas/
├── index.html    # Página principal
├── styles.css    # Estilos
├── app.js        # Lógica e notificações
├── manifest.json # Configuração PWA (Chrome)
├── sw.js         # Service Worker
├── iniciar.bat   # Inicia servidor (Windows)
└── README.md     # Este arquivo
```
