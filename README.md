[![Build Status](https://travis-ci.org/Wei-1/Scala-gRPC-HelloWorld.svg?branch=master)](https://travis-ci.org/Wei-1/Scala-gRPC-HelloWorld)

[![License](https://img.shields.io/:license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

# Scala-gRPC-HelloWorld

A scala version of the official HelloWorld GRPC example.

## Context

This repo is another example to use the [`sbt-protoc`](https://github.com/thesamet/sbt-protoc) plugin and implements gRPC services using [`scalaPB`](https://github.com/scalapb/ScalaPB).

The `HelloWorld` example is taken from [grpc-java](https://github.com/grpc/grpc-java) examples.

## How to use?

First, run

```
sbt compile
```

to create the case class GreeterGrpc.

Second, run

```
sbt "runMain io.grpc.helloworld.HelloWorldServer"
```

to start the HelloWorldServer.

Third, run

```
sbt "runMain io.grpc.helloworld.HelloWorldClient"
```

to start a client that will send a `world` to HelloWorldServer.

The server will reply with a `Hello world`.

## Why this repo?

After checking the [official repo of Scalapb with gRPC done by xuwei-k](https://github.com/xuwei-k/grpc-scala-sample),

I found that xuwei-k's example cannot be built alone and will need to have the [official Java repo](https://github.com/grpc/grpc-java) with it.

Also, his/her example doesn't follow the original build path `src`, which will cause some problems in my environment.

Therefore, I search for a simpler solution and found the [gRPC example from btlines](https://github.com/btlines/grpcexample).

btlines's example is very well written and support several different connection methods with easy and reliable control.

The only problem to me is that btlines's example uses a lot of his/her own dependencies to support the abundant connection methods.

For an example, I am looking for an easier approach.

By combining all these repositories, I created this repo for a basic Hello World example that you can just `compile` and `run`.

## Reference

 - [grpc/grpc-java](https://github.com/grpc/grpc-java)

 - [xuwei-k/grpc-scala-sample](https://github.com/xuwei-k/grpc-scala-sample)

 - [btlines/grpcexample](https://github.com/btlines/grpcexample)
