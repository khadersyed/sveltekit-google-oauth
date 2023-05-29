# sveltekit-google-oauth

A test repository showing how you could potentially use SvelteKit deployed to S3 with Google OAuth for authentication. Not the only way or perhaps even the best way, but a way.

[Demo](https://tbd.khadersyed.com)

## Setup

### Pre-requisites
- Create [OAuth 2.0 credentials](https://support.google.com/cloud/answer/6158849?hl=en) for your application.
- Add an authorized redirect URI entry for `http://localhost:3000/auth/callback`.

### Local
- Copy `.env.sample` to `.env`
- Generate secrets for JWT and cookie signing.

```node
node -p "require('crypto').randomBytes(64).toString('hex');"
```

- Optionally set `AUTHORIZED_DOMAIN` to restrict authentication to only this domain.
- The other values can remain the same for local development.
- Install dependencies and run.

```
npm install
npm run dev
```

### S3

- Create your s3 bucket
- Rest is TBD

## Acknowledgements

Thanks to a few different articles and authors for inspiration and help.

- [Sveltekit Authentication](https://blog.hyper.io/sveltekit-authentication/)
- [Serverless OAuth with Multiple Providers](https://ryanbethel.org/serverless-o-auth-with-multiple-providers)
- [Creative Tim Tailwind Starter](https://www.creative-tim.com/learning-lab/tailwind-starter-kit/presentation)
- [Original code from Duffn](https://github.com/duffn/sveltekit-netlify-google-oauth-example)

## License

[MIT](https://opensource.org/licenses/MIT)
