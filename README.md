# Testes Codex Octo

Este repositório contém a página de exemplo `hello-codex.html`, publicada via GitHub Pages a partir da branch `main` na raiz do projeto.

## Como publicar no GitHub Pages

> ⚠️ Apenas abrir um Pull Request não executa o deploy. É necessário que o conteúdo esteja na branch publicada pelo GitHub Pages (geralmente `main`).

1. Faça merge do Pull Request com o diagrama BPMN na branch `main` (ou outra branch configurada para deploy).
2. Faça push do conteúdo desta pasta para o GitHub, garantindo que os arquivos `index.html` e `studio-x-bpmn.html` estejam na branch publicada.
3. No GitHub, acesse **Settings > Pages** do repositório.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Defina `main` como branch e `/ (root)` como pasta.
6. Salve as configurações; o GitHub Pages inicia a publicação e o status aparece em **Actions** e na tela de **Pages**.

### URL pública

Depois que o GitHub Pages terminar o deploy, a aplicação ficará disponível em:

```
https://<seu-usuario>.github.io/testes-codex-octo/
```

As páginas relevantes podem ser acessadas diretamente:

```
https://<seu-usuario>.github.io/testes-codex-octo/index.html
https://<seu-usuario>.github.io/testes-codex-octo/studio-x-bpmn.html
```

Substitua `<seu-usuario>` pelo nome de usuário ou organização proprietário do repositório no GitHub.

Caso você esteja trabalhando em um fork ou em uma organização, verifique também se o GitHub Pages está habilitado para o tipo de conta correspondente.

### E se eu quiser testar antes do merge?

- Você pode apontar o GitHub Pages temporariamente para a branch do Pull Request (ex.: `feature/studio-x-bpmn`). Basta repetir os passos acima escolhendo essa branch na etapa 5. O site ficará disponível enquanto a configuração estiver ativa.
- Alternativamente, faça o teste local seguindo as instruções da próxima seção.

## Como visualizar o diagrama BPMN localmente

Para abrir a página `studio-x-bpmn.html` sem esperar pelo deploy:

1. No terminal, navegue até a raiz do projeto (a pasta que contém este `README.md`). Por exemplo:

   ```bash
   cd /caminho/para/testes-codex-octo
   ```

   Em seguida, inicie o servidor local:

   ```bash
   python3 -m http.server 8000
   ```

2. Abra o navegador e acesse:

   ```
   http://localhost:8000/studio-x-bpmn.html
   ```

Você também pode abrir `index.html` pela mesma URL (`http://localhost:8000/`) e clicar no botão **Ver fluxo BPMN do Studio X** para acessar o diagrama.

> 💡 **404?** Se você iniciou o servidor em outra pasta (por exemplo, na raiz do sistema), adicione o caminho completo na URL: `http://localhost:8000/<caminho>/testes-codex-octo/studio-x-bpmn.html`. O mais simples, porém, é garantir que o `python3 -m http.server` seja executado dentro da pasta do projeto.
