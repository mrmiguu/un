# un
un.Wrap your errors

<b>Before:</b>
```go
b, err := json.Marshal(data)
if err != nil {
    panic(err)
}

...

reData := Data{}
err = json.Unmarshal(b, &reData)
if err != nil {
    panic(err)
}
```

<b>After!</b>
```go
b := un.Bytes(json.Marshal(data))

...

reData := Data{}
un.Wrap(json.Unmarshal(b, &reData))
```
