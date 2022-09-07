reference：https://www.udemy.com/course/aidocker/learn/lecture/20295327#overview Section10

## build

`docker build --platform linux/amd64 .`
※ m1 の場合は `--platform linux/amd64` をつけないと失敗する

## run

```docker
docker run -p port_of_host:8888 -v ~/dir_of_hosts:/dir_of_container --rm docker_image
```

example

```docker
docker run -p 8080:8888 -v ~/Documents/xxx/:/yyyy --rm  0dda6a42e52b
```

## access to localhost

```
localhost:port_of_host
```

example

```
localhost:8080
```
