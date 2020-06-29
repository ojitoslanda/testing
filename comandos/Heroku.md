https://devcenter.heroku.com/articles/heroku-cli#download-and-install


Ubuntu / Debian apt-get
```
curl https://cli-assets.heroku.com/install-ubuntu.sh | sh
```

Version
```
heroku -v         #heroku/7.42.1 linux-x64 node-v12.16.2
```

Configurar package.json
```
 "scripts": {
    "start": "node server.js",
    "nodemon": "nodemon server.js",
  },
```

```
git init
git add .
git commit -m "mensaje"

https://dashboard.heroku.com/apps/node-webpage-starter/deploy/heroku-git

heroku login                                # Solo unica vez escribir eso
heroku git:remote -a nombredelproyecto     # set git remote heroku to https://git.heroku.com/node-webpage-starter.git    
git push heroku master

#El resultando final
heroku open
https://node-webpage-starter.herokuapp.com/ deployed to Heroku
```
