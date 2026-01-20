# Tour & Business in China - Deployment Guide

## Netlify Deployment Steps

### Prerequisites
- A Netlify account
- A GitHub repository containing your project code

### Deployment Process

1. **Connect your repository to Netlify**
   - Go to [Netlify](https://app.netlify.com/) and sign in
   - Click on "New site from Git"
   - Select "GitHub" and authorize Netlify to access your repository
   - Choose the repository containing your project code

2. **Automatic Configuration**
   - The project includes a `netlify.toml` file that will automatically configure:
     - Build command: `npm ci --legacy-peer-deps && npm run build`
     - Publish directory: `dist`
     - Environment variables: NODE_VERSION=20

3. **Deploy your site**
   - Click on "Deploy site" to start the deployment process
   - Wait for Netlify to build and deploy your site
   - Once deployment is complete, you'll receive a unique URL for your site

## Project Overview

Tour & Business in China is a professional ground services provider dedicated to helping international visitors make the most of their time in China. The website offers information about:

- Guided tours to historical and cultural sites
- Exhibition support services for IT and technology events
- Custom travel itineraries
- Accommodation arrangements

The site features a responsive design, multi-language support (English and Chinese), and a user-friendly interface to help visitors plan their trip to China.

## Project Structure
```
├── src/                  # Source code directory
│   ├── components/       # Reusable UI components
│   ├── contexts/         # React context providers
│   ├── hooks/            # Custom React hooks
│   ├── lib/              # Utility functions and libraries
│   ├── pages/            # Page components
│   ├── App.tsx           # Main application component
│   ├── index.css         # Global styles
│   ├── main.tsx          # Entry point
├── netlify.toml          # Netlify configuration
├── package.json          # Project dependencies and scripts
└── README.md             # Project documentation
```

Professional ground services for international visitors to China. Offering tour guides, exhibition support, and customized travel solutions across major cities.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Development](#development)
- [Deployment](#deployment)
  - [Netlify Deployment Steps](#netlify-deployment-steps)

## Project Overview

This is a React application built with TypeScript and Tailwind CSS, designed to showcase the services offered by Tour & Business in China. The application provides information about tours, exhibition support, and contact details.

## Features

- Responsive design for both desktop and mobile devices
- Multilingual support (English and Chinese)
- Animated UI components using Framer Motion
- Interactive elements including navigation, consultation button, and more
- Tour and exhibition information display

## Installation

1. Clone the repository
   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory
   ```bash
   cd tour-business-in-china
   ```

3. Install dependencies
   ```bash
   npm install
   ```
   
   or if using pnpm:
   ```bash
   pnpm install
   ```

## Development

To start the development server:

```bash
npm run dev
```

The application will be available at `http://localhost:5173`

## Deployment

### Netlify Deployment Steps

1. **Prepare Your Project**
   - Ensure you have a `netlify.toml` file in the root directory (already included in this project)
   - Make sure your build command is correctly set in `package.json`

2. **Create a Netlify Account**
   - Go to [Netlify](https://www.netlify.com/) and sign up for a free account

3. **Connect Your GitHub Repository**
   - Click on "Add new site"
   - Select "Import an existing project"
   - Connect to GitHub and authorize Netlify
   - Select the repository for your project

4. **Configure Build Settings**
   - Netlify should automatically detect your build settings from the `netlify.toml` file
   - Build command: `npm run build`
   - Publish directory: `dist`
   - Click "Deploy site"

5. **Wait for Deployment**
   - Netlify will start building and deploying your site
   - You can monitor the progress in the deployment logs

6. **Access Your Site**
   - Once deployment is complete, you'll be provided with a Netlify subdomain (e.g., your-site-name.netlify.app)
   - You can visit your site using this URL
   
7. **Custom Domain Setup (Optional)**
   - Go to "Domain settings" in your Netlify dashboard
   - Click "Add custom domain" and follow the instructions to connect your own domain

8. **Continuous Deployment**
   - Netlify will automatically deploy new changes whenever you push to your connected GitHub repository branch