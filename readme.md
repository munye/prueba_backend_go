# ![RealWorld Example App](logo.png)


[![Build Status](https://travis-ci.org/munye/prueba_backend_go.svg?branch=master)](https://travis-ci.org/munye/prueba_backend_go)
[![codecov](https://codecov.io/gh/munye/prueba_backend_go/branch/master/graph/badge.svg)](https://codecov.io/gh/munye/prueba_backend_go)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/munye/prueba_backend_go/blob/master/LICENSE)
[![GoDoc](https://godoc.org/github.com/munye/prueba_backend_go?status.svg)](https://godoc.org/github.com/munye/prueba_backend_go)

> ### Golang/Gin codebase containing real world examples (CRUD, auth, advanced patterns, etc) that adheres to the [RealWorld](https://github.com/gothinkster/realworld) spec and API.


This codebase was created to demonstrate a fully fledged fullstack application built with **Golang/Gin** including CRUD operations, authentication, routing, pagination, and more.


# How it works
```
.
├── gorm.db
├── hello.go
├── common
│   ├── utils.go        //small tools function
│   └── database.go     //DB connect manager
└── users
    ├── models.go       //data models define & DB operation
    ├── serializers.go  //response computing & format
    ├── routers.go      //business logic & router binding
    ├── middlewares.go  //put the before & after logic of handle request
    └── validators.go   //form/json checker
```

# Getting started

## Install the Golang
https://golang.org/doc/install
## Environment Config
make sure your ~/.*shrc have those varible:
```
➜  echo $GOPATH
/Users/zitwang/test/
➜  echo $GOROOT
/usr/local/go/
➜  echo $PATH
...:/usr/local/go/bin:/Users/zitwang/test//bin:/usr/local/go//bin
```
## Install Govendor & Fresh
I used Govendor manage the package, and Fresh can help build without reload

https://github.com/kardianos/govendor

https://github.com/pilu/fresh
```
cd 
go get -u github.com/kardianos/govendor
go get -u github.com/pilu/fresh
```

## Start
```
➜  govendor sync
➜  fresh
```

## Testing
```
➜  go test -v ./... -cover
```

## Todo
- More elegance config
- Test coverage (common & users 100%, article 0%)
- ProtoBuf support
- Code structure optimize (I think some place can use interface)
- Continuous integration (done)
