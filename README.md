# 🏠 Estate Management Application

A modern, full-stack real estate management platform built with React, Node.js, and real-time communication capabilities. This application enables users to browse, post, and manage real estate listings with interactive features like real-time chat, map integration, and comprehensive property management.

## ✨ Features

### 🏘️ Property Management
- **Property Listings**: Create and manage real estate posts with detailed information
- **Property Types**: Support for apartments, houses, condos, and land
- **Transaction Types**: Buy and rent options
- **Rich Media**: Multiple image uploads for property showcases
- **Location Services**: Integrated maps with latitude/longitude coordinates
- **Property Details**: Comprehensive property information including utilities, pet policies, income requirements, size, school ratings, and accessibility

### 👥 User Management
- **Authentication**: Secure user registration and login with JWT tokens
- **User Profiles**: Customizable user profiles with avatar support
- **Saved Properties**: Bookmark and save favorite properties
- **User Dashboard**: Manage personal listings and saved properties

### 💬 Real-Time Communication
- **Live Chat**: Real-time messaging between users
- **Chat Management**: Organized conversations with message history
- **Notifications**: Real-time updates for new messages and interactions

### 🎨 Modern UI/UX
- **Responsive Design**: Mobile-first approach with SCSS styling
- **Interactive Maps**: Leaflet integration for property location visualization
- **Rich Text Editor**: React Quill for detailed property descriptions
- **State Management**: Zustand for efficient client-side state management
- **Real-Time Updates**: Socket.io integration for live features

## 🛠️ Tech Stack

### Frontend
- **React 18** - Modern React with hooks and functional components
- **Vite** - Fast build tool and development server
- **SCSS/Sass** - Advanced CSS preprocessing
- **React Router DOM** - Client-side routing
- **Leaflet** - Interactive maps and geolocation
- **React Quill** - Rich text editor
- **Zustand** - Lightweight state management
- **Axios** - HTTP client for API communication
- **Socket.io Client** - Real-time communication

### Backend
- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework
- **Prisma** - Modern database ORM
- **MongoDB** - NoSQL database
- **JWT** - JSON Web Token authentication
- **Bcrypt** - Password hashing
- **CORS** - Cross-origin resource sharing
- **Cookie Parser** - Cookie handling middleware

### Real-Time Communication
- **Socket.io** - Real-time bidirectional communication
- **WebSocket** - Persistent connections for live updates

## 📁 Project Structure

```
full-stack-estate-main/
├── api/                    # Backend API server
│   ├── controllers/        # Route controllers
│   ├── middleware/         # Custom middleware
│   ├── routes/            # API route definitions
│   ├── lib/               # Utility libraries
│   ├── prisma/            # Database schema and migrations
│   └── app.js             # Main server file
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── routes/        # Application routing
│   │   ├── context/       # React context providers
│   │   ├── lib/           # Utility functions
│   │   └── App.jsx        # Main application component
│   ├── public/            # Static assets
│   └── package.json       # Frontend dependencies
└── socket/                 # Real-time communication server
    └── app.js             # Socket.io server
```

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v16 or higher)
- **npm** or **yarn** package manager
- **MongoDB** database (local or cloud instance)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/full-stack-estate.git
   cd full-stack-estate
   ```

2. **Set up environment variables**
   Create `.env` files in the `api/` directory:
   ```env
   DATABASE_URL="mongodb://localhost:27017/estate_app"
   JWT_SECRET="your_jwt_secret_key"
   CLIENT_URL="http://localhost:3000"
   ```

3. **Install backend dependencies**
   ```bash
   cd full-stack-estate-main/api
   npm install
   ```

4. **Install frontend dependencies**
   ```bash
   cd ../client
   npm install
   ```

5. **Install socket server dependencies**
   ```bash
   cd ../socket
   npm install
   ```

### Database Setup

1. **Set up MongoDB**
   - Install MongoDB locally or use MongoDB Atlas
   - Update the `DATABASE_URL` in your environment variables

2. **Run database migrations**
   ```bash
   cd full-stack-estate-main/api
   npx prisma generate
   npx prisma db push
   ```

### Running the Application

1. **Start the API server**
   ```bash
   cd full-stack-estate-main/api
   npm start
   # Server runs on http://localhost:8800
   ```

2. **Start the frontend development server**
   ```bash
   cd full-stack-estate-main/client
   npm run dev
   # Client runs on http://localhost:3000
   ```

3. **Start the socket server**
   ```bash
   cd full-stack-estate-main/socket
   npm start
   # Socket server runs on configured port
   ```

## 📱 Usage

### For Property Seekers
- Browse available properties with advanced filtering
- Save favorite properties to your profile
- Contact property owners through real-time chat
- View property locations on interactive maps
- Access detailed property information and amenities

### For Property Owners
- Create comprehensive property listings
- Upload multiple property images
- Set pricing and property details
- Manage inquiries through the chat system
- Update listing information in real-time

## 🔧 Development

### Available Scripts

**Frontend (Client)**
```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
```

**Backend (API)**
```bash
npm start            # Start production server
npm run dev          # Start development server (if configured)
```

### Code Structure

- **Components**: Reusable UI components in `client/src/components/`
- **Routes**: API endpoints in `api/routes/`
- **Controllers**: Business logic in `api/controllers/`
- **Database**: Prisma schema in `api/prisma/schema.prisma`

## 🌐 API Endpoints

- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User authentication
- `GET /api/users/:id` - Get user profile
- `GET /api/posts` - Get all property listings
- `POST /api/posts` - Create new property listing
- `GET /api/posts/:id` - Get specific property details
- `POST /api/chats` - Create new chat
- `GET /api/messages/:chatId` - Get chat messages

## 🔒 Security Features

- **JWT Authentication**: Secure token-based authentication
- **Password Hashing**: Bcrypt encryption for user passwords
- **CORS Protection**: Configured cross-origin resource sharing
- **Input Validation**: Server-side validation for all inputs
- **Secure Cookies**: HTTP-only cookies for session management

## 🚀 Deployment

### Frontend Deployment
```bash
cd client
npm run build
# Deploy the 'dist' folder to your hosting service
```

### Backend Deployment
```bash
cd api
npm install --production
# Set production environment variables
npm start
```

### Environment Variables for Production
```env
NODE_ENV=production
DATABASE_URL="your_production_mongodb_url"
JWT_SECRET="your_secure_jwt_secret"
CLIENT_URL="your_production_frontend_url"
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

If you encounter any issues or have questions:

- Create an issue in the GitHub repository
- Check the existing issues for solutions
- Review the code documentation and comments

## 🔮 Future Enhancements

- **Advanced Search**: Filters for price range, property type, and location
- **Image Optimization**: Automatic image compression and optimization
- **Push Notifications**: Browser and mobile push notifications
- **Analytics Dashboard**: Property view statistics and user analytics
- **Payment Integration**: Secure payment processing for property transactions
- **Mobile App**: React Native mobile application
- **AI Recommendations**: Machine learning-based property suggestions

---

**Built with ❤️ using modern web technologies**
