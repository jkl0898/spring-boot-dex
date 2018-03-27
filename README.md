# spring-boot-dex
Spring Boot demo with Oauth authentication and Dex. 

# Setup
1. Install Golang: https://golang.org/doc/install
2. Install Dex:

```
go get github.com/coreos/dex
cd $GOPATH/src/github.com/coreos/dex
make
```

3. Clone this repo:

```
git clone https://github.com/wearearima/spring-boot-dex.git
```

4. Copy the dex configuration file for this spring-boot demo application

```
cp spring-boot-demo.yaml $GOPATH/src/github.com/coreos/dex/examples
```

# Run
5. Run dex:

```
cd $GOPATH/src/github.com/coreos/dex
./bin/dex serve examples/spring-boot-demo.yaml
```

6. Run Spring Boot demo application
```
mvn spring-boot:run
```

7. Go to http://localhost:8080/

Credentials to authenticate in Dex: admin@example.com / password
