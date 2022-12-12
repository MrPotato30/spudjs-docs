# Reply Options

```js
<ButtonPagination>.replyOptions ( { options }, enabled )
```

## options
### mention
- Boolean
- Default: true
```js
.replyOption({
  mention: false;
})
```

---

### ephemeral
- Boolean
- Default: false
- Only for interactions
```js
.replyOption({
  ephemeral: true;
})
```

---

### interaction
- Boolean
- Default: false
```js
.replyOption({
  interaction: true;
})
```

---

### message
- Discord.Message
- Default: message
```js
.replyOption({
  message: message,
})
```

---

### type
- Default: "reply"
```js
.replyOption({
  message: message,
  type: "editReply" // for interactions
})
```

---

## enabled
### Boolean
- Default: false;
```js
.replyOption({ ... }, true)
```
