# SkyLink - Airline Operations Platform (front-end demo)

A browser-based airline booking and operations site: customer accounts, flight search and booking,
an admin dashboard with customer management, and a route map of India.

## Run it locally

Sign-in uses the browser's Web Crypto API, which needs `localhost` or `https`.

    python -m http.server 8000

Then open http://localhost:8000 (run the command inside the folder that contains index.html).
An internet connection is needed for the Leaflet library, map tiles and fonts. The India outline is built into the page.

## Put it online (free)

GitHub Pages: create a repository, upload `index.html` and `README.md`, then open
Settings > Pages > Deploy from branch (main, root). Netlify Drop also works: drag the folder onto it.

## Demo accounts

- Administrator: login ID `admin`, password `Admin@123`
- Customers: create an account from the Create account page.

## Features

- Account first: every page except Sign in and Create account needs a login. After creating an account the customer signs in with their login ID and password.
- Customer: search by route, date, passengers, status; sort; flight details with map; booking with passengers and meals; cancellation with a refund rule; printable confirmation.
- Free airline hotels (customers): partner hotels near each airport, free for a few hours (up to 6) or one day for passengers with a confirmed booking to or from that airport. Each hotel shows rooms taken, rooms left and a Full / Almost full / Available tag. Stays are released when the booking or flight is cancelled.
- Admin hotels: capacity table, edit total rooms, active stays with check-out.
- Admin: dashboard (scheduled, today, delayed, cancelled, bookings, customers, aircraft, occupancy), route popularity, add flight with aircraft conflict checks, delay or cancel flights, fleet list, activity log.
- Customer management: search, add, edit, reset password, disable or enable, delete (blocked while bookings are confirmed), view and cancel bookings.
- Route map: Leaflet with a built-in India outline (works even if map tiles fail to load), airport code labels and popups, planned routes sized by scheduled flights, airport filter.

