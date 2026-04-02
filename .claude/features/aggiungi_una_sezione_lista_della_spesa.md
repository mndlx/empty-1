You are the AI engineer for the ToDo Frontend. Implement a new “Lista della spesa” section in the React/TypeScript SPA.

1. Routing & Navigation:
   • Add a new route /shopping-lists in src/App.tsx or router config.
   • Add a navigation link in the header/nav component labeled “Lista della spesa.”

2. API Service Layer (src/services):
   • Create shoppingListService with methods:
     – getLists(): GET `${process.env.REACT_APP_CORE_SERVICE_URL}/shopping-lists`
     – getList(id)
     – createList(payload)
     – updateList(id, payload)
     – deleteList(id)
   • Create itemService with methods for items under a list.
   • Include Authorization header with Bearer token from React Keycloak context.

3. State Management & Components:
   • Use React Context or Redux slice for shopping lists and items.
   • Build components under src/components/shopping:
     – ShoppingListPage: displays all lists
     – ShoppingListDetails: shows items for a selected list, with forms to add/edit/delete items
   • Forms must validate name and quantity.
   • Conditionally render UI (e.g., list deletion) only for authenticated owner.

4. Styling & UX:
   • Use the existing component library (Material-UI or Bootstrap) for layout, tables, buttons, dialogs.
   • Ensure mobile responsiveness.

5. Permissions & Error Handling:
   • If API returns 401/403, show appropriate error or redirect to login.
   • Show loading indicators and success/error toasts.

6. Testing:
   • Write unit tests with Jest and React Testing Library for:
     – shoppingListService mocks
     – key components and flows: listing, creating, editing, deleting lists/items
   • Achieve coverage >80% for new code.

7. Configuration & Docs:
   • Update .env.example with REACT_APP_CORE_SERVICE_URL and any new vars.
   • Update README: instructions to run, new routes, env vars.

Adhere to existing conventions for hooks, contexts, and environment-driven endpoints. Ensure the feature integrates seamlessly with Keycloak authentication.