**JavaScript** library for generating **ImageProxy** urls **both on browser and server**.

# Installation

```bash
npm i -s @sholehmuhammad3/image-proxy-yubi
# or
yarn add @sholehmuhammad3/image-proxy-yubi
```

# Usage

```js
import ImgProxy from '@sholehmuhammad3/image-proxy-yubi';

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


# Methods
`@sholehmuhammad3/image-proxy-yubi` currently does not support all the **imgproxy** methods (it will do in the near future).

- `.image(<string>)`: The image to be resized
- `.width(<number>)`: Resize Width
- `.height(<number>)`: Resize height
- `.extension(<string>)`: The resized image extension
- `.gravity(<string>)`: The resize gravity
- `.enlarge(<number>`: Enlarge image
- `.resizeType(<string)`: The resize type

