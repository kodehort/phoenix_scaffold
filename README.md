# Code generation for Phoenix

In this repo I have built a Phoenix application that matches the functionality of the [Rails 5 video](https://www.youtube.com/watch?v=Gzj723LkRJY&feature=youtu.be)

## Steps

### Create project

```bash
mix phx.new demo
```

```bash
* creating demo/config/config.exs
* creating demo/config/dev.exs
* creating demo/config/prod.exs
* creating demo/config/prod.secret.exs
* creating demo/config/test.exs
* creating demo/lib/demo/application.ex
* creating demo/lib/demo.ex

...

Fetch and install dependencies? [Yn]
* running mix deps.get
* running mix deps.compile
* running cd assets && npm install && node node_modules/webpack/bin/webpack.js --mode development

We are almost there! The following steps are missing:

    $ cd demo

Then configure your database in config/dev.exs and run:

    $ mix ecto.create

Start your Phoenix app with:

    $ mix phx.server

You can also run your app inside IEx (Interactive Elixir) as:

    $ iex -S mix phx.server
```

### Create database

```bash
cd demo
mix ecto.create
```

```bash
The database for Demo.Repo has been created
```

### Start application

```bash
mix phx.server
```

```bash
[info] Running DemoWeb.Endpoint with cowboy 2.7.0 at 0.0.0.0:4000 (http)
[info] Access DemoWeb.Endpoint at http://localhost:4000

webpack is watching the files…

Hash: 8d20b4ef859436fc514b
Version: webpack 4.41.5
Time: 1617ms
Built at: 04/09/2020 9:35:34 AM
                Asset       Size       Chunks             Chunk Names
       ../css/app.css   10.6 KiB  ./js/app.js  [emitted]  ./js/app.js
       ../favicon.ico   1.23 KiB               [emitted]
../images/phoenix.png   13.6 KiB               [emitted]
        ../robots.txt  202 bytes               [emitted]
               app.js   8.23 KiB  ./js/app.js  [emitted]  ./js/app.js
Entrypoint ./js/app.js = ../css/app.css app.js
[0] multi ./js/app.js 28 bytes {./js/app.js} [built]
[../deps/phoenix_html/priv/static/phoenix_html.js] 2.21 KiB {./js/app.js} [built]
[./css/app.css] 39 bytes {./js/app.js} [built]
[./js/app.js] 493 bytes {./js/app.js} [built]
    + 2 hidden modules
Child mini-css-extract-plugin node_modules/css-loader/dist/cjs.js!css/app.css:
    Entrypoint mini-css-extract-plugin = *
    [./node_modules/css-loader/dist/cjs.js!./css/app.css] 436 bytes {mini-css-extract-plugin} [built]
    [./node_modules/css-loader/dist/cjs.js!./css/phoenix.css] 10.9 KiB {mini-css-extract-plugin} [built]
        + 1 hidden module
[debug] Duplicate channel join for topic "phoenix:live_reload" in Phoenix.LiveReloader.Socket. Closing existing channel for new join.
```
