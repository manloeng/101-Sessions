.PHONY: build clean deploy

build:
	env GOOS=linux go build -ldflags="-s -w" -o bin/hello hello/main.go
	env GOOS=linux go build -ldflags="-s -w" -o bin/sendWait sendWait/main.go
	env GOOS=linux go build -ldflags="-s -w" -o bin/printItem printItem/main.go
	env GOOS=linux go build -ldflags="-s -w" -o bin/processItem processItem/main.go
	env GOOS=linux go build -ldflags="-s -w" -o bin/flakey flakey/main.go
	env GOOS=linux go build -ldflags="-s -w" -o bin/monitor monitor/main.go

clean:
	rm -rf ./bin

deploy: clean build
	sls deploy --verbose
