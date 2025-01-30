# fast-react-pizza

fast -react-pizza is an app on which users can order pizzza and it gets deleivered to their homes.This app demonstrates the professional app building in react using some advances tools and techniques.

## How to Build and Plan A React Application (small):

(theses steps works well for small apps with one page and a few components.In real world apps we need to adapt the process)

- Break the desired Ui into components.
- Build a static version (no state yet).
- Think abount state management and data flows.

## How to Build and Plan A Professional React Application:

- 1. gathering application requirements and features.
- 2. based on requirements divide the application into multiple pages.
     - think about overall and page level UI.
     - break the desired UI into components.
     - design and build static version (no state yet)
- 3. divide the application into feature categories.
     - Think about state management and data flows(for each of feature categories we define we need to think what data it needs and where it needs to be placed)
- 4. decide on what libraries we want to use(technology decisions)

## Project Requirements from the business

- very simple app , where users can order one or more pizza from the menu
- requires no user account and no login,users just input their names before using the app.
- pizza menu can change so it should be loaded from an API.
- users can add multiple pizzas to cart before they order.
- GPS location should be provided to make deleivry easy.
- user can amrk their order as a priority order, for an additional 20% of the cart price.
- orders are made by sending the Post Request with the order data to the API.
- no payment processing , payment on deleivry.
- each order will get a uniqueID,so users can look up their order based on their ID.
- users be able to mark their order as priority even after the order is placed

# Feature Categories:

- User
- Menu
- Cart
- Order

# Necessary Pages:

- homepage /
- pizza menu /menu
- cart /cart
- placing a new order /order/new
- looking up an order /order/:orderID (by passing order ID as param)

# State management + Technology decisions:

## State domain / slices

- User --> global UI state (no accounts,so stays in app)
- Menu --> global remote state (menu is fetched from API)
- Cart --> global UI state (no need fro API,just stored in app)
- Order --> global remote state (fetched and submitted to API)

## Technology Stacks:

- routing --> react router (Standard for React APIs)
- styling --> tailwind (trendy way of styling apps)
- remote state mangement --> using react router (new way of fetching data right inside the React Router (render as you fetch instead of fetch as you render) Not really a state management as it does not persist state)
- UI state management - Using Redux
