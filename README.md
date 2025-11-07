## Ecommerce cart application 


https://github.com/user-attachments/assets/c67838cb-6ed7-42dc-aa2e-462f0833182b


This simple shopping cart prototype shows how React with Typescript, React hooks, react Context and Styled Components can be used to build a friendly user experience with instant visual updates and scaleable code in ecommerce applications.

#### Features

- Add and remove products from the floating cart using Context Api
- Filter products by available sizes using Context Api
- Responsive design


## Build/Run

#### Requirements

- Node.js
- NPM










A modern, responsive e‑commerce cart built with React 18, TypeScript, Context API, and styled-components. The app features size-based filtering, dynamic product cards, and a floating cart with real-time totals. Production builds are deployable to Firebase Hosting.


## Highlights
- **Context-driven state**: Separate products and cart providers (`ProductsProvider`, `CartProvider`) with focused hooks (`useProducts`, `useCart`).
- **Responsive UI**: Styled-components theme with breakpoints and accessible focus states.
- **Filtering**: Size filters using reusable `Checkbox` and products context.
- **Cart UX**: Add/remove items, adjust quantities, subtotal and installments, floating toggle.
- **Data layer**: Local JSON during dev; Axios + Firebase endpoint in production.
- **Quality gates**: 90%+ coverage thresholds, RTL tests, prettier, ESLint, and commit linting.

## Tech Stack
- React 18, TypeScript, Create React App (`react-scripts` 5)
- Context API + custom hooks
- styled-components (macro) + theme
- Axios
- Jest + React Testing Library (snapshots included)
- Firebase Hosting

## Project Structure
```text
src/
  components/          # App, Cart, Products, Filter, Github, Loader, Recruiter
  contexts/            # cart-context, products-context and related hooks
  commons/             # Checkbox, styled-components shim, theme, global styles
  services/            # products.ts (dev/production data sources)
  utils/               # formatPrice + test utilities
  static/              # products assets (.webp), cart/delete icons, JSON data
```

Key files:
- `src/index.tsx`: Wraps `App` with `ThemeProvider`, `ProductsProvider`, `CartProvider`.
- `src/services/products.ts`: Dev loads `static/json/products.json`; prod fetches Firebase.
- `src/components/Cart/*`: Floating cart, products list, quantity controls, subtotal.
- `src/components/Products/*`: Product grid, hover imagery, free shipping badge.
- `src/components/Filter/Filter.tsx`: Size checkboxes wired to products context.
- `src/commons/style/*`: Theming, global styles, responsive breakpoints.

## Getting Started
Requirements:
- Node `14.17.3` (see `package.json` and `.nvmrc`)
- npm

```bash
npm install
npm start
```
- Dev server: `http://localhost:3000`
- Dev data source: `src/static/json/products.json`

## Available Scripts
- `npm start` – start development server
- `npm run build` – production build to `build/`
- `npm test` – Jest tests (silent)
- `npm run test:watch` – tests in watch mode
- `npm run test:coverage` – coverage report (90%+ thresholds; 64% branches)
- `npm run lint` – ESLint on `src/`
- `npm run format` – format with Prettier
- `npm run deploy` – deploy to Firebase Hosting

## Testing
- 18 suites cover components, hooks, and utilities.
- Snapshot tests live under `__snapshots__/`.
- `utils/test/test-utils.tsx` provides a themed render helper.

## Deployment (Firebase Hosting)
1. Build: `npm run build`
2. Login: `firebase login`
3. Select project: `firebase use <project>`
4. Deploy: `npm run deploy`

`firebase.json` rewrites all routes to `index.html` for SPA routing.

## Data Sources
- Dev: `require('static/json/products.json')`
- Prod: `axios.get('https://react-shopping-cart-67954.firebaseio.com/products.json')`

## Accessibility & UX
- Keyboard navigable product cards with `tabIndex` and `onKeyUp` handlers.
- `:focus-visible` outlines using theme colors.
- Hover transitions for imagery and CTA buttons.

## Customization
- Update branding/colors via `src/commons/style/theme.ts`.
- Adjust breakpoints in `theme.ts` and component styles.
- Replace recruiter info in `src/components/Recruiter/Recruiter.tsx`.
- Swap assets in `src/static/products/` and update `products.json`.

## Roadmap
- Persist cart state (localStorage or backend API)
- Add sorting, price filters, and pagination
- Replace alert checkout with a modal/route; integrate payments
- Add E2E tests (Cypress/Playwright) for core flows

## License
This project is provided as-is for demonstration and educational purposes.







