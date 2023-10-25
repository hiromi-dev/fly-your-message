# 青い紙飛行機 app

- [デプロイ](https://vercel.com/making-oasis/amo-project)
- [本番 url](https://fly-your-message.making-oasis.com)

# セットアップ

各種ローカルで用意するもの。

- npm (v6.14.4)か yarn(v1.22.10)
- node(v14.1.0)

### Step 1. install

```
1, git clone
2, npm install
3, npm run dev
※ npm install -g npmしとくと良いかも。
```

で [http://localhost:3002](http://localhost:3002)から確認できます。

### Step 2. Set up environment variables

```bash
touch `.env.local`
```

Set each variable on `.env.local`:(RDS の環境変数は salck にて)

- `MYSQL_HOST` - Your MySQL host URL.
- `MYSQL_DATABASE` - The name of the MySQL database you want to use.
- `MYSQL_USERNAME` - The name of the MySQL user with access to database.
- `MYSQL_PASSWORD` - The passowrd of the MySQL user.
- `MYSQL_PORT` - xxxx

### Step 3. Run migration script

You'll need to run a migration to create the necessary table for the example.

```bash
npm run migrate
# or
yarn migrate
```

### Step 4. Run Next.js in development mode

```
ctrl + cでサーバーを一旦落として
```

```bash
npm install
npm run dev
# or
yarn install
yarn dev
```

Your app should be up and running on [http://localhost:3002](http://localhost:3002)!

# リリース

github に push することで自動的に vercel で preview 環境と production 環境が用意されます。
