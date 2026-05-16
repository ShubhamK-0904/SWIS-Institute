# 🌍 SWIS Institute - Educational NGO Website

<p align="center">
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" />
  <img src="https://img.shields.io/badge/Tailwind%20CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />
</p>

---

## 🌟 Overview

**SWIS Institute Website** is a modern, responsive educational platform website for an NGO. Built with **React**, **Node.js**, and **Tailwind CSS**, it features a clean, accessible-first design with excellent UI/UX. Showcases web development best practices including semantic HTML, clean CSS architecture, and interactive JavaScript functionality.

**Perfect for:** Full-stack portfolio showcase, educational institution websites, NGO platforms.

---

## ✨ Key Features

- 🎨 **Modern Responsive Design**
  - Mobile-first approach
  - Responsive across all devices
  - Smooth animations
  - Clean, professional UI

- ♿ **Accessibility-First**
  - WCAG 2.1 compliant
  - Semantic HTML
  - Screen reader friendly
  - Keyboard navigation

- 🚀 **High Performance**
  - Optimized assets
  - Fast load times
  - Code splitting
  - Lazy loading

- 📱 **Full-Stack Architecture**
  - React frontend
  - Node.js backend
  - RESTful API
  - Database integration

- 📊 **Rich Content**
  - About section
  - Programs & courses
  - Success stories
  - Contact form
  - Event listing

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 18+, JavaScript ES6+ |
| **Styling** | Tailwind CSS, CSS3 |
| **Backend** | Node.js, Express |
| **Database** | MongoDB/PostgreSQL |
| **Package Manager** | npm/yarn |
| **Build Tool** | Webpack/Vite |

---

## 📋 Requirements

```
Node.js: 14.x or higher
npm: 6.x or higher
Git: 2.x or higher
```

---

## 🚀 Installation & Setup

### 1. **Clone Repository**
```bash
git clone https://github.com/ShubhamK-0904/SWIS-Institute.git
cd SWIS-Institute
```

### 2. **Install Dependencies**

**Frontend:**
```bash
cd frontend
npm install
```

**Backend:**
```bash
cd backend
npm install
```

### 3. **Environment Configuration**

Create `.env` file in backend:
```env
PORT=5000
DATABASE_URL=mongodb://localhost:27017/swis
NODE_ENV=development
JWT_SECRET=your_secret_key
```

### 4. **Run Development Server**

**Frontend (Terminal 1):**
```bash
cd frontend
npm start
```

**Backend (Terminal 2):**
```bash
cd backend
npm start
```

Visit: `http://localhost:3000`

---

## 📁 Project Structure

```
SWIS-Institute/
├── frontend/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── components/
│   │   │   ├── Header.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── Hero.jsx
│   │   │   ├── About.jsx
│   │   │   ├── Programs.jsx
│   │   │   └── Contact.jsx
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── About.jsx
│   │   │   └── Contact.jsx
│   │   ├── App.jsx
│   │   └── index.css
│   └── package.json
├── backend/
│   ├── routes/
│   │   ├── contact.js
│   │   ├── programs.js
│   │   └── events.js
│   ├── models/
│   │   ├── User.js
│   │   ├── Program.js
│   │   └── Event.js
│   ├── server.js
│   └── package.json
└── README.md
```

---

## 🎯 Main Pages & Features

### **Home Page**
- Hero section with call-to-action
- Featured programs
- Testimonials
- News & updates
- Contact CTA

### **About Page**
- Organization mission/vision
- History
- Team members
- Impact statistics
- Values

### **Programs Page**
- Course listings
- Program details
- Enrollment information
- Success stories
- Schedule

### **Contact Page**
- Contact form
- Location map
- Phone/email
- Social links
- Message submission

### **Events Page**
- Upcoming events
- Past events
- Event registration
- Calendar view
- Event details

---

## 🎨 Design Highlights

