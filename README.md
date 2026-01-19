# Tour & Business in China

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