# vcluster

Script to manage a local, docker-based, Apache Spark cluster.

## Requirements

- A copy of Spark's source code
- docker

## Installation
Download the script and put it in your PATH.

`curl https://raw.githubusercontent.com/jodersky/vcluster/master/vcluster -o ~/bin/vcluster && chmod 0755 ~/bin/vcluster`

## Usage

1. Create docker image from Spark's source

		vcluster init <path to spark's source>
		
2. Spin up a "local cluster", consisting of several containers

		vcluster start <number of workers, default 5>
		
3. Start spark-shell in a container

		vcluster shell
		
4. Show the status of the cluster

		vcluster list
		
5. Shut down the cluster

		vcluster stop
