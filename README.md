# About my-gluestack-app

> **Note:** This repository contains my-gluestack-app built using the gluestack framework.

# Installation

```shell
npx create-gluestack-app@latest my-gluestack-app
```

```shell
cd my-gluestack-app
node glue
```

```Usage: glue [options] [command]

gluestack framework

Options:
  -V, --version                              output the version number
  -h, --help                                 display help for command

Commands:
  plugin-list                                Prints the list of available plugins
  plugin-init                                Initializes the gluestack app as a plugin
  publish                                    Publishes the gluestack app as a plugin
  plugin-version                             Prints the current version of the plugin
  instance-list                              Prints the list of installed plugin instances
  add|install <plugin-name> <instance-name>  installs a gluestack plugin, use help for more info on subcommands
  develop:list                               Lists all the container instances
  develop:up [instance-name]                 Starts provided container instances or all the containers if no instance is provided
  develop:down [instance-name]               Stops provided container instances or all the containers if no instance is provided
  build [instance-name]                      Builds provided container instances or all the containers if no instance is provided
  route:list                                 Prints a table of entries of the registered routes
  route:generate                             Generates nginx config from registered routes
  postgres                                   Postgres instance commands
  help [command]                             display help for command
```

# Commands used to built this app

```shell
node glue add web website
```

```shell
node glue develop:up website
```

```shell
node glue add postgres postgres-hasura
```

```shell
node glue add graphql hasura
```

```shell
node glue add hasura-console hasura-console
```

### Go to console and connect to postgres database before continuing

```shell
node glue add minio minio
```

### Go to console and change public bucket privacy to `public` before continuing

```shell
node glue add storage storage
```

```shell
node glue add auth auth
```

```shell
node glue add functions f1
```

```shell
node glue add functions f2
```

### We can see the installed plugins

```shell
node glue develop:list
```

### We can edit routes.json & set routes

```shell
node glue route:list
```

## Available Routes 

> **Note:** Ports might differ as per availability

1. Next App: [website](http://localhost:3103) (exposed port `3103`)
2. Graphql: [hasura](http://localhost:10880/v1/graphql) (exposed port `10880`)
3. Signin: [auth](http://localhost:6670/authentication/signin) (exposed port `6670`)
4. Signup: [auth](http://localhost:6670/authentication/signup) (exposed port `6670`)
5. S3 Storage: [storage](http://localhost:7650/upload) (exposed port `7650`)
6. Express App: [f1](http://localhost:4506/users) (exposed port `4506`)
7. Express App: [f2](http://localhost:4507/users) (exposed port `4507`)
