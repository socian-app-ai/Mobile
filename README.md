# 🎓 Socian - Beyond The Class

[![Flutter](https://img.shields.io/badge/Flutter-3.5.4-blue.svg)](https://flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-3.5.4-blue.svg)](https://dart.dev/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-1.0.0-orange.svg)](pubspec.yaml)
[![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20iOS%20%7C%20Web-lightgrey.svg)](https://flutter.dev/)

> A campus-focused social platform that connects students, alumni, and educators for academic collaboration, career opportunities, and university-wide engagement.

## 📋 Table of Contents

- [About](#-about)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [Environment Variables](#-environment-variables)
- [API Documentation](#-api-documentation)
- [Contributing](#-contributing)
- [License](#-license)
- [Credits](#-credits)
- [Demo](#-demo)

## 🎯 About

**Socian – Beyond The Class** exists to bridge the communication and collaboration gap within academic institutions by providing a centralized, role-based platform for students, alumni, and educators. Traditional platforms like Facebook groups, LinkedIn, or Discord either lack academic structure, are hard to moderate, or fail to foster meaningful university-level engagement.

### 🚀 Purpose

This project solves several pain points in the academic ecosystem:

- **Students** repeatedly asking about teachers, courses, or past papers across scattered forums
- **Alumni** struggling to reconnect with their campus or offer referrals in a structured way
- **Educators and student councils** having no direct feedback loop or petition system
- **Lack of community collaboration** for policy change, event organization, or academic help

By offering features like verified communities, teacher reviews, alumni referral systems, real-time chat, searchable past papers, and AI-powered moderation, Socian ensures that academic dialogue goes "beyond the class."

### 🎯 Target Audience

- **Students** seeking academic support, community bonding, and transparency
- **Alumni** wanting to give back through mentorship, job referrals, and hiring
- **Educators and Admins** looking for structured feedback, engagement, and outreach
- **External Organizations** aiming to connect with verified university talent pools in an ethical and streamlined way

## ✨ Features

### 🔍 Core Features

- **Verified Campus Communities**: Users join using university email with dynamic regex validation; ensures only real students, alumni, teachers, and approved organizations access campus-specific spaces
- **Academic Collaboration Hub**: Access and contribute to past papers, teacher reviews, course advice, and real-time discussion threads—making it easier for students to learn from each other
- **Alumni-Powered Job & Internship Referrals**: Alumni can post verified job/internship opportunities and recommend students, creating a trusted pipeline beyond LinkedIn noise
- **AI-Powered Content Moderation**: Custom-built ML models filter NSFW or harmful content in real-time, keeping the platform respectful and secure for academic communities
- **Campus Navigation & Café Info**: Integrated campus maps and student-rated cafeteria reviews help new students and visitors explore their university easily
- **Role-Based Layouts & Notifications**: Each user type (student, alumni, teacher, external org) sees a tailored UI and notification flow, making their experience more focused and relevant

### 🚧 Upcoming Features

- 📱 In-app video Q&A and voice chat support
- 🤖 Smart feed recommendations using vector similarity + embeddings
- 🎓 Alumni mentorship scheduling module
- 🔗 API for universities to integrate with their internal systems

## 🛠️ Tech Stack

### Frontend

- **Mobile**: Flutter (Dart)
- **Web**: React.js (with Vite), Tailwind CSS

### Backend

- **Runtime**: Node.js, Express.js, Nest.js (select modules)
- **Database**: MongoDB (with Mongoose ODM)
- **Authentication**: JWT, bcrypt, dynamic email regex validation

### Cloud & DevOps

- **Cloud**: AWS (EC2, S3)
- **Deployment**: Vercel, GitHub Actions (CI/CD)
- **Mobile Deployment**: Play Store & App Store

### ML & AI

- **Content Moderation**: Custom NSFW Detection Model (Python)
- **Content Flagging**: Intelligent content flagging logic

### State Management

- **Web**: React Context API
- **Mobile**: Provider pattern (Flutter)

### API Communication

- **Web**: RESTful APIs using Axios
- **Mobile**: HTTP package (Flutter)

### Other Services

- **Maps**: Google Maps API
- **Email**: Resend, Zoho Mail
- **Push Notifications**: Firebase Cloud Messaging (FCM)
- **Monorepo Management**: pnpm with shared packages

## 📁 Project Structure

```
BeyondTheClass_mobile/
├── lib/
│   ├── core/                    # Core utilities and use cases
│   │   ├── utils/              # Utility functions and constants
│   │   └── usecases/           # Business logic use cases
│   ├── features/               # Feature-based modules
│   │   ├── auth/               # Authentication features
│   │   └── past_papers/        # Past papers functionality
│   ├── shared/                 # Shared components and services
│   │   ├── services/           # API services, WebSocket, etc.
│   │   └── widgets/            # Reusable UI components
│   ├── pages/                  # Screen pages and UI
│   ├── components/             # UI components
│   ├── theme/                  # App theming and styling
│   ├── utils/                  # Utility functions
│   └── ads/                    # Advertisement components
├── assets/                     # Images, animations, and static files
├── android/                    # Android-specific configurations
├── ios/                        # iOS-specific configurations
├── web/                        # Web platform configurations
├── test/                       # Test files
└── pubspec.yaml               # Flutter dependencies and configuration
```

## 🚀 Installation

### Prerequisites

- [Flutter SDK](https://flutter.dev/docs/get-started/install) (3.5.4 or higher)
- [Dart SDK](https://dart.dev/get-dart) (3.5.4 or higher)
- [Android Studio](https://developer.android.com/studio) (for Android development)
- [Xcode](https://developer.apple.com/xcode/) (for iOS development, macOS only)
- [Git](https://git-scm.com/)

### Step-by-Step Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/socian.git
   cd socian
   ```

2. **Install Flutter dependencies**

   ```bash
   flutter pub get
   ```

3. **Set up environment variables**

   ```bash
   cp .env.example .env
   # Edit .env with your actual values
   ```

4. **Run the application**

   ```bash
   # For development
   flutter run
   
   # For specific platforms
   flutter run -d android
   flutter run -d ios
   flutter run -d chrome
   ```

## 📱 Usage

### Getting Started

1. **Launch the app** and you'll be greeted with the splash screen
2. **Sign up/Login** using your university email for verification
3. **Join your campus community** and start exploring features
4. **Customize your profile** based on your role (student, alumni, teacher, etc.)

### Key Features Usage

#### 🔍 Campus Communities

- Join verified communities using your university email
- Access role-specific features and content
- Engage in academic discussions and collaborations

#### 📚 Academic Hub

- Browse and contribute to past papers
- Read and write teacher reviews
- Participate in course-related discussions

#### 💼 Alumni Network

- Post job and internship opportunities
- Connect with students for mentorship
- Access verified referral system

#### 🗺️ Campus Navigation

- Explore campus maps and locations
- Find and rate campus cafeterias
- Navigate university facilities

## 🔧 Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
# JWT Configuration
JTM=your_jwt_secret_key_here

# Google Services
GOOGLE_CLIENT_ID=your_google_client_id
MAPS_API_KEY=your_google_maps_api_key

# Giphy Integration
GIPHY_API_KEY=your_giphy_api_key

# Mobile Ads
NATIVE_AD_MOB=your_native_ad_unit_id

# Analytics (Optional)
POSTHOG_API=your_posthog_api_key
POSTHOG_HOST=your_posthog_host_url
```

### Required API Keys

- **Google Maps API**: For campus navigation features
- **Google Client ID**: For Google Sign-In authentication
- **Giphy API**: For GIF picker functionality
- **Mobile Ads**: For advertisement integration

## 📚 API Documentation

### Authentication Endpoints

```http
POST /api/auth/login
POST /api/auth/register
POST /api/auth/refresh
GET /api/auth/verify
```

### User Management

```http
GET /api/users/profile
PUT /api/users/profile
GET /api/users/{id}
```

### Communities

```http
GET /api/communities
POST /api/communities
GET /api/communities/{id}
POST /api/communities/{id}/join
```

### Past Papers

```http
GET /api/papers
POST /api/papers
GET /api/papers/{id}
PUT /api/papers/{id}
DELETE /api/papers/{id}
```

### Teacher Reviews

```http
GET /api/reviews
POST /api/reviews
GET /api/reviews/{id}
PUT /api/reviews/{id}
```

For complete API documentation, visit: `https://api.socian.com/docs`

## 🤝 Contributing

We welcome contributions from the community! Please follow these steps:

### Development Setup

1. **Fork the repository**
2. **Create a feature branch**

   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes** and ensure code quality
4. **Run tests**

   ```bash
   flutter test
   ```

5. **Commit your changes**

   ```bash
   git commit -m "feat: add your feature description"
   ```

6. **Push to your branch**

   ```bash
   git push origin feature/your-feature-name
   ```

7. **Create a Pull Request**

### Code Style Guidelines

- Follow [Dart Style Guide](https://dart.dev/guides/language/effective-dart/style)
- Use meaningful commit messages following [Conventional Commits](https://www.conventionalcommits.org/)
- Write tests for new features
- Update documentation as needed

### Reporting Issues

- Use the [GitHub Issues](https://github.com/yourusername/socian/issues) page
- Provide detailed bug reports with steps to reproduce
- Include device information and app version

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 Socian Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 🙏 Credits

### Team Members

- **Mobile Developer**: Muhammad Rayyan
- **UI/UX Designer**:  Muhammad Bilal Ellahi & Muhammad Rayyan
- **Backend Developer**: Muhammad Bilal Ellahi & Muhammad Rayyan
- **Web Developer**: Muhammad Bilal Ellahi

### Libraries & Tools

- [Flutter](https://flutter.dev/) - UI framework
- [Riverpod](https://riverpod.dev/) - State management
- [Dio](https://pub.dev/packages/dio) - HTTP client
- [Google Maps Flutter](https://pub.dev/packages/google_maps_flutter) - Maps integration
- [Firebase](https://firebase.google.com/) - Push notifications
- [MongoDB](https://www.mongodb.com/) - Database
- [Node.js](https://nodejs.org/) - Backend runtime

### Inspiration

- Campus social platforms
- Academic collaboration tools
- Professional networking applications

## 🎬 Demo

### Live Demo

- **Web App**: [https://socian.com](https://socian.com)
- **Mobile App**: Available on [Google Play Store](https://play.google.com/store/apps/details?id=community.socian.app) and [App Store](https://apps.apple.com/app/socian/id123456789)

### Screenshots

![Socian App Screenshots](assets/images/screenshots.png)

### Video Demo

[Watch Demo Video](https://youtube.com/watch?v=WILL-UPLOAD)

---

<div align="center">
  <p>Made with ❤️ by the Socian Team</p>
  <p>Connecting students, alumni, and educators beyond the classroom</p>
</div>


<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/socian_logo.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/socian_splash.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0003.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/student feedback reply.jpg"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/student feedbacks.jpg"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/students feedback on student console.jpg"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/teacher choose model.jpg"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/teacher choosing modals.jpg"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0004.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0005.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0006.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0007.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0008.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0009.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0010.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0011.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0012.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0013.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0014.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0015.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0016.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0017.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0018.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0019.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0020.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0021.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0022.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0023.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0024.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0025.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0026.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0027.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0028.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0029.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0030.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0031.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0032.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0033.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0034.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0035.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0036.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0037.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0038.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0039.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0040.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0041.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0042.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0043.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0044.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0045.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0046.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0047.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0048.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0049.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0050.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0051.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0052.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0053.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0054.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0055.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0056.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0057.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0058.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0059.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0060.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0061.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0062.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0063.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0064.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0065.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0066.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0067.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0068.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0069.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0070.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0071.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0072.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0073.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0074.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0075.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0076.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0077.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0078.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0079.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0080.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0081.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0082.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0083.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0084.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0085.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0086.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0087.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0088.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0089.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0090.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0091.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0092.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0093.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0094.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0095.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0096.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0097.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0098.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0099.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0100.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0101.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0102.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0103.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0104.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0105.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0106.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0107.webp"/>
<img src="https://bilalellahi.com/Projects Information/Socian/mobile/socian/webp/IMG-20250724-WA0108.webp"/>

