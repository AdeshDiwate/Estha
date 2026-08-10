# Estha 🛕🌏

### Explore. Learn. Experience India's Spiritual & Cultural Heritage.

**Estha** is a web platform designed to make India's rich spiritual, religious, and cultural heritage more accessible through a modern digital experience.

The platform brings together information about **religious and heritage destinations, cultural content, books, blogs, and organizations** in one place. Estha aims to create a meaningful bridge between traditional heritage and modern technology by providing users with an intuitive and visually engaging way to discover India's diverse cultural landscape.

> **Live Demo:** `estha-beta.vercel.app`

---

## ✨ Features

### 🛕 Spiritual & Heritage Destinations

* Explore curated religious and heritage destinations.
* View destination name, city, state, religion, and associated imagery.
* Includes destinations representing multiple faiths and cultural traditions.
* Current dataset includes places such as:

  * Hazrat Nizamuddin Dargah
  * Akshardham
  * Sri Harmandir Sahib
  * Jama Masjid
  * Sanchi Stupa
  * Ram Janmabhoomi Temple
  * Santa Cruz Cathedral Basilica

### 📚 Books & Cultural Resources

* Dedicated book discovery section.
* Reusable card and slider components for presenting cultural resources.
* Designed to make heritage-related reading material easier to discover.

### 📰 Blogs & Articles

* Blog-focused content section.
* Reusable blog cards and sliders.
* Provides a foundation for publishing cultural, historical, spiritual, and travel-related content.

### 🏛️ Organizations

* Dedicated section for cultural and religious organizations.
* Organization cards and sliders provide a structured way to showcase relevant institutions.

### 🔐 User Authentication

* User registration and login functionality.
* Authentication is implemented using **Appwrite**.
* Supports:

  * Account creation
  * Email/password login
  * Current-user retrieval
  * Logout/session management

### 🎨 Modern & Responsive UI

* Component-based React architecture.
* Interactive navigation and sliders.
* Motion and animation support.
* Modern card-based layouts.
* Tailwind CSS-based styling.
* Multiple UI libraries are integrated for reusable interface components.

### 🧭 Navigation

The application includes navigation for key sections such as:

* Home
* About
* Contact

---

## 🏗️ Tech Stack

| Category            | Technology                            |
| ------------------- | ------------------------------------- |
| Frontend            | React 18                              |
| Build Tool          | Vite                                  |
| Styling             | Tailwind CSS                          |
| State Management    | Redux Toolkit                         |
| Authentication      | Appwrite                              |
| Routing             | React Router DOM                      |
| UI Components       | Radix UI, NextUI, Headless UI         |
| Icons               | Tabler Icons, Heroicons, Lucide React |
| Animation           | Framer Motion                         |
| Sliders / Carousels | Swiper, React Slick, Embla Carousel   |
| Particle Effects    | tsParticles                           |
| Forms               | React Hook Form                       |
| Utility             | clsx, tailwind-merge                  |
| Deployment          | Vercel                                |

The project's dependency configuration confirms React 18, Vite, Tailwind CSS, Redux Toolkit, Appwrite, React Router, Framer Motion, Swiper, React Slick, Radix UI, NextUI, and other supporting libraries.

---

## 🧩 Project Architecture

Estha follows a component-based React architecture where UI elements, authentication services, application state, configuration, and static data are separated into dedicated modules.

```text
Estha/
│
├── public/
│   ├── esthalogo1.svg
│   └── vite.svg
│
├── src/
│   │
│   ├── appwrite/
│   │   └── auth.js
│   │
│   ├── assets/
│   │
│   ├── booksimg/
│   │
│   ├── components/
│   │   ├── AuthLayout.jsx
│   │   ├── BlogCard.jsx
│   │   ├── BlogCardSlider.jsx
│   │   ├── BooksCard.jsx
│   │   ├── BooksCardSlider.jsx
│   │   ├── Fnavbar.jsx
│   │   ├── Footer.jsx
│   │   ├── Header.jsx
│   │   ├── Login.tsx
│   │   ├── LogoutBtn.jsx
│   │   ├── Navbar.tsx
│   │   ├── OrgCards.jsx
│   │   ├── OrgCardSlider.jsx
│   │   ├── TempleCard.jsx
│   │   ├── TempleCardSlider.jsx
│   │   └── ui/
│   │
│   ├── conf/
│   │   └── conf.js
│   │
│   ├── datas/
│   │   └── templeData.js
│   │
│   ├── functionalities/
│   │   └── CardSlider.jsx
│   │
│   ├── store/
│   │   ├── authSlice.js
│   │   └── store.js
│   │
│   ├── image/
│   │
│   ├── homeimg/
│   │
│   ├── orgimg/
│   │
│   ├── App.jsx
│   ├── App.css
│   ├── index.css
│   └── main.jsx
│
├── .gitignore
├── components.json
├── index.html
├── package.json
├── package-lock.json
├── postcss.config.js
├── tailwind.config.js
├── tsconfig.json
└── vite.config.js
```

---

## 🔐 Authentication Architecture

Estha uses **Appwrite** as its authentication service.

The authentication layer is encapsulated inside:

```text
src/appwrite/auth.js
```

The service provides methods for:

