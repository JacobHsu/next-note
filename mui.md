[unexpected behavior when using Tailwind, and MUI in NextJS Project (White Button error)](https://stackoverflow.com/questions/70536210/unexpected-behavior-when-using-tailwind-and-mui-in-nextjs-project-white-button)

```tailwind.config.js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{js,jsx,ts,tsx}",],
  important: '#root',
  theme: {
    extend: {},
  },
  plugins: [],
  corePlugins: {
    preflight: false,
  },
}
```
