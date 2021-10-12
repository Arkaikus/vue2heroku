# Vue2Heroku Example

## Repo Setup

- If vuejs app is in current folder then add engine and start commands

```json
{
    ...
    "engines": {
        "node": "14.x"
    },
    ...
    "scripts": {
        ...
        "start": "npm run serve",
        ...
    },
    ...
}
```
- If vuejs app is in some folder like frontend then run `npm init` to generate `package.json` and add


```json
{
    ...
    "engines": {
        "node": "14.x"
    },
    ...
    "scripts": {
        ...
        "start": "cd frontend && npm run serve",
        ...
    },
    ...
}
```

- Create `Procfile` and add `web: npm start`

## Herkou Setup

- Sign in to heroku
> ![](img/1.png)
- Create an app
> ![](img/2.png)
- Connect to github repo
> ![](img/3.png)
- Search repo and connect
> ![](img/4.png)
> ![](img/5.png)
- Enable automatic deploy
> ![](img/6.png)
- Or deploy manually
> ![](img/7.png)