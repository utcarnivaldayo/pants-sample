# pants-sample

## docker image build

- キャッシュを利用しない場合は、下記コマンドに`--docker-build-no-cache`を追加

### example-nest-project

- build full dev-image

```sh
pants --tag='example-nest-project' --tag='dev-image' package ::
```

- build only dev-common-image

```sh
pants --tag='example-nest-project' --tag='dev-common-image' package ::
```

- build only dev-frontend-image

```sh
pants --tag='example-nest-project' --tag='dev-frontend-image' package ::
```

- build only dev-backend-image

```sh
pants --tag='example-nest-project' --tag='dev-backend-image' package ::
```

### example-rust-project

- build full dev-image

```sh
pants --tag='example-rust-project' --tag='dev-image' package ::
```

- build only dev-common-image

```sh
pants --tag='example-rust-project' --tag='dev-common-image' package ::
```

- build only dev-frontend-image

```sh
pants --tag='example-rust-project' --tag='dev-frontend-image' package ::
```

- build only dev-backend-image

```sh
pants --tag='example-rust-project' --tag='dev-backend-image' package ::
```
