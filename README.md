# Dine Strapi Provider Upload AWS S3

## Install

```
npm install dine-strapi-provider-upload-aws-s3
```

```
yarn add dine-strapi-provider-upload-aws-s3
```

```
pnpm add dine-strapi-provider-upload-aws-s3
```

## Configuration

`config/plugins.js`

```js
module.exports = ({ env }) => ({
  upload: {
    config: {
      provider: 'dine-strapi-provider-upload-aws-s3',
      providerOptions: {
        baseUrl: 'https://foo.bar.com',
        accessKeyId: env('AWS_ACCESS_KEY_ID'),
        secretAccessKey: env('AWS_ACCESS_SECRET'),
        endpoint: env('AWS_ENDPOINT'),
        params: {
          Bucket: env('AWS_BUCKET'),
        },
      },
    },
  },
})
```
