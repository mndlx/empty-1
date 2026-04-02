You are an AI agent tasked with building the MarketStock.FrontendApp using React and TypeScript. Follow these instructions:

1. Project Setup
   • Initialize a new React project (using Create React App or Vite) named marketstock-frontend with TypeScript support.
   • Configure ESLint, Prettier, and Husky for code quality and pre-commit hooks.

2. Architecture & State Management
   • Organize code into src/components, src/pages, src/services, src/hooks, and src/types.
   • Use React Router for navigation.
   • Choose a state management solution (Context API or Redux Toolkit) to manage global state: products, stock transactions, and restock orders.

3. UI Components & Pages
   • ProductsListPage: fetch and display all products with columns for name, stock level, expiration status, and low-stock indicator. Include filter for expired/low-stock.
   • ProductFormPage: form to create or edit products (name, description, expiration date, reorder threshold).
   • StockMovementPage: two separate forms or tabs for stock in and stock out operations.
   • RestockOrderPage:
     – List existing restock orders.
     – Form to place a new restock order (select product, enter quantity).

4. API Integration
   • Create a service layer (src/services/api.ts) using Axios or fetch:
     – GET /api/products
     – GET /api/products/{id}
     – POST /api/products
     – PUT /api/products/{id}
     – POST /api/products/{id}/stock/in
     – POST /api/products/{id}/stock/out
     – GET /api/restock-orders
     – POST /api/restock-orders
     – PUT /api/restock-orders/{id}
   • Handle loading states, errors, and success notifications.

5. Styling & UX
   • Use a component library like Material-UI or Bootstrap for consistent styling.
   • Show visual indicators for expired products (e.g., red highlight) and low-stock items (e.g., yellow badge).
   • Add form validation and user feedback on success/failure.

6. Testing & Deploy
   • Write unit tests for critical components using Jest and React Testing Library.
   • Set up a GitHub Actions workflow (.github/workflows/frontend-ci.yml) to:
     – Install dependencies
     – Run lint, format checks
     – Run unit tests
     – Build the production bundle

7. Environment & Deployment
   • Use environment variables for the backend API base URL.
   • Provide instructions or scripts to deploy the built frontend to a static hosting service (e.g., Netlify, Vercel, AWS S3 + CloudFront).

Deliver the complete React TypeScript frontend in a Git repository ready for deployment.