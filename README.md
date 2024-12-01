# My starter for rails

Includes:

- Vite Ruby (configured with rails extension)
- Tailwind
- .erb, js and tailwind formatting in prettier

## Run the thing

You need to run both `bin/vite dev` and `rails s`, If you use a multiplexer like zeliij, just run them in a separate tab, it's all good.

## Notes

- Uses Yarn
- This currently does not work with Ruby LSP in VSCode, as it cannot target .erb files.
  Running this setup in Panic Nova, it works great and doesn't clash with solargraph/rubocop in my setup
- @4az/prettier-plugin-html-erb has some minor issues with .erb formatting at the moment.

## Troubleshooting

If you have issues with vite disconnecting, remove this line from vite.json:

```
"development": {
  "autoBuild": true,
  "host": "127.0.0.1", <------------ This guy.
  "publicOutputDir": "vite-dev",
  "port": 3036
},
```

More info can be found here https://vite-ruby.netlify.app/guide/troubleshooting.html
