# portfolio-sabrina-resources

Repositório de **assets** (imagens e outros arquivos estáticos) para usar via **link cru** (raw URL) em qualquer projeto — sites, portfólio, README, e-mails, etc.

Basta colocar o arquivo dentro da pasta [`images/`](./images), dar commit/push, e usar o link cru direto no seu projeto. Sem build, sem CDN paga, sem upload manual em serviço externo.

---

## Como usar o link cru

Depois que um arquivo está no repositório (ex.: `images/logo.png`), você tem duas formas de gerar o link:

### 1. GitHub Raw (oficial)

```
https://raw.githubusercontent.com/marinellibr/portfolio-sabrina-resources/main/images/NOME-DO-ARQUIVO
```

Exemplo:

```html
<img src="https://raw.githubusercontent.com/marinellibr/portfolio-sabrina-resources/main/images/logo.png" alt="Logo" />
```

### 2. jsDelivr (CDN gratuita, recomendada para produção)

É mais rápida, tem cache global e não sofre limite de banda como o raw do GitHub:

```
https://cdn.jsdelivr.net/gh/marinellibr/portfolio-sabrina-resources@main/images/NOME-DO-ARQUIVO
```

Exemplo:

```html
<img src="https://cdn.jsdelivr.net/gh/marinellibr/portfolio-sabrina-resources@main/images/logo.png" alt="Logo" />
```

> 💡 Troque `main` pela branch ou tag que você estiver usando.

---

## Estrutura

```
.
├── images/        ← coloque aqui suas imagens
└── README.md
```

---

## Boas práticas

- **Nomes sem espaços nem acentos**: use `foto-perfil.png` em vez de `Foto Perfil.png`. Espaços viram `%20` na URL e acentos podem quebrar.
- **Tudo minúsculo** e separado por hífen (`-`).
- **Otimize as imagens** antes de subir (ferramentas como [Squoosh](https://squoosh.app)) para o link carregar rápido.
- O **GitHub Raw não deve ser usado como CDN de alto tráfego** — para sites com muitos acessos, prefira o link do **jsDelivr**.
