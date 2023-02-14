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
## Vercel Deployment

Here is the settings for the vercel deployment

![image](https://user-images.githubusercontent.com/1437205/218611025-4509b593-26bb-440a-90f6-6cf23d083b16.png)

![image](https://user-images.githubusercontent.com/1437205/218611205-dac4d2ed-2102-4214-94ca-01705ebf5acc.png)

![image](https://user-images.githubusercontent.com/1437205/218611276-530d7a8f-86ea-4276-a7df-db6635919df3.png)

Here are the screenshots after deployment

## Vercel Fix

Here I tried to fix the issue by changing some settings and then redeployed the project.

![image](https://user-images.githubusercontent.com/1437205/218611589-cf2d54dd-5da5-4c76-9750-04ab872eed1e.png)

After deployment, I can now see my website but it is not SSR.

![image](https://user-images.githubusercontent.com/1437205/218612038-d0f7c80c-3ea3-46c3-a81a-b1edb09553be.png)

So I tried again by changing the settings once more.

![image](https://user-images.githubusercontent.com/1437205/218612160-e1b813f6-9752-4502-9092-3b8d8098fccb.png)

Then I got these results:

![image](https://user-images.githubusercontent.com/1437205/218612471-bf4f2785-cd99-4e5d-8861-b49d48e90675.png)

![image](https://user-images.githubusercontent.com/1437205/218612585-e3eede62-7b49-49ac-b14d-33c0f9ab777f.png)

