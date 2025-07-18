# 🌱 EcoHive - Sustainability Idea Hub

<div align="center">
    <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js">
    <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
    <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
    <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">

</div>

<div align="center">
  <h3>🚀 <a href="https://sustainability-idea-hub-client-topaz.vercel.app/">Live Demo</a> | 🔧 <a href="https://github.com/Kamrul-Islam-171/idea-hub-backend">Backend Repository</a></h3>
</div>



## 🎯 About The Project

EcoHive is a comprehensive sustainability platform designed to address Bangladesh's environmental challenges through community-driven innovation. The platform serves as a collaborative hub where innovators, community members, and stakeholders can share, discover, and develop sustainable solutions.

### 🌍 Mission
To create a digital ecosystem that empowers communities to tackle environmental challenges through collective intelligence and innovative thinking.


## ✨ Features

### 👥 User Management
- **Secure Authentication**: JWT-based login and registration system
- **Role-Based Access**: User and admin role management
- **Profile Management**: Comprehensive user profile system

### 💡 Idea Management
- **Idea Submission**: Users can share their ideas.
- **Category Organization**: Browse ideas by Category.
- **Voting**: Upvote and comment on ideas.
- **Premium Content**: Publish and access premium content.
  
### 📊 Analytics & Insights
- **User Dashboard**: Personal idea management and analytics
- **Admin Dashboard**: Platform oversight and content moderation
- **Engagement Metrics**: Track idea performance and community engagement

### 🎨 User Experience
- **Responsive Design**: Optimized for all device sizes
- **Modern UI/UX**: Clean, intuitive interface design
- **Performance Optimized**: Fast loading and smooth interactions

---

## 🛠️ Tech Stack

### Frontend
- **Framework**: Next.js 
- **Language**: TypeScript
- **Styling**: TailwindCSS
- **UI Components**: Radix UI
- **Form Handling**: React Hook Form + Zod validation
- **State Management**: React Context API for user management and Redux for add-to-card.
- **Notifications**: Sonner toast notifications

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB with Mongoose
- **Authentication**: JWT
- **Validation**: Zod
- **File Upload**: Multer

### Development Tools
- **Version Control**: Git
- **Package Manager**: npm/yarn
- **Code Quality**: ESLint, Prettier
- **Deployment**: Vercel (Frontend), Railway/Heroku (Backend)

---

## 🚀 Getting Started

### Prerequisites
Before you begin, ensure you have the following installed:
- Node.js (v18.0.0 or higher)
- npm or yarn
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Kamrul-Islam-171/idea-hub.git
   cd idea-hub
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env.local
   ```

4. **Start the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

5. **Open your browser**
   Navigate to `http://localhost:3000`

### Environment Variables
Create a `.env.local` file in the root directory:

```env
# API Configuration
NEXT_PUBLIC_BACKEND_URL=http://localhost:5000/api
```

---

## 💻 Usage

### For Users
1. **Register/Login**: Create an account or sign in
2. **Browse Ideas**: Explore sustainability ideas by category
3. **Submit Ideas**: Share your innovative solutions
4. **Engage**: Vote and comment on ideas
5. **Track Progress**: Monitor your ideas through the review process

### For Admins
1. **Dashboard Access**: Comprehensive admin panel
2. **Content Moderation**: Review and approve submitted ideas
3. **User Management**: Manage user accounts and permissions
4. **Analytics**: Monitor platform engagement and performance

---

## 📁 Project Structure

```
src/
├── app/                    # Next.js App Router pages
│   ├── (auth)/            # Authentication pages
│   ├── dashboard/         # Dashboard pages
│   ├── ideas/             # Idea-related pages
│   └── layout.tsx         # Root layout
├── components/            # Reusable UI components
│   ├── ui/               # Base UI components
│   ├── forms/            # Form components
│   ├── dashboard/        # Dashboard-specific components
│   └── common/           # Common components
├── lib/                   # Utility functions
│   ├── actions/          # Server actions
│   ├── utils.ts          # Helper functions
│   └── validations.ts    # Validation schemas
├── providers/            # React context providers
├── services/             # API communication layer
├── types/                # TypeScript type definitions
├── hooks/                # Custom React hooks
├── constants/            # Application constants
└── assets/               # Static assets
```

---

## 📚 API Documentation

### Base URL
```
https://your-backend-url.com/api
```

### Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/login` | User login |
| POST | `/api/auth/refresh-token` | Refresh access token |
| POST | `/api/auth/change-password` | Change user password |
| POST | `/api/auth/forgot-password` | Request password reset |
| POST | `/api/auth/reset-password` | Reset password with token |

### User Management
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/user/create-user` | Create a new user |
| GET | `/api/user` | Get all users (admin only) |
| PATCH | `/api/user/:id/status` | Update user status (admin only) |
| PATCH | `/api/user/:id/role` | Update user role (admin only) |

### Ideas
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/idea` | Create a new idea |
| GET | `/api/idea` | Get all ideas with filtering |
| GET | `/api/idea/:id` | Get a single idea by ID |
| PATCH | `/api/idea/:id` | Update an idea |
| DELETE | `/api/idea/:id` | Delete an idea |
| PATCH | `/api/idea/:id/status` | Update idea status (admin only) |
| POST | `/api/idea/:id/submit` | Submit idea for review |

### Votes
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/vote/:ideaId` | Vote on an idea |
| GET | `/api/vote/:ideaId` | Get votes for an idea |

### Comments
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/comment/create` | Add a comment |
| GET | `/api/comment/:ideaId` | Get comments for an idea |
| DELETE | `/api/comment/:commentId` | Delete a comment (admin only) |

### Admin
| Method | Endpoint | Description |
|--------|----------|-------------|
| PATCH | `/api/admin/idea/:id/rejectIdea` | Reject an idea with feedback |

For detailed API documentation and request/response examples, visit: [Backend Repository](https://github.com/Kamrul-Islam-171/idea-hub-backend)



**Project Links**:
- Frontend Repository: [EcoHive Client](https://github.com/thesanchitadevi/sustainability-idea-hub-client)
- Backend Repository: [EcoHive Backend](https://github.com/Kamrul-Islam-171/idea-hub-backend)
- Live Demo: [EcoHive Platform](https://sustainability-idea-hub-client-topaz.vercel.app/)



## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) for the amazing React framework
- [TailwindCSS](https://tailwindcss.com/) for utility-first styling
- [Radix UI](https://www.radix-ui.com/) for accessible UI components
- [Vercel](https://vercel.com/) for seamless deployment
- The open-source community for inspiration and resources

