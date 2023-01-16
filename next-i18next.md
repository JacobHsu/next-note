# [next-i18next](https://www.npmjs.com/package/next-i18next)

next.config.js
```js
const { i18n } = require('./next-i18next.config')

module.exports = {
  i18n,
}
```

next-i18next.config
```js
module.exports = {
  i18n: {
    defaultLocale: 'en',
    locales: ['en', 'de'],
  },
}
```

_app
```
import { appWithTranslation } from 'next-i18next'

const MyApp = ({ Component, pageProps }) => (
  <Component {...pageProps} />
)

export default appWithTranslation(MyApp)
```

index.tsx

```js
export const getStaticProps = async ({ locale }: { locale: string }) => ({
  props: {
    ...(await serverSideTranslations(locale, ['common', 'footer'])),
  },
})
```
