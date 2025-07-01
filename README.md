# 🏫 Astra Preschool ERP System

A comprehensive **Enterprise Resource Planning (ERP)** system designed specifically for **Astra Preschool** to manage student records, fee payments, and generate receipts efficiently.

## 🌟 Features

### 🔐 Authentication System
- **User Registration** - Create new admin accounts
- **Secure Login** - JWT-based authentication
- **Session Management** - Automatic token handling

### 👶 Student Management
- **Add New Students** - Register students with class information
- **Fee Management** - Track fee payments and outstanding balances
- **Class Organization** - Organize students by Play Group, Nursery, LKG, UKG
- **Search Functionality** - Quick student lookup by name
- **Record Management** - View, update, and delete student records

### 🧾 Receipt Generation
- **Digital Receipts** - Generate professional payment receipts
- **Print Functionality** - Print receipts directly from browser
- **Download Options** - Save receipts as HTML files
- **Automatic Calculations** - Calculate totals and balances

### 🎨 User Interface
- **Modern Design** - Clean and intuitive interface
- **Dark/Light Mode** - Toggle between themes
- **Responsive Layout** - Works on desktop and mobile devices
- **Real-time Updates** - Live data synchronization

## 🛠️ Technology Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **JWT** - Authentication
- **bcryptjs** - Password hashing
- **CORS** - Cross-origin resource sharing

### Frontend
- **React.js** - Frontend framework
- **React Router** - Navigation
- **Axios** - HTTP client
- **CSS3** - Styling
- **Context API** - State management

## 📂 Project Structure

```
astra-preschool/
├── backend/
│   ├── config/
│   │   └── database.js          # MongoDB connection
│   ├── controllers/
│   │   ├── authController.js    # Authentication logic
│   │   └── studentController.js # Student CRUD operations
│   ├── middleware/
│   │   └── auth.js              # JWT middleware
│   ├── models/
│   │   ├── User.js              # User schema
│   │   └── Student.js           # Student schema
│   ├── routes/
│   │   ├── auth.js              # Auth routes
│   │   └── students.js          # Student routes
│   ├── .env                     # Environment variables
│   ├── server.js                # Main server file
│   └── package.json
└── frontend/
    ├── public/
    │   ├── myapplogo.jpeg       # School logo
    │   └── index.html
    ├── src/
    │   ├── components/
    │   │   ├── Dashboard.js     # Main dashboard
    │   │   ├── Login.js         # Login component
    │   │   ├── Register.js      # Registration component
    │   │   └── Receipt.js       # Receipt component
    │   ├── context/
    │   │   └── AuthContext.js   # Authentication context
    │   ├── services/
    │   │   └── api.js           # API configuration
    │   ├── styles/
    │   │   ├── globals.css      # Global styles
    │   │   ├── Dashboard.css    # Dashboard styles
    │   │   └── Login.css        # Login/Register styles
    │   ├── App.js               # Main app component
    │   └── index.js             # Entry point
    └── package.json
```

## 🚀 Installation & Setup

### Prerequisites
- **Node.js** (v14 or higher)
- **MongoDB** (local or MongoDB Atlas)
- **npm** or **yarn**

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/astra-preschool-erp.git
cd astra-preschool-erp
```

### 2. Backend Setup
```bash
cd backend
npm install
```

Create a `.env` file in the backend directory:
```env
MONGODB_URI=mongodb://localhost:27017/astra-preschool
# Or for MongoDB Atlas:
# MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/astra-preschool

JWT_SECRET=your-super-secret-jwt-key-here
PORT=5000
```

### 3. Frontend Setup
```bash
cd ../frontend
npm install
```

### 4. Start the Application

**Start Backend Server:**
```bash
cd backend
npm start
# Server runs on http://localhost:5000
```

**Start Frontend Development Server:**
```bash
cd frontend
npm start
# Application runs on http://localhost:3000
```

## 📱 Usage Guide

### Initial Setup
1. **Register an Admin Account**
   - Navigate to `/register`
   - Create your admin credentials
   - Login with your new account

### Adding Students
1. **Access Dashboard**
   - Login to access the main dashboard
   - Fill in the student registration form
   - Select appropriate class (Play Group, Nursery, LKG, UKG)
   - Enter fee paid and balance amounts
   - Submit to create student record

### Managing Records
1. **Search Students**
   - Use the search bar to find specific students
   - Results update in real-time

2. **Generate Receipts**
   - Click "Download Receipt" on any student card
   - Print or save the generated receipt
   - Professional format with school letterhead

### Theme Customization
- Toggle between light and dark modes using the theme switch in the header

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login

### Students
- `GET /api/students` - Get all students (with search)
- `POST /api/students` - Create new student
- `PUT /api/students/:id` - Update student
- `DELETE /api/students/:id` - Delete student

## 🎨 Screenshots

### Login Page
- Clean, professional login interface
- School branding and logo
- Responsive design

### Dashboard
- Comprehensive student management
- Real-time search functionality
- Dark/Light mode toggle
- Receipt generation

### Student Records
- Card-based layout
- Quick actions for each student
- Professional receipt downloads

## 🔒 Security Features

- **Password Hashing** - bcrypt encryption
- **JWT Tokens** - Secure authentication
- **Protected Routes** - Authentication required
- **Input Validation** - Server-side validation
- **CORS Configuration** - Secure cross-origin requests

## 🌐 Environment Variables

Create a `.env` file in the backend directory with:

```env
# Database
MONGODB_URI=your_mongodb_connection_string

# Authentication
JWT_SECRET=your_jwt_secret_key

# Server
PORT=5000
```

## 📋 School Information

**Astra Preschool**
- **Address**: 5th Cross, Ganesh Temple Road, Sadashiv Nagar, Tumkur - 572101
- **Phone**: 9008887230
- **Classes**: Play Group, Nursery, LKG, UKG

## 🚀 Deployment

### Backend Deployment (Railway/Heroku)
1. Set environment variables in your hosting platform
2. Deploy backend code
3. Update API base URL in frontend

### Frontend Deployment (Netlify/Vercel)
1. Build the React app: `npm run build`
2. Deploy the build folder
3. Configure redirects for React Router

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Known Issues

- Receipt printing requires browser print dialog
- Mobile responsiveness could be improved for complex forms
- File upload functionality not yet implemented

## 🔮 Future Enhancements

- [ ] **Student Photos** - Upload and display student images
- [ ] **Attendance Tracking** - Daily attendance management
- [ ] **Parent Portal** - Separate portal for parents
- [ ] **SMS Notifications** - Fee reminder notifications
- [ ] **Bulk Operations** - Import/export student data
- [ ] **Advanced Reporting** - Financial and academic reports
- [ ] **Multi-branch Support** - Support for multiple school locations
- [ ] **Mobile App** - React Native mobile application

## 💡 Support

For support and questions:
- **Email**: support@astrapreschool.com
- **Phone**: +91 9008887230
- **Issues**: [GitHub Issues](https://github.com/yourusername/astra-preschool-erp/issues)

## 🙏 Acknowledgments

- Built with ❤️ for Astra Preschool
- Thanks to all the educators who make early childhood education possible
- Special thanks to the React and Node.js communities

---

**Made with ❤️ for Astra Preschool | © 2025 All Rights Reserved**
