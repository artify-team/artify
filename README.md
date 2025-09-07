Artify - Real-time Auction Platform
A modern real-time auction platform for collectibles and art pieces, featuring AI-powered bidding insights and real-time notifications.

Features
Core Functionality
Real-time Bidding: Live auction updates using Socket.IO
User Authentication: Secure JWT-based authentication system
Item Management: Browse and search auction items with detailed views
Bid History: Complete bidding history and tracking
AI-Powered Features
Smart Analysis: AI-powered item valuation using Google Gemini 1.5 Flash
Price Prediction: Intelligent price forecasting based on market trends
Bidding Strategy: Personalized bidding recommendations
User Experience
Responsive Design: Mobile-first approach with Tailwind CSS
Real-time Notifications: Instant updates for bid activities
Countdown Timers: Live auction end-time tracking
Professional UI: Clean, gallery-inspired interface
Technology Stack
Frontend
React 19 - Modern UI library
React Router Dom 7 - Client-side routing
Tailwind CSS 3 - Utility-first styling
Vite 7 - Fast build tool and dev server
Socket.IO Client - Real-time communication
Axios - HTTP client
React Hook Form - Form handling
SweetAlert2 - Enhanced notifications
Backend
Node.js - Runtime environment
Express.js - Web application framework
Socket.IO - Real-time bidirectional communication
Sequelize - PostgreSQL ORM
PostgreSQL - Primary database
JWT - Authentication tokens
bcryptjs - Password hashing
AI Integration
Google Gemini 1.5 Flash - AI analysis and predictions
Custom AI Services - Price prediction and bidding strategies
Installation
Prerequisites
Node.js (v18 or higher)
PostgreSQL (v12 or higher)
npm or yarn package manager
Backend Setup
Navigate to the server directory:
cd server
Install dependencies:
npm install
Configure environment variables:
cp .env.example .env
Edit the .env file with your configuration:

NODE_ENV=development
PORT=3001
DB_HOST=localhost
DB_PORT=5432
DB_NAME=artify_db
DB_USERNAME=postgres
DB_PASSWORD=your_password
JWT_SECRET=your_jwt_secret
GEMINI_API_KEY=your_gemini_api_key
SOCKET_CORS_ORIGIN=http://localhost:3000
Setup database:
npm run db:create
npm run db:migrate
npm run db:seed
Start the server:
npm run dev
Frontend Setup
Navigate to the client directory:
cd client
Install dependencies:
npm install
Start the development server:
npm run dev
The application will be available at:

Frontend: http://localhost:3000
Backend API: http://localhost:3001
API Documentation
The API provides comprehensive endpoints for authentication, item management, bidding, and AI features. Key endpoints include:

Authentication
POST /api/auth/register - User registration
POST /api/auth/login - User login
Items
GET /api/items - Get all auction items
GET /api/items/:id - Get specific item details
Bidding
GET /api/bids/:itemId - Get item bid history
POST /api/bids - Place a new bid (authenticated)
AI Features
POST /api/ai/why-worth-it - AI item analysis
POST /api/ai/price-prediction - Price forecasting
POST /api/ai/bidding-strategy - Bidding recommendations
For complete API documentation, see API_DOCUMENTATION.md.

Real-time Features
The platform uses WebSocket connections for real-time updates:

Live bid updates
Auction countdown timers
Instant notifications
Real-time price changes
Project Structure
artify/
├── client/                 # React frontend application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/         # Page components
│   │   ├── context/       # React context providers
│   │   ├── services/      # API service functions
│   │   ├── hooks/         # Custom React hooks
│   │   └── utils/         # Utility functions
│   └── public/            # Static assets
├── server/                # Node.js backend application
│   ├── controllers/       # Route controllers
│   ├── models/           # Database models
│   ├── routes/           # API routes
│   ├── middlewares/      # Custom middleware
│   ├── services/         # Business logic services
│   ├── sockets/          # Socket.IO handlers
│   ├── migrations/       # Database migrations
│   └── seeders/          # Database seed files
└── README.md
Database Schema
The application uses PostgreSQL with the following main entities:

Users: Authentication and user profiles
Items: Auction items with details and pricing
Bids: Bidding history and current prices
Development
Available Scripts
Backend (server/)
npm run dev - Start development server with nodemon
npm start - Start production server
npm run db:migrate - Run database migrations
npm run db:seed - Seed database with sample data
npm run db:reset - Reset and reseed database
Frontend (client/)
npm run dev - Start development server
npm run build - Build for production
npm run preview - Preview production build
npm run lint - Run ESLint
Code Quality
The project includes:

ESLint configuration for code consistency
React hooks and best practices enforcement
Consistent error handling patterns
Comprehensive API response formatting
Deployment
Production Deployment
Set up production environment variables
Build the frontend application
Configure database for production
Deploy backend with PM2 or Docker
Serve frontend through nginx or CDN
For detailed deployment instructions, see DEPLOYMENT.md.

Environment Configuration
Ensure all required environment variables are set:

Database connection details
JWT secret for authentication
Google Gemini API key for AI features
CORS origins for frontend integration
Contributing
Fork the repository
Create a feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request
Security
JWT-based authentication with secure token handling
Input validation and sanitization
CORS configuration for secure cross-origin requests
Environment variable protection for sensitive data
Rate limiting on API endpoints
Performance
Efficient database queries with proper indexing
Real-time updates without polling
Optimized frontend builds with Vite
Connection pooling for database operations
Lazy loading for improved initial load times
License
This project is licensed under the ISC License.

Support
For questions or support, please open an issue in the GitHub repository.

Built with modern web technologies for the future of online auctions.

---

**Made with ❤️ by Artify Team**

_If you found this project helpful, please consider giving it a ⭐!_

