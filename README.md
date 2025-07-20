# ALX Listing App

A modern Airbnb clone built with Next.js, TypeScript, and TailwindCSS. This project serves as the foundation for a property listing platform, featuring reusable components, type-safe development, and responsive design.

## 🚀 Project Overview

The ALX Listing App is designed to showcase modern web development practices while building a scalable property rental platform. This initial milestone focuses on establishing a solid foundation with proper project structure, reusable components, and development best practices.

### Key Features

- **Modern Tech Stack**: Built with Next.js 13+, TypeScript, and TailwindCSS
- **Responsive Design**: Mobile-first approach with beautiful UI components
- **Type Safety**: Full TypeScript integration for robust code
- **Reusable Components**: Modular component architecture
- **Performance Optimized**: Next.js Image optimization and best practices
- **Developer Experience**: ESLint configuration for code quality

## 🏗️ Project Structure

```
alx-listing-app/
├── components/          # Reusable UI components
│   └── common/         # Common components used across the app
│       ├── Card.tsx    # Property card component
│       └── Button.tsx  # Reusable button component
├── interfaces/         # TypeScript interface definitions
│   └── index.ts       # All type definitions and interfaces
├── constants/         # Application constants and configuration
│   └── index.ts      # API URLs, UI text, app config
├── pages/            # Next.js pages (routing)
│   ├── index.tsx     # Home page
│   └── _app.tsx      # App configuration
├── public/           # Static assets
│   └── assets/       # Images, icons, and other static files
├── styles/           # Global styles and Tailwind configuration
│   └── globals.css   # Global CSS and Tailwind imports
├── tailwind.config.js # TailwindCSS configuration
├── tsconfig.json     # TypeScript configuration
├── next.config.js    # Next.js configuration
└── README.md         # Project documentation
```

### Directory Explanations

#### `/components/common/`
Houses reusable UI components that can be used throughout the application:
- **Card.tsx**: Displays property information with image, title, description, price, and rating
- **Button.tsx**: Flexible button component with multiple variants and states

#### `/interfaces/`
Contains TypeScript interface definitions for type safety:
- **CardProps**: Defines the structure for Card component properties
- **ButtonProps**: Defines the structure for Button component properties
- **PropertyListing**: Interface for property data structure

#### `/constants/`
Centralizes application constants for easy maintenance:
- API configuration and URLs
- UI text and labels
- Application settings and configuration
- Color schemes and design tokens

#### `/public/assets/`
Stores static assets like images, icons, and other files that need to be publicly accessible.

## 🛠️ Technology Stack

- **Next.js 13+**: React framework with file-based routing and optimization features
- **TypeScript**: Adds static type checking for better code quality and developer experience
- **TailwindCSS**: Utility-first CSS framework for rapid UI development
- **ESLint**: Code linting tool for maintaining code quality and consistency

## 📋 Prerequisites

Before running this project, make sure you have the following installed:

- **Node.js** (version 16 or higher)
- **npm** (comes with Node.js) or **yarn**
- **Git** for version control
- A modern web browser
- Code editor (VS Code recommended)

### Recommended VS Code Extensions

- ES7+ React/Redux/React-Native snippets
- Tailwind CSS IntelliSense
- TypeScript Importer
- Prettier - Code formatter
- ESLint

## 🚀 Getting Started

Follow these steps to run the project locally:

### 1. Clone the Repository

```bash
git clone <repository-url>
cd alx-listing-app
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. Start the Development Server

```bash
npm run dev
# or
yarn dev
```

### 4. Open in Browser

Navigate to [http://localhost:3000](http://localhost:3000) to view the application.

## 📦 Available Scripts

- `npm run dev` - Starts the development server on http://localhost:3000
- `npm run build` - Creates an optimized production build
- `npm run start` - Starts the production server (requires build first)
- `npm run lint` - Runs ESLint to check for code quality issues
- `npm run lint:fix` - Automatically fixes ESLint issues where possible

## 🎨 Styling with TailwindCSS

This project uses TailwindCSS for styling. Here are some key concepts:

### Utility Classes
- `bg-blue-600` - Background color
- `text-white` - Text color
- `p-4` - Padding
- `m-2` - Margin
- `rounded-lg` - Rounded corners
- `shadow-md` - Drop shadow

### Responsive Design
- `md:grid-cols-2` - 2 columns on medium screens and up
- `lg:text-xl` - Large text on large screens and up
- `sm:px-6` - Horizontal padding on small screens and up

### Hover Effects
- `hover:bg-blue-700` - Background color on hover
- `hover:scale-105` - Slight scale increase on hover

## 🔧 Configuration

### TailwindCSS Configuration

The `tailwind.config.js` file is configured to scan all relevant files for Tailwind classes:

```javascript
module.exports = {
  content: [
    './pages/**/*.{ts,tsx}',
    './components/**/*.{js,ts,jsx,tsx}',
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### TypeScript Configuration

The project includes a `tsconfig.json` with strict type checking enabled for better code quality.

## 🧩 Component Usage Examples

### Using the Card Component

```tsx
<Card
  imageSrc="/assets/property-1.jpg"
  imageAlt="Beautiful apartment"
  title="Modern Downtown Apartment"
  description="Stunning 2-bedroom apartment with city views"
  price="120"
  rating={4.8}
  location="New York, NY"
  onClick={() => handleCardClick('1')}
/>
```

### Using the Button Component

```tsx
<Button 
  variant="primary" 
  size="large"
  onClick={handleAction}
  loading={isLoading}
>
  Book Now
</Button>
```

## 🎯 Next Steps

This milestone establishes the foundation for the ALX Listing App. Future milestones will include:

1. **API Integration**: Connect to backend services for dynamic data
2. **User Authentication**: Add login and registration functionality  
3. **Property Details Page**: Create detailed property view pages
4. **Search and Filtering**: Implement property search and filter features
5. **Booking System**: Add reservation and booking capabilities
6. **User Dashboard**: Create user profile and booking management
7. **Payment Integration**: Add secure payment processing

## 🐛 Troubleshooting

### Common Issues

**Port 3000 is already in use:**
```bash
# Kill the process using port 3000
lsof -ti:3000 | xargs kill -9
# or use a different port
npm run dev -- -p 3001
```

**Module not found errors:**
```bash
# Clear npm cache and reinstall
npm cache clean --force
rm -rf node_modules package-lock.json
npm install
```

**TailwindCSS styles not working:**
- Ensure the file path is included in `tailwind.config.js` content array
- Check that `globals.css` properly imports Tailwind directives
- Restart the development server

## 📚 Learning Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [TailwindCSS Documentation](https://tailwindcss.com/docs)
- [React Documentation](https://react.dev/)

## 🤝 Contributing

This is a learning project. To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## 📄 License

This project is for educational purposes as part of the ALX Software Engineering program.

---

**Happy Coding! 🚀**

For questions or support, please refer to the project documentation or reach out to me via zealgabriels@gmail.com.
