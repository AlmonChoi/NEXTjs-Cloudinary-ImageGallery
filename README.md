# nextjs-cloudinary-imageGallery 
Demo of Next.JS Image Gallery Starter Template with image storage in Cloudinary

## Components

This example created from Vercel image gallery template using Next.js, [Cloudinary](https://cloudinary.com), and [Tailwind](https://tailwindcss.com).

![Home](./README.screen/Picture.jpg)

![Sample Image](./README.screen/sample_image.jpg)


## Create the Demo application

![Image_Gallery_Starter](./README.screen/Image_Gallery_Starter_template.jpg)

```bash
 npx create-next-app --example with-cloudinary nextjs-image-gallery
```

## Configuration Setup
- Get the API key (create free account, if needed)
![API key](./README.screen/API_key.jpg)

- Rename the .env.local.example to .env
'''
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
CLOUDINARY_FOLDER=
'''

## Fix Error: Invalid src prop on `next/image`, hostname "res.cloudinary.com" is not configured under images in your `next.config.js`

- Remark or remove 'port' and 'pathname' in next.config.js file
'''
// next.config.js
module.exports = {
  images: {
    formats: ["image/avif", "image/webp"],
    remotePatterns: [
      {
        protocol: "https",
        hostname: "res.cloudinary.com",
        //port: "",
        //pathname: "/my-account/**",
      },
    ],
  },
};
'''

## Deployment

- Complie and Run production code

'''
npm run build

npm run start
'''

- Access http://localhost:3000/ 
Home Page
![Home](./README.screen/Home.jpg)

Image zoom, download
![Home](./README.screen/Picture.jpg)


