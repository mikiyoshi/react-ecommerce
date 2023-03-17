# React Ecommerce App

Completed React Ecommerce App Repo

# Setting

```
nvm install v16
```

[strapi](https://docs.strapi.io/dev-docs/installation/cli)

```
npx create-strapi-app@latest server
```

- y : yes
- Quickstart (recommended)

# Strapi

- http://localhost:1337/admin/
  - create fake account
    - memorize pass and id

## Content-Type Builder

- Create new collection type
  - Item
    - name: text
    - shortDescription: Rich text
    - longDescription: Rich text
    - price: Number / decimal
    - image: Media / single media
    - category: Enumeration / newArrivals bestSellers topRated
  - Save
- Media Library
  - Add new assets
    - [strapi-images](client-backup/src/assets/strapi-images)
- Content Manager
  - Create new entry
    - name
    - shortDescription
    - longDescription
    - price
    - image
    - category: topRated
  - save
  - publish
- Create new collection type
  - Order
    - products: JSON
    - userName: text Short text
    - stripeSessionId: text Short text
  - Save

All item updated at

- server

  - src
    - api
      - item
        - content-types
        - controllers
        - routes
        - services
      - order
        - content-types
        - controllers
        - routes
        - services

- Settings
  - Roles
    - Public
      - Item: find, findOne
      - Order: create
    - Save

# React

- New Terminal <!-- 別のターミナルを立ち上げる / Strapi のターミナルはキープ -->

```
nvm install v16
```

```
npx create-react-app client
```

```
cd client
```

```
npm i @mui/material @emotion/react @emotion/styled @mui/icons-material react-router-dom@6 react-redux @reduxjs/toolkit formik yup dotenv react-responsive-carousel
```

```
npm run start
```

# Tailwind Shades

- theme.js

```
#000000
```

- select highlight
  - command + K
  - command + G

下記が自動で作られる

```
black: {
  100: "#cccccc",
  200: "#999999",
  300: "#666666",
  400: "#333333",
  500: "#000000",
  600: "#000000",
  700: "#000000",
  800: "#000000",
  900: "#000000"
},
```

# Stripe

[Stripe](https://dashboard.stripe.com/test/dashboard)

- Stripe Login
- Developers / light corner sub menu
- API key

  - Publishable key / put at client/src/scenes/Checkout.jsx
    - stripePromise

- New Terminal

```
cd client
```

```
npm i @stripe/stripe-js
```

```
cd server
```

```
npm i stripe
```

- Stripe Login
- Developers / light corner sub menu
- API key

  - Secret key / put at server/.env
    - STRIPE_SECRET_KEY=
  - Update server/src/api/order/controllers/order.js
    [Stripe API / Create a Session](https://stripe.com/docs/api/checkout/sessions/create)
    <!-- ここを確認すること -->
    [Stripe Docs/ Prebuilt Checkout page](https://stripe.com/docs/checkout/quickstart)
    <!-- これはシンプルなチェックアウトで不十分 -->

<!-- "@emotion/react": "^11.10.4",
"@emotion/styled": "^11.10.4",
"@mui/icons-material": "^5.10.3",
"@mui/material": "^5.10.3",
"@reduxjs/toolkit": "^1.8.5",
"@stripe/react-stripe-js": "^1.10.0",
"@stripe/stripe-js": "^1.35.0",
"@testing-library/jest-dom": "^5.16.5",
"@testing-library/react": "^13.3.0",
"@testing-library/user-event": "^13.5.0",
"": "^16.0.2",
"": "^2.2.9",
"pure-react-carousel": "^1.29.0",
"react": "^18.2.0",
"react-dom": "^18.2.0",
"react-redux": "^8.0.2",
"": "^3.2.23",
"react-router-dom": "^6.3.0",
"react-scripts": "5.0.1",
"web-vitals": "^2.1.4",
"": "^0.32.11" -->

<!-- ############################################## -->

# Entention

- ES7+ React/Redux/React-Native  
  `dsznajder.es7-react-js-snippets`

  React のスニペット(ショートカット)を使えるようにする
  https://github.com/dsznajder/vscode-react-javascript-snippets/blob/HEAD/docs/Snippets.md

- Pesticide for Chrome
  レイアウトの確認ができる

- Turbo Console Log / VS Code
  Control ± Option ± L で選択してハイライトしたものを console.log('highlight:', highlight) とできる

# Test at localhost

```
nvm install v16
```

```
npm install
```

```
npm start
```

- http://localhost:5000
- http://10.0.0.86:5000

# Git commit fix

[Commit を取り消したい](https://www.sejuku.net/blog/70611)

```
git add .
```

```
git commit -m "wrong message"
```

```
git reset --soft HEAD^
```

```
git commit -m "fix message"
```

```
git push origin master
```

- push の後は修正できない
