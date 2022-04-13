# Read:39 - React III - 04/12/2022

```javascript
// Links
import Link from 'next/link'

<Link href="/">
  <a>Home</a>
</Link>

// Assets
import Image from 'next/image'

<Image
  src="/images/hello.jpg"
  height={100}
  width={100}
  alt="hello"
/>

// Metadata
import Head from 'next/head'
import Script from 'next/script'

<Head>
  <title>Hello World</title>
  <link rel="icon" href="/favicon.ico" />
</Head>
<Script
  src="someCDN"
  strategy="lazyOnLoad"
  onLoad={callback_function}
/>

// install tailwindcss
// npm i -D tailwindcss autoprefixer postcss

// create a postcss.config.js
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {}
  }
}

// tailwind.config.js
module.exports = {
  content: [
    './pages/**/*.{js,ts,jsx,tsx}',
    './components/**/*.{js,ts,jsx,tsx}'
  ]
}
```
