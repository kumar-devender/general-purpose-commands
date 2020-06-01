#### grep
```
history | grep 'docker'
```
#### tail
`tail -f result.log`

`tail -n 100 result.log`

`tail -n 15 -F result.log`

`tail -n 15 -F result.log`

Display only last 15 line

`watch tail -n 15 result.log`

Control watch timer. Below lime will watch logs every 1 second

`watch -n 1 tail -n 15 result.log`

Want to copy logs line into other file

`tail -100 result.log  > newLogfile`
