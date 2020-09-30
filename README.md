**JavaScript** library for generating **ImageProxy** urls **both on browser and server**.

# Installation

```bash
npm i -s image-proxy-yubi
# or
yarn add image-proxy-yubi
```

# Usage

```js
import ImgProxy from 'image-proxy-yubi';

const proxy = new ImgProxy({ 
  key:  process.env.IMGPROXY_KEY, 
  salt: process.env.IMGPROXY_SALT, 
  url:  process.env.IMGPROXY_URL
});

const myResizedImage = proxy
                        .image('https://example.com/img.jpg')
                        .width(500)
                        .height(0)
                        .extension('png')

console.log(myResizedImage.get()); // => "Image URL Result"