### **Color Palette**
```
Primary: #3B82F6 (Blue)
Secondary: #10B981 (Green)
Accent: #F59E0B (Amber)
Dark: #1F2937 (Gray-900)
Light: #F9FAFB (Gray-50)
```

### **Typography**
```
Headings: Inter, Poppins
Body: Inter, System fonts
Font Sizes: Responsive
Line Heights: Readable (1.5-1.8)
```

### **Spacing & Layout**
```
Grid System: 12-column
Breakpoints: 640px, 1024px, 1280px
Padding: 16px, 24px, 32px
Margins: Consistent spacing
```

---

## 🔄 API Endpoints

### **Contact**
```
POST /api/contact/submit
- Send contact form message
```

### **Programs**
```
GET /api/programs
- Get all programs

GET /api/programs/:id
- Get specific program

POST /api/programs/enroll
- Enroll in program
```

### **Events**
```
GET /api/events
- Get upcoming events

POST /api/events/register
- Register for event
```

---

## 💻 Component Examples

### **Header Component**
```jsx
import React from 'react';

export default function Header() {
  return (
    <header className="bg-white shadow-sm sticky top-0 z-50">
      <nav className="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
        <div className="text-2xl font-bold text-blue-600">SWIS</div>
        <ul className="flex gap-8">
          <li><a href="/">Home</a></li>
          <li><a href="/about">About</a></li>
          <li><a href="/programs">Programs</a></li>
          <li><a href="/contact">Contact</a></li>
        </ul>
      </nav>
    </header>
  );
}
```

### **Program Card Component**
```jsx
export default function ProgramCard({ program }) {
  return (
    <div className="bg-white rounded-lg shadow-lg p-6 hover:shadow-xl transition">
      <h3 className="text-xl font-bold mb-3">{program.title}</h3>
      <p className="text-gray-600 mb-4">{program.description}</p>
      <button className="bg-blue-600 text-white px-6 py-2 rounded hover:bg-blue-700">
        Learn More
      </button>
    </div>
  );
}
```

---

## 🎓 Learning Outcomes

Master these concepts:
- ✅ React component architecture
- ✅ Node.js/Express server setup
- ✅ Tailwind CSS utility-first design
- ✅ Responsive web design
- ✅ Accessibility best practices
- ✅ RESTful API design
- ✅ Form handling and validation
- ✅ Database integration

---

## 🚀 Deployment

### **Frontend (Vercel)**
```bash
npm run build
vercel deploy
```

### **Backend (Heroku)**
```bash
heroku create
git push heroku main
```

---

## 🔒 Security Features

- ✅ Input validation
- ✅ CSRF protection
- ✅ XSS prevention
- ✅ SQL injection prevention
- ✅ Secure headers
- ✅ Rate limiting
- ✅ HTTPS enforcement

---

## 📊 Performance Metrics

| Metric | Target |
|--------|--------|
| **Lighthouse Score** | 95+ |
| **Page Load Time** | <2s |
| **Core Web Vitals** | Green |
| **Accessibility Score** | 95+ |

---

## 🚀 Future Enhancements

- [ ] User authentication system
- [ ] Student portal
- [ ] Online course platform
- [ ] Payment integration
- [ ] Admin dashboard
- [ ] Email notifications
- [ ] Search functionality
- [ ] Multi-language support

---

## 🤝 Contributing

Contributions welcome!
1. Fork repository
2. Create feature branch
3. Make improvements
4. Submit pull request

---

## 📝 License

MIT License - see LICENSE file

---

## 👨‍💻 Author

**Shubham Kadam**
- GitHub: [@ShubhamK-0904](https://github.com/ShubhamK-0904)
- LinkedIn: [Shubham Kadam](https://www.linkedin.com/in/shubham-kadam-b8856031a/)
- Email: shubham85kadam@gmail.com

---

<p align="center">
  <strong>⭐ Give it a star if you found it helpful! ⭐</strong>
</p>

<p align="center">
  Made with ❤️ by Shubham Kadam | Last Updated: May 2026
</p>
