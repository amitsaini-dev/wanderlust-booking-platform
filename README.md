# Wanderlust – Full-Stack Rental Marketplace

Wanderlust is a full-stack Airbnb-inspired rental marketplace where users can discover properties, create listings, upload images, leave reviews, and explore locations on an interactive map. The application follows the MVC architecture and includes authentication, authorization, cloud image storage, geolocation services, and a responsive user interface.

## 🚀 Live Demo

**Live Application:** https://wonderlust-booking-platform.onrender.com/listings

**GitHub Repository:** https://github.com/amitsaini-dev/wonderlust-booking-platform

---

## ✨ Features

### Property Listings
- Browse all available listings
- View detailed property information
- Create, edit, and delete listings
- Upload property images
- Property ownership management

### Authentication & Authorization
- User registration and login
- Secure authentication using Passport.js
- Session-based login management
- Protected routes for authenticated users
- Owner-only listing modification and deletion
- Review author authorization

### Reviews & Ratings
- Add reviews to listings
- Star-based rating system
- Delete personal reviews
- Review ownership validation

### Image Management
- Cloudinary integration for image storage
- Secure image uploads using Multer
- Automatic image replacement during updates
- Optimized image rendering

### Maps & Location Services
- Mapbox Geocoding integration
- Interactive maps for each listing
- Automatic coordinate generation from location names
- Property location markers

### User Experience
- Responsive design for mobile, tablet, and desktop
- Flash success and error notifications
- Form validation with Bootstrap
- Server-side validation using Joi
- Clean and intuitive UI

---

## 🏗️ Architecture

The application follows the **MVC (Model-View-Controller)** architecture:

```text
Client
  │
  ▼
Express Routes
  │
  ▼
Middleware Layer
(Auth • Authorization • Validation)
  │
  ▼
Controllers
  │
  ▼
Mongoose Models
  │
  ▼
MongoDB Database
```

### External Services

```text
Cloudinary → Image Storage
Mapbox     → Geocoding & Maps
Render     → Deployment
MongoDB Atlas → Database
```

---

## 🛠️ Tech Stack

### Backend
- Node.js
- Express.js

### Database
- MongoDB Atlas
- Mongoose ODM

### Frontend
- EJS
- EJS-Mate
- Bootstrap 5
- CSS3
- JavaScript

### Authentication
- Passport.js
- Passport Local
- Passport Local Mongoose
- Express Session
- Connect Mongo

### Validation & Security
- Joi
- Connect Flash
- Cookie Parser

### File Uploads
- Multer
- Cloudinary
- Multer Storage Cloudinary

### Maps & Geolocation
- Mapbox GL JS
- Mapbox Geocoding API

### Deployment
- Render

---

## 📂 Key Features Implemented

### MVC Architecture
Business logic is separated into:
- Models
- Views
- Controllers

### Authentication
Implemented using:
- Passport.js
- Sessions
- Secure login persistence

### Authorization
Custom middleware ensures:
- Only listing owners can edit/delete listings
- Only review authors can delete reviews

### Validation
Dual-layer validation:
- Bootstrap client-side validation
- Joi server-side validation

### Error Handling
- Custom ExpressError class
- Async wrapper utility
- Centralized error handling middleware

### Database Relationships
Implemented using Mongoose references:
- User ↔ Listings
- User ↔ Reviews
- Listing ↔ Reviews

### Image Storage
Images are stored on Cloudinary and linked to listings via URLs.

### Geolocation
Listing locations are converted into coordinates using Mapbox Geocoding and displayed on interactive maps.

---

## 📸 Core Functionalities

### User Flow

1. Register or log in
2. Create a listing
3. Upload property image
4. Add property details and location
5. Location coordinates generated automatically
6. Listing displayed publicly
7. Users can review and rate properties
8. Owners can manage their listings

---

## ⚙️ Environment Variables

Create a `.env` file in the root directory and add:

```env
ATLASDB_URL=your_mongodb_connection_string

SECRET=your_session_secret

CLOUD_NAME=your_cloudinary_cloud_name
CLOUD_API_KEY=your_cloudinary_api_key
CLOUD_API_SECRET=your_cloudinary_api_secret

MAP_TOKEN=your_mapbox_access_token
```

---

## 📦 Installation

### Clone Repository

```bash
git clone https://github.com/amitsaini-dev/wonderlust-booking-platform.git
```

### Navigate to Project

```bash
cd wonderlust-booking-platform
```

### Install Dependencies

```bash
npm install
```

### Seed Database

```bash
node init/index.js
```

### Start Application

```bash
node app.js
```

### Open Browser

```text
http://localhost:8080/listings
```

---

## 🎯 Concepts Demonstrated

- RESTful Routing
- MVC Architecture
- Authentication & Authorization
- Session Management
- Flash Messaging
- Middleware Design
- Database Relationships
- Image Upload Pipelines
- Geolocation Services
- Cloud Deployment
- Error Handling
- Data Validation
- Responsive Web Design

---

## 🚀 Future Improvements

- AI-powered property search using RAG and vector embeddings
- Property search and advanced filtering
- Wishlist/Favorites functionality
- Booking and reservation system
- Payment gateway integration
- Admin dashboard
- Property categories
- Pagination and lazy loading
- Redis caching
- JWT-based API support
- React frontend version

---

## 👨‍💻 Developer

**Amit Saini**

- GitHub: https://github.com/amitsaini-dev
- Email: amitsaini.ce@gmail.com

---

If you found this project interesting, consider giving it a ⭐ on GitHub.
