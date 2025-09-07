# Yarn Calculator Application

## Overview

This is a full-stack web application for calculating yarn cost-effectiveness. The application allows users to input yarn details (name, price, yardage) and automatically calculates the cost per yard to help compare different yarn options. It features a modern React frontend with shadcn/ui components and an Express.js backend with PostgreSQL database integration using Drizzle ORM.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized production builds
- **Routing**: Wouter for lightweight client-side routing
- **UI Framework**: shadcn/ui components built on top of Radix UI primitives
- **Styling**: Tailwind CSS with CSS custom properties for theming
- **State Management**: TanStack Query (React Query) for server state management
- **Form Handling**: React Hook Form with Zod validation for type-safe form schemas

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database ORM**: Drizzle ORM for type-safe database operations
- **Validation**: Zod schemas shared between frontend and backend
- **Session Management**: express-session with connect-pg-simple for PostgreSQL session store
- **Development**: tsx for TypeScript execution and hot reloading

### Database Design
- **Database**: PostgreSQL with Neon serverless driver
- **Schema Management**: Drizzle Kit for migrations and schema management
- **Tables**: 
  - `yarn_entries`: Stores yarn information (id, name, price, yardage) with UUID primary keys and decimal precision for monetary values
- **Validation**: Zod schemas ensure data integrity with proper constraints (positive numbers, string length limits)

### Data Storage Strategy
- **Production**: PostgreSQL database with Drizzle ORM for production data persistence
- **Development**: In-memory storage implementation for rapid development and testing
- **Flexibility**: Storage interface pattern allows easy switching between storage backends

### Build and Deployment
- **Development Mode**: Vite dev server with Express backend, hot module replacement enabled
- **Production Build**: 
  - Frontend: Vite builds optimized static assets
  - Backend: esbuild bundles server code with external dependencies
- **Deployment Structure**: Static frontend served by Express with API routes under `/api` prefix

### Development Features
- **Hot Reloading**: Full-stack development with automatic reloading
- **Error Handling**: Runtime error overlay in development mode
- **Code Quality**: TypeScript strict mode with comprehensive path aliases
- **Replit Integration**: Custom plugins for Replit development environment

## External Dependencies

### Core Frontend Libraries
- **React Ecosystem**: React 18, React DOM, React Hook Form for component architecture and form management
- **UI Components**: Comprehensive shadcn/ui component library with Radix UI primitives for accessible components
- **Styling**: Tailwind CSS with PostCSS, Autoprefixer, and class-variance-authority for component variants
- **State Management**: TanStack React Query for efficient server state synchronization
- **Utilities**: clsx and tailwind-merge for conditional styling, date-fns for date manipulation

### Backend Dependencies
- **Server Framework**: Express.js with TypeScript support
- **Database**: Neon Database serverless PostgreSQL driver, Drizzle ORM for database operations
- **Session Management**: express-session with connect-pg-simple PostgreSQL session store
- **Validation**: Zod for runtime type validation and drizzle-zod for schema integration
- **Utilities**: nanoid for unique ID generation, crypto module for UUID generation

### Development Tools
- **Build Tools**: Vite with React plugin, esbuild for backend bundling
- **TypeScript**: Full TypeScript configuration with strict mode and comprehensive type checking
- **Database Tooling**: Drizzle Kit for database migrations and schema management
- **Development Experience**: tsx for TypeScript execution, custom Vite plugins for error handling and development features

### Database Service
- **Neon Database**: Serverless PostgreSQL database with connection pooling and automatic scaling
- **Connection**: Environment variable-based database URL configuration
- **Migration Strategy**: Drizzle Kit manages database schema changes and migrations