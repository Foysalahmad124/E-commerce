# Ecommers

Professional Node.js/Express e-commerce platform with MongoDB, featuring admin and user roles, shopping cart, and order management.

## Setup
1. Install dependencies: `npm install`
2. Start MongoDB: `mongod --dbpath "C:\data\db"`
3. Setup database: `node db-setup.js`
4. Seed products: `node seed-products.js`
5. Seed admin users: `node seed-admins.js`
6. Start server: `npm run dev` (requires nodemon) or `npm start`

## Database Collections
- users: User accounts with role-based access (admin/user)
- products: Product catalog with pricing, stock, ratings
- orders: Order history with shipping and payment details
- admins: Admin user permissions and management data
- item: Time-series collection for analytics

## Admin Accounts
After running `node seed-admins.js`, you can login with:

### Super Admin (Full Access)
- Email: `superadmin@ecommerce.com`
- Password: `password123`
- Permissions: All (products, orders, users, analytics, settings)

### Senior Admin
- Email: `admin@ecommerce.com`
- Password: `password123`
- Permissions: Products, orders, users, analytics

### Junior Admin
- Email: `junioradmin@ecommerce.com`
- Password: `password123`
- Permissions: Products, orders only

## Features
- ✅ User registration and authentication
- ✅ Role-based access control (admin/user)
- ✅ Product catalog with search and filtering
- ✅ Shopping cart with session persistence
- ✅ Order placement and confirmation
- ✅ Admin dashboard and management
- ✅ Responsive design with modern UI/UX
- ✅ Payment method placeholders (Credit Card, Mobile Money, Bank Transfer)

## API Endpoints
- `GET /` - Home page
- `GET /products` - Product catalog
- `GET /cart` - Shopping cart
- `GET /checkout` - Checkout process
- `GET /admin` - Admin dashboard
- `GET /user` - User dashboard

## Tech Stack
- Backend: Node.js, Express.js
- Database: MongoDB with Mongoose ODM
- Authentication: express-session, bcrypt
- Templating: EJS with express-ejs-layouts
- Styling: Custom CSS with modern design system
- Session Storage: express-session (in-memory)

