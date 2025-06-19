# REST Express Application

## Overview

This is a full-stack web application built with React and Express.js, featuring a modern UI component library (shadcn/ui), database integration with Drizzle ORM, and PostgreSQL. The application follows a monorepo structure with separate client and server directories, sharing common schemas and types.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for client-side routing
- **State Management**: TanStack Query for server state management
- **UI Components**: shadcn/ui component library with Radix UI primitives
- **Styling**: Tailwind CSS with custom design tokens
- **Build Tool**: Vite for development and production builds

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **Runtime**: Node.js 20
- **Database ORM**: Drizzle ORM for type-safe database operations
- **Session Storage**: PostgreSQL-based session storage with connect-pg-simple
- **API Structure**: RESTful API with `/api` prefix

### Data Storage
- **Primary Database**: PostgreSQL 16
- **ORM**: Drizzle ORM with TypeScript integration
- **Schema Management**: Shared schema definitions in `/shared` directory
- **Migrations**: Drizzle Kit for database migrations
- **Development Storage**: In-memory storage implementation for development

## Key Components

### Database Schema
- **Users Table**: Basic user management with username/password authentication
- **Schema Validation**: Zod integration for runtime type checking
- **Type Safety**: Full TypeScript integration with inferred types

### Storage Layer
- **Interface-based Design**: `IStorage` interface for flexible storage implementations
- **Memory Storage**: Development implementation for rapid prototyping
- **PostgreSQL Integration**: Production-ready database storage (configured but not implemented)

### UI System
- **Design System**: Custom design tokens defined in CSS variables
- **Component Library**: Comprehensive set of UI components from shadcn/ui
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Accessibility**: Built-in accessibility features from Radix UI

### Development Tools
- **Hot Reload**: Vite HMR for fast development iteration
- **Error Handling**: Runtime error overlay for development
- **Code Quality**: TypeScript strict mode with comprehensive type checking

## Data Flow

1. **Client Requests**: React components make API calls using TanStack Query
2. **API Processing**: Express.js routes handle requests with proper error handling
3. **Data Access**: Storage interface abstracts database operations
4. **Response Handling**: Structured JSON responses with error states
5. **State Updates**: TanStack Query manages cache invalidation and updates

## External Dependencies

### Core Libraries
- **@neondatabase/serverless**: Neon database driver for PostgreSQL
- **drizzle-orm**: Type-safe ORM for database operations
- **@tanstack/react-query**: Server state management
- **@radix-ui/***: Accessible UI primitives
- **tailwindcss**: Utility-first CSS framework

### Development Tools
- **vite**: Build tool and development server
- **typescript**: Type checking and compilation
- **drizzle-kit**: Database migration tool
- **esbuild**: Production build bundling

## Deployment Strategy

### Development Environment
- **Local Development**: Vite dev server with Express.js backend
- **Hot Reload**: Full-stack hot reload for rapid development
- **Database**: PostgreSQL 16 instance

### Production Build
- **Client Build**: Vite production build with optimizations
- **Server Build**: esbuild bundle for Node.js deployment
- **Static Assets**: Client build served from Express.js
- **Environment**: Node.js production environment

### Replit Configuration
- **Autoscale Deployment**: Configured for Replit's autoscale platform
- **Port Configuration**: External port 80 mapping to internal port 5000
- **Module Dependencies**: Node.js 20, web, and PostgreSQL 16 modules

## User Preferences

Preferred communication style: Simple, everyday language.

## Changelog

Changelog:
- June 19, 2025. Initial setup