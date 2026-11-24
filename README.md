# Somus Movelaria — Site institucional
 
Site de uma página (one-page) da **Somus Movelaria**, marcenaria sob medida em Santo André – SP. Apresenta os serviços, o portfólio de projetos em slider, o processo de trabalho e um formulário de contato.
 
## Conteúdo do site
 
- **Início:** apresentação da marca e chamadas para orçamento e portfólio
- **Serviços:** cozinhas planejadas, dormitórios e closets, home office, áreas gourmet e externas, projetos comerciais
- **Portfólio:** slider horizontal com 20 fotos de projetos entregues (setas, deslizar no celular, arrastar com o mouse e teclado)
- **Processo:** como funciona o trabalho, do projeto à instalação
- **Contato:** WhatsApp, e-mail, Instagram, endereço e formulário que leva o pedido de orçamento ao WhatsApp
## Tecnologias
 
Arquivo único em **HTML, CSS e JavaScript puro**, sem frameworks, sem dependências e sem requisições a serviços externos. As imagens estão embutidas no próprio arquivo (base64), então ele funciona offline e pode ser aberto com um duplo clique.
 
## Estrutura do repositório
 
```
.
├── index.html   # o site completo (renomeie somus-movelaria-site.html para index.html)
└── README.md
```
 
## Como publicar no GitHub
 
1. Crie um repositório novo em [github.com/new](https://github.com/new) (por exemplo, `somus-movelaria`).
2. Renomeie o arquivo `somus-movelaria-site.html` para **`index.html`**.
3. Envie os arquivos `index.html` e `README.md` para o repositório (botão **Add file → Upload files**, ou via Git):
```bash
git init
git add index.html README.md
git commit -m "Primeira versão do site da Somus Movelaria"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/somus-movelaria.git
git push -u origin main
```
 
## Como colocar o site no ar (GitHub Pages)
 
1. No repositório, vá em **Settings → Pages**.
2. Em **Build and deployment → Source**, escolha **Deploy from a branch**.
3. Selecione a branch **main** e a pasta **/ (root)**, e clique em **Save**.
4. Aguarde alguns minutos. O site ficará disponível em:
```
https://SEU-USUARIO.github.io/somus-movelaria/
```
 
### Domínio próprio (opcional)
 
Em **Settings → Pages → Custom domain**, informe o domínio (por exemplo, `www.somusmovelaria.com.br`) e aponte o DNS conforme a [documentação do GitHub](https://docs.github.com/pt/pages/configuring-a-custom-domain-for-your-github-pages-site). Ative também **Enforce HTTPS**.
 
## Como editar
 
Abra o `index.html` em qualquer editor de texto (por exemplo, VS Code). Os pontos mais comuns de alteração:
 
| O que alterar | Onde procurar no arquivo |
| --- | --- |
| Telefone / WhatsApp | seção `Fale conosco`, link `wa.me/5511968584888` |
| E-mail, endereço, Instagram | seção `Fale conosco` |
| Textos dos serviços | seção `O que fazemos` (`class="card"`) |
| Fotos do portfólio | seção `Portfólio` (`<figure>` dentro de `id="track"`) |
| Cores | variáveis `--orange`, `--black` etc. no início do `<style>` |
 
Para trocar uma foto, converta a nova imagem para base64 (ou, se preferir, salve-a em uma pasta `img/` e use `src="img/foto.jpg"`). Se usar imagens em arquivos separados, o arquivo `index.html` fica bem mais leve.
 
## Formulário de contato
 
O formulário valida e limpa os campos no navegador e, ao enviar, **abre o WhatsApp da Somus (+55 11 96858-4888) com a mensagem já pronta** (nome, ambiente, telefone e mensagem). Nenhum dado passa por servidores de terceiros; o cliente confirma o envio no próprio WhatsApp. Para trocar o número de destino, altere a constante `WHATSAPP` no final do `index.html`.
 
## Pendências antes de divulgar
 
- **Política de privacidade (LGPD):** o site coleta nome e telefone, então vale publicar uma política de privacidade.
- **Foto da oficina/equipe:** a seção Sobre ainda mostra uma caixa de exemplo no lugar da foto.
## Segurança
 
- Nenhum script, fonte, foto ou rastreador de terceiros; as imagens ficam embutidas no próprio arquivo.
- **Política de segurança de conteúdo (CSP)** no `<head>`: bloqueia por padrão qualquer recurso externo, iframes, plugins e envio de formulários a outros sites.
- Proteção contra *clickjacking* por script (o site não abre dentro de iframe de outro domínio).
- Entradas do formulário limpas e validadas; a mensagem é codificada para URL antes de abrir o WhatsApp.
- Links externos usam `rel="noopener noreferrer"`.
- **Limitação do GitHub Pages:** ele não permite configurar cabeçalhos HTTP, então `X-Frame-Options` e `frame-ancestors` não podem ser usados. Se isso for importante, hospede em Cloudflare Pages, Netlify ou Vercel.
- O CSP mantém `script-src 'unsafe-inline'` porque o site é um arquivo único. Isso é aceitável aqui, pois a página não exibe conteúdo digitado por visitantes. Se um dia o JavaScript for movido para um arquivo `.js` separado, remova o `unsafe-inline`.
## Contato
 
- **WhatsApp:** [+55 11 96858-4888](https://wa.me/5511968584888)
- **E-mail:** somusmovelaria@outlook.com
- **Instagram:** [@somusmovelaria](https://www.instagram.com/somusmovelaria/)
- **Endereço:** Rua Barão de Loreto, 364 — Condomínio Maracanã, Santo André – SP
## Licença
 
© Somus Movelaria. Todos os direitos reservados. As fotos, o logotipo e os textos não podem ser copiados ou reutilizados sem autorização.