```text
createAccount()
login()
getCurrentUser()
logout()
```

Appwrite configuration is loaded through environment variables:

```text
VITE_APPWRITE_URL
VITE_APPWRITE_PROJECT_ID
```

Authentication state is then managed using Redux Toolkit through:

```text
src/store/authSlice.js
```

The Redux authentication state maintains:

```text
status
userData
```

This separation keeps authentication logic independent from the UI layer.

---

## ⚙️ Getting Started

Follow the steps below to run Estha locally.

### 1. Clone the Repository

```bash
git clone https://github.com/AdeshDiwate/Estha.git
```

### 2. Navigate to the Project

```bash
cd Estha
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Configure Environment Variables

Create a `.env` file in the project root:

```env
VITE_APPWRITE_URL=your_appwrite_endpoint
VITE_APPWRITE_PROJECT_ID=your_appwrite_project_id
```

> Never commit sensitive credentials or private configuration values to GitHub.

### 5. Start the Development Server

```bash
npm run dev
```

Vite will start the development server and provide a local URL in the terminal.

---

## 📜 Available Scripts

### Development

```bash
npm run dev
```

Starts the Vite development server.

### Production Build

```bash
npm run build
```

Creates an optimized production build.

### Preview Production Build

```bash
npm run preview
```

Runs the generated production build locally.

### Lint

```bash
npm run lint
```

Runs ESLint against the project source files.

---

## 🌐 Deployment

The project is configured as a Vite application and is currently deployed using **Vercel**.

For production deployment:

```bash
npm run build
```

The generated `dist/` directory can then be deployed through a compatible static hosting platform.

When deploying, make sure the required Appwrite environment variables are configured in the hosting provider.

---

## 🎯 Project Objective

India has an exceptionally diverse spiritual and cultural heritage spread across different religions, regions, languages, traditions, and historical periods.

However, information about these places and traditions is often scattered across different platforms.

Estha was designed around the idea of creating a centralized digital experience where users can:

* Discover spiritual destinations
* Learn about cultural heritage
* Explore religious places
* Discover books and educational resources
* Read cultural content
* Discover relevant organizations
* Interact with the platform through user authentication

The broader objective is to use technology to make cultural and spiritual exploration more accessible to a modern audience.

---

## 🧠 Design & Development Approach

Estha follows several software development principles:

### Component Reusability

Repeated UI patterns are abstracted into reusable React components such as:

```text
TempleCard
TempleCardSlider
BooksCard
BooksCardSlider
BlogCard
BlogCardSlider
OrgCards
OrgCardSlider
```

This makes the interface easier to maintain and extend.

### Separation of Concerns

The project separates:

* UI components
* Authentication services
* Configuration
* Application state
* Static data
* Styling
* Functional components

This creates a cleaner project structure and makes future development easier.

### Centralized State Management

Redux Toolkit is used to manage authentication state rather than keeping user state scattered across individual components.

---

## 🔮 Future Improvements

Estha can be extended into a more comprehensive cultural and pilgrimage platform.

Potential future improvements include:

* [ ] Detailed destination pages
* [ ] Search and advanced filtering
* [ ] Interactive maps
* [ ] Destination recommendations
* [ ] Historical timelines
* [ ] Live temple/event streaming
* [ ] Virtual tours
* [ ] User reviews and ratings
* [ ] Personalized user profiles
* [ ] Saved/favourite destinations
* [ ] Personalized pilgrimage planning
* [ ] Multilingual support
* [ ] Accessibility improvements
* [ ] Content management dashboard
* [ ] Dynamic backend/database integration
* [ ] Mobile application
* [ ] AI-powered cultural and destination recommendations

---

## 🛠️ Current Project Status

**Status:** Active Development / Prototype

The current repository primarily contains the frontend implementation and supporting authentication/state-management infrastructure.

The architecture has been structured to allow additional backend services, dynamic content, destination intelligence, and personalization features to be integrated in future iterations.

---

## 🤝 Contributing

Contributions and suggestions are welcome.

### Fork the repository

```bash
git fork
```

### Create a feature branch

```bash
git checkout -b feature/your-feature
```

### Commit your changes

```bash
git add .
git commit -m "Add: your feature"
```

### Push your branch

```bash
git push origin feature/your-feature
```

Then open a Pull Request.

---

## 📄 License

This project currently does not include a dedicated open-source license file.

If you intend to make Estha open source, add an appropriate `LICENSE` file to the repository before publishing or accepting external contributions.

---

## 👨‍💻 Author

### Adesh Diwate

Computer Science & Design

Interested in building technology-driven products at the intersection of **software engineering, data, AI, and user experience**.

---

## ⭐ Acknowledgements

Estha is built using the modern React ecosystem and several open-source UI and development libraries.

Special thanks to the open-source communities behind:

* React
* Vite
* Tailwind CSS
* Appwrite
* Redux Toolkit
* Radix UI
* NextUI
* Framer Motion
* Tabler Icons
* Heroicons
* Lucide React
* Swiper
* tsParticles

---

## 📌 Repository

**Estha — Spiritual & Cultural Heritage Platform**

Built with ❤️ using React, Vite, Tailwind CSS, Redux Toolkit, and Appwrite.
