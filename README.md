# extensions-lp

Landing page estática para o portfólio de extensões de navegador (Chrome Web Store e Microsoft Edge Add-ons).

## Site ao vivo

**https://siegeapp.github.io/extensions-lp/**

## Sobre

Página única (`index.html`) que lista extensões com:

- Filtros por categoria (Todas, Produtividade, Ferramentas, Finanças, Mídia, Privacidade)
- Suporte a 13 idiomas (detecção automática do navegador + seletor manual)
- Botões **Chrome** e **Edge** em cada card, apontando para as lojas oficiais
- Layout responsivo em tema escuro, sem dependências externas (HTML, CSS e JavaScript inline)

## Extensões

| Extensão | Chrome | Edge |
|----------|--------|------|
| Clock, Alarm, Timer & Stopwatch | [Chrome](https://chromewebstore.google.com/detail/najjeheikebkcgojohngpeapdambdlnh) | [Edge](https://microsoftedge.microsoft.com/addons/detail/paopgockjlhjgojnnnimbijagkckinmi) |
| Image Downloader Assistant | [Chrome](https://chromewebstore.google.com/detail/mmehagcgobifajenenomcbbcdabnjooh) | [Edge](https://microsoftedge.microsoft.com/addons/detail/plnnnhnpjjlkbikhknnmkpllenkphnfe) |
| Undo Closed Tabs | [Chrome](https://chromewebstore.google.com/detail/pmiplgmplhmiaieiggpnoocpbdlcoino) | [Edge](https://microsoftedge.microsoft.com/addons/detail/oinofgjodhlkicjgclkdhmggmkcllbee) |
| Video Speed Controller | [Chrome](https://chromewebstore.google.com/detail/gmpgnedihbpapkkeafjehjnlgnghlmjd) | [Edge](https://microsoftedge.microsoft.com/addons/detail/gcoehecbgogpiakimhlljbdkmoocifik) |
| QR Code Generator & Reader | [Chrome](https://chromewebstore.google.com/detail/afjjlnbbgojjefpnkfopdiajidjeijmb) | [Edge](https://microsoftedge.microsoft.com/addons/detail/igafjkcnpablnaggafbjemdgilfkcclp) |
| One-Click Cleaner | [Chrome](https://chromewebstore.google.com/detail/ibdojpbaclajkbmjmcfneimfnjpebcpo) | [Edge](https://microsoftedge.microsoft.com/addons/detail/naomgcjepmbcjfkdgjgndcphlhdpganj) |
| Chroma Color Picker | [Chrome](https://chromewebstore.google.com/detail/ghcgolhjnajkjeogfjkaakdfohebocfa) | [Edge](https://microsoftedge.microsoft.com/addons/detail/pcmnjdkmhdocjlcepjlcdnhhmokjlcgk) |
| Real-Time Crypto Price Alert Tracker | [Chrome](https://chromewebstore.google.com/detail/fiebjoapbhobkgnfkeefpjfembalkngj) | [Edge](https://microsoftedge.microsoft.com/addons/detail/ndbjppbkegghgimepbjpeimpohpdhbin) |
| Calculator Plus | [Chrome](https://chromewebstore.google.com/detail/bajijfddodanimeolonbjdaehmphfkpp) | [Edge](https://microsoftedge.microsoft.com/addons/detail/lcjjlldaggopebgdehkpbdiehiigaoio) |
| Monitix | [Chrome](https://chromewebstore.google.com/detail/cjekmkpgodnejbnmpkbaaoaaggbknjjm) | [Edge](https://microsoftedge.microsoft.com/addons/detail/pcfkdmehcjlomlnefbjadilkjkpbpmhe) |
| Alarm, Timer & Stopwatch for Browser | [Chrome](https://chromewebstore.google.com/detail/dobehameiiojoddgpdjjgonghbjejfjk) | [Edge](https://microsoftedge.microsoft.com/addons/detail/bdhohgoehamdgapipfclhhpbbeligaib) |
| Full Page Capture | [Chrome](https://chromewebstore.google.com/detail/cmfoidiacmlllaifebpdflabafobibnk) | [Edge](https://microsoftedge.microsoft.com/addons/detail/clpamonfoilgnmpbfdhiggbadjmdpbkh) |
| Pomodoro Focus Timer | [Chrome](https://chromewebstore.google.com/detail/bkbiklcbhkpphflodkdoedlokkknnebh) | [Edge](https://microsoftedge.microsoft.com/addons/detail/cjpfgipkkicleedpigbfjofeonnpiiee) |

## Desenvolvimento local

Abra o arquivo diretamente no navegador ou sirva a pasta com um servidor HTTP simples:

```bash
python3 -m http.server 8765
```

Acesse `http://localhost:8765`.

## Publicar no GitHub Pages

1. No repositório [siegeapp/extensions-lp](https://github.com/siegeapp/extensions-lp), vá em **Settings → Pages**.
2. Em **Build and deployment**, escolha **Deploy from a branch**.
3. Branch: `main`, pasta: `/ (root)`.
4. Salve. O site ficará disponível em **https://siegeapp.github.io/extensions-lp/** (pode levar alguns minutos na primeira publicação).

Como o projeto é só `index.html` na raiz, não é necessário build nem GitHub Actions.

## Atualizar extensões

Edite o array `extensionData` em `index.html`. Cada item aceita:

| Campo | Descrição |
|-------|-----------|
| `id` | Identificador interno (ex.: `clock`, `img`) |
| `icon` | URL do ícone na Chrome Web Store |
| `edgeIcon` | URL do ícone no CDN da Edge Add-ons (opcional; usado só se quiser trocar o ícone do card no futuro) |
| `url` | Link da Chrome Web Store |
| `edgeUrl` | Link da Microsoft Edge Add-ons |
| `category` | `productivity`, `tools`, `finance`, `media` ou `privacy` |
| `names` | Títulos por idioma (`en`, `pt_BR`, …) |
| `descriptions` | Descrições por idioma |

Traduções da interface ficam em `uiTranslations`. Ordem dos cards em “Todas” pode ser ajustada em `preferredAllOrder`.

## Repositório

https://github.com/siegeapp/extensions-lp
