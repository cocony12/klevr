# Make declare first
# declare -x WEBCONSOLE="192.168.2.100:8000"
# or use under variable
# WEBCONSOLE=localhost:8080
hello:
	# make run/build

init:
	go mod init
require:
	go get -u

build: require
	go build -o ./Dockerfile/klevr ./main.go
run:
##	go run ./main.go -id=ralf -platform=baremetal -webconsole=${WEBCONSOLE} -zone=dev -group="klevr-a-team"
	go run ./main.go -apiKey="apiKey" -platform="linux_laptop" -manager="192.168.15.163:8090" -zoneId="8282"

all: build
