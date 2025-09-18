# Grokit - Build Documentation

## Project Overview

Grokit is a smart meal planning and shopping application built with React, TypeScript, and Supabase. It helps users save money, eat healthier, and reduce food waste through intelligent meal planning and smart shopping lists.

## Prerequisites

Before building this project, ensure you have the following installed:

- **Node.js** (v18 or higher) - [Download](https://nodejs.org/)
- **npm** (comes with Node.js) or **yarn**
- **Git** - [Download](https://git-scm.com/)

## Quick Start

### 1. Clone the Repository

```bash
git clone <YOUR_GIT_URL>
cd grokit
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Setup

Create a `.env.local` file in the root directory with your Supabase credentials:

```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

### 4. Start Development Server

```bash
npm run dev
```

The application will be available at `http://localhost:8080`

## Build Process

### Development Build

```bash
npm run dev
```

Starts the development server with:
- Hot module replacement (HMR)
- Fast refresh
- TypeScript compilation
- Tailwind CSS processing

### Production Build

```bash
npm run build
```

Creates an optimized production build in the `dist/` directory with:
- Minified JavaScript and CSS
- Tree-shaking for smaller bundle size
- Static asset optimization
- Source maps (optional)

### Preview Production Build

```bash
npm run preview
```

Serves the production build locally for testing.

## Project Structure

```
grokit/
├── public/                 # Static assets
├── src/
│   ├── components/        # React components
│   │   ├── main/         # Main application screens
│   │   ├── onboarding/   # User onboarding flow
│   │   ├── ui/           # Reusable UI components (shadcn/ui)
│   │   └── web/          # Web-specific components
│   ├── hooks/            # Custom React hooks
│   ├── lib/              # Utility libraries
│   ├── pages/            # Route components
│   ├── assets/           # Images and media
│   ├── App.tsx           # Main application component
│   ├── main.tsx          # Application entry point
│   └── index.css         # Global styles and design tokens
├── tailwind.config.ts    # Tailwind CSS configuration
├── vite.config.ts        # Vite bundler configuration
└── package.json          # Project dependencies and scripts
```

## Technology Stack

### Core Technologies
- **React 18** - User interface library
- **TypeScript** - Type-safe JavaScript
- **Vite** - Fast build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework

### UI Components
- **shadcn/ui** - High-quality React components
- **Radix UI** - Unstyled, accessible UI primitives
- **Lucide React** - Beautiful SVG icons

### Backend & Data
- **Supabase** - Backend-as-a-Service
- **@supabase/supabase-js** - Supabase client library
- **@tanstack/react-query** - Data fetching and caching

### Additional Libraries
- **React Router DOM** - Client-side routing
- **React Hook Form** - Form handling
- **Zod** - Schema validation
- **date-fns** - Date manipulation
- **Recharts** - Data visualization

## Development Workflow

### 1. Feature Development

1. Create a new branch: `git checkout -b feature/your-feature-name`
2. Make your changes
3. Test locally: `npm run dev`
4. Build and test: `npm run build && npm run preview`
5. Commit changes: `git commit -m "feat: description"`
6. Push and create pull request

### 2. Code Quality

The project uses:
- **ESLint** - Code linting
- **TypeScript** - Type checking
- **Prettier** (recommended) - Code formatting

Run linting:
```bash
npm run lint
```

### 3. Component Development

- Use TypeScript for all components
- Follow the established component structure in `src/components/`
- Utilize the design system tokens from `index.css`
- Create reusable components in `src/components/ui/`

## Deployment

### Lovable Platform (Recommended)

1. Open your [Lovable Project](https://lovable.dev/projects/f5571d1c-6186-475e-b9ac-2e6beb343964)
2. Click **Share** → **Publish**
3. Your app will be deployed automatically

### Manual Deployment

1. Build the project: `npm run build`
2. Deploy the `dist/` folder to your hosting platform:
   - **Vercel**: `vercel --prod`
   - **Netlify**: Drag and drop `dist/` folder
   - **GitHub Pages**: Configure GitHub Actions

## Environment Variables

### Required Variables

```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

### Optional Variables

```env
VITE_APP_TITLE=Grokit
VITE_APP_DESCRIPTION=Smart Meal Planning & Shopping
```

## Troubleshooting

### Common Issues

**Node.js Version Error**
```bash
# Use Node Version Manager (nvm)
nvm install 18
nvm use 18
```

**Dependency Issues**
```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
```

**Build Errors**
```bash
# Type checking
npx tsc --noEmit

# ESLint checking
npm run lint
```

**Supabase Connection Issues**
- Verify your Supabase URL and keys in `.env.local`
- Check Supabase project status
- Ensure RLS policies are configured correctly

### Performance Optimization

**Bundle Analysis**
```bash
npm run build -- --analyze
```

**Image Optimization**
- Use WebP format when possible
- Implement lazy loading for images
- Optimize image sizes for different screen densities

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## Support

- **Lovable Documentation**: [https://docs.lovable.dev/](https://docs.lovable.dev/)
- **Supabase Docs**: [https://supabase.io/docs](https://supabase.io/docs)
- **React Documentation**: [https://react.dev/](https://react.dev/)

## License

This project is built with Lovable. Please refer to your project's license terms.

---

**Last Updated**: September 2024  
**Build Version**: 1.0.0