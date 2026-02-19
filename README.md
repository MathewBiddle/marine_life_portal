This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

Documentation resources:
* https://www.portaljs.com/opensource/developers/comprehensive-guide-building-robust-data-portal-ckan
* https://github.com/datopian/portaljs/tree/main/examples/ckan

## Getting Started

### Install Node.js

1. Download the Node.js binaries: Go to the official [Node.js Downloads page](https://nodejs.org/en/download) and select the **"Windows Binary (.zip)"** file corresponding to your system architecture (32-bit or 64-bit).
1. Extract the files:
   1. Create a new folder in a location where you have write access (e.g., `C:\Users\YourUsername\nodejs`).
   2. Extract the contents of the downloaded zip file into this new folder.
1. Add the folder to your User Environment Variables:
   1. Open the "Run" dialog by pressing `Win` + `R`.
   1. Type `rundll32 sysdm.cpl,EditEnvironmentVariables` and press Enter. This opens the **Environment Variables** dialog directly, even if standard access is limited.
   1. Under the "User variables for [YourUsername]" section (not the "System variables" section which requires admin rights), find the `Path` variable and click **Edit**. If it doesn't exist, click **New**.
   1. Add the full path to your new Node.js folder (e.g., C:\Users\YourUsername\nodejs) to the list of paths.
1. Verify the installation:
   1. Close and reopen any open Command Prompt windows to refresh the environment variables.
   1. In a new command prompt, type `node -v` and press Enter.
   1. Type `npm -v` and press Enter.
   1. Both commands should return the installed Node.js and npm versions, confirming a successful setup without admin right

### Create PortalJS application from example
This process creates all of the files in this repository. No need to run this again. Sharing for reproducibility sake.
```bash
npx create-next-app marine_life_portal --example https://github.com/datopian/datahub/tree/main/examples/ckan
cd marine_life_portal
```

#### Point to the CKAN instance:
This file is already in this repository. Again, just sharing this for reproducibility.

This project uses CKAN as a backend, so you need to point it to the desired CKAN instance URL. You can do so by setting up the `DMS` environment variable in your terminal or creating an `.env` file with the following content:
```bash
DMS=https://data.ioos.us/
```

#### Run the development app:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.tsx`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.ts`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!
