Docker images:

**mysql**:
* Build:
`docker build -t my-mysql .`
* Run:

```
docker run -it -d -p 3306:3306 --name my-mysql \
-v ${PWD}/test/component/data:/docker-entrypoint-initdb.d/ \
-e MYSQL_ROOT_PASSWORD=supersecret \
-e MYSQL_DATABASE=fjviera \
mysql
```

Alpine:

Built to mount a binary and run it.
* Build `docker build -t alpine .`
* Run `docker run -it -p 1323:1323 -v $PWD:/app alpine /app/command`
  