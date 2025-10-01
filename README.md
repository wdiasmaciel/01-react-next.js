# Fundamentos de React e Next.js

## Objetivo
Compreender os conceitos iniciais de **React** e **Next.js**, e construir a primeira página com estilização personalizada.

---

## React
React é uma biblioteca criada pelo **Facebook (Meta)** para desenvolver aplicações para a Web.

## Next.js
Next.js é um framework criado pela **Vercel** que estende o React com funcionalidades que facilitam a criação de aplicações modernas para a Web.

---

## Configuração do Ambiente

### Requisitos
- **Node.js**: [https://nodejs.org/](https://nodejs.org/)  
  No Linux e Codespace:
  ```bash
  sudo apt install -y nodejs
  node -v
  ```

- **NPM (Node Package Manager)**:
  ```bash
  npm install -g npm@latest
  npm -v
  ```

- **Editor recomendado**: Visual Studio Code (VS Code)

---

## Criar um Projeto com Next.js

### Passo a passo
1. Execute o comando:
   ```bash
   npx create-next-app@latest
   ```

2. Se aparecer a mensagem abaixo, digite `y`:
   ```
   Need to install the following packages:
   create-next-app@15.5.4
   Ok to proceed? (y)
   ```

3. Responda às perguntas conforme abaixo:
   ```
   What is your project named? meu-app
   Would you like to use TypeScript? Yes
   Which linter would you like to use? ESLint
   Would you like to use Tailwind CSS? Yes
   Would you like your code inside a `src/` directory? Yes
   Would you like to use App Router? (recommended) Yes
   Would you like to use Turbopack? (recommended) Yes
   Would you like to customize the import alias (`@/*` by default)? Yes
   What import alias would you like configured? @/*
   ```

4. Acesse o diretório do projeto:
   ```bash
   cd meu-app
   ```

5. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```

6. Abra o navegador e acesse:
   ```
   http://localhost:3000
   ```

---

## Estilizando a Página

### Arquivo `globals.css`
Substitua o conteúdo por:
```css
@import "tailwindcss";

div {
  color: blue;
}
```

### Arquivo `layout.tsx`
Substitua o conteúdo por:
```tsx
import "./globals.css"

export default function RootLayout({children}: {children: React.ReactNode}) {
  return (
    <html lang="pt-br">
      <body>{children}</body>
    </html>
  )
}
```

### Arquivo `page.tsx`
Substitua o conteúdo por:
```tsx
export default function Home() {
  return (
    <div>
      Olá, Mundo!
    </div>
  )
}
```

Atualize a aba do navegador para visualizar a alteração.

---

## Repositório no GitHub
[https://github.com/wdiasmaciel/01-react-next.js](https://github.com/wdiasmaciel/01-react-next.js)

---

## Exercício

1. Atualize a mensagem da página para:
   - Exibir um cumprimento com o seu nome.
   - Aplicar fundo vermelho na tela.

### Dica
Use:
```css
background-color: red;
```

Altere o texto para algo como:
```
  Olá, Ana!
```