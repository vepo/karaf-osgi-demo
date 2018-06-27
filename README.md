# Apache Karaf Docker example

This image of Karaf is build with a very simple Apache Camel command. It reads the files inside `/tmp/in` copying to `/tmp/out`.

## Start

```
docker build -t karaf .
docker run --name karaf -p 8101:8101 karaf
```

## Connect

Use the password `karaf`.

```
ssh -p 8101 karaf@localhost
```

## Test

1. Access: 
```
docker exec -it karaf bash
```

2. Create Input file

```
echo "TEST" > /tmp/in/test.txt
```

3. Check output

```
cat /tmp/out/test.txt
```