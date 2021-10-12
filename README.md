# Vue2Heroku Example

## Vuejs Setup

- Create `static.json` file in vuejs app folder, in this example `frontend`

```json
{
    "root": "dist",
    "clean_urls": true,
    "routes": {
        "/**": "index.html"
    }
}
```
- Install [HerokuCLI](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)
- Open terminal in repo folder
- Run

```bash
heroku login
heroku create <app-name>
heroku buildpacks:set https://github.com/timanovsky/subdir-heroku-buildpack
heroku buildpacks:add heroku/nodejs
heroku buildpacks:add https://github.com/heroku/heroku-buildpack-static
heroku config:set PROJECT_PATH=frontend --app <app-name>
git push heroku main
```

- **It's recommended using heroku client to specify buildpacks**