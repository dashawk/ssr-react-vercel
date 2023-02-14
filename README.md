# ReactJS SSR for Vercel

## On Local Development
1. Using the command:
  ```bash
  yarn dev
  ```

It results to this screenshot
![image](https://user-images.githubusercontent.com/1437205/218609850-83bf56d4-dee1-4b9d-a1e8-e4f5263d05ad.png)

2. Using the build command:
  ```bash
  yarn build
  ```
  Will result to have a `dist` folder
  ![image](https://user-images.githubusercontent.com/1437205/218610343-451e7bb8-5f40-47f9-9a8e-a109870255f5.png)
  The package.json scripts:
   ```json
   "scripts": {
    "dev": "node server",
    "build": "npm run build:client && npm run build:server",
    "build:client": "vite build --ssrManifest --outDir dist/client",
    "build:server": "vite build --ssr src/entry-server.jsx --outDir dist/server",
    "preview": "cross-env NODE_ENV=production node server"
  }
   ```

