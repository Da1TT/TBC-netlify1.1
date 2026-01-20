# Tour & Business in China - Deployment Guide

## Netlify Deployment Steps

1. Create a Netlify account at [https://www.netlify.com/](https://www.netlify.com/)
2. Connect your GitHub repository to Netlify
3. Configure deployment settings:
   - Build command: `npm ci --legacy-peer-deps && npm run build`
   - Publish directory: `dist`
   - Environment variables:
     - NODE_ENV: production
     - NODE_VERSION: 20
     - NPM_CONFIG_PRODUCTION: false

4. Click "Deploy site" and wait for the deployment to complete

## Key Fixes for Netlify Deployment Issues

1. **Dependency Version Mismatch**: Updated `vite-tsconfig-paths` in package.json to match the version in pnpm-lock.yaml (^5.1.4)

2. **Package Manager Configuration**: Configured Netlify to use npm instead of pnpm to avoid lockfile synchronization issues

3. **Development Dependencies**: Set `NPM_CONFIG_PRODUCTION=false` to ensure development dependencies are installed even in production environment

## Troubleshooting

If you encounter issues during deployment:

1. Check the Netlify deploy logs for specific error messages
2. Ensure all dependencies are properly listed in package.json
3. Verify that the build command correctly generates the `dist` directory
4. Confirm that the repository has the necessary configuration files (netlify.toml)