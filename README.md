
# un
un.Wrap your errors

Before:
```go
b, err := json.Marshal(data)
if err != nil {
    panic(err)
}
```

After!
```go
b := un.Bytes(json.Marshal(data))
```
