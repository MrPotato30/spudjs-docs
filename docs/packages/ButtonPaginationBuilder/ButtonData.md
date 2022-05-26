# <ins>Button Names and Properties</ins>

## <ins>Button Names</ins>

#### type: [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

### first
- Only displayed if `fastSkip` is enabled
- Travel to the first page
- Default (emoji: ⏪, style: PRIMARY )

### previous
- Always displayed
- Travel to the previous page
- Default (emoji: ◀️, style: PRIMARY )

### next
- Always displayed
- Travel to the next page
- Default (emoji: ▶️, style: PRIMARY )


### last
- Only display if `fastSkip` is enabled
- Travel to the last page
- Default (emoji: ⏩, style: PRIMARY )


### pageTravel
- Only displayed if `pageTravel` is enabled
- Type in channel the page to travel
- Default (emoji: #️⃣, style: SUCCESS )

### pageTravel
- Only displayed if `trash` is enabled
- Deletes the pagination
- Default (emoji: ⛔, style: DANGER )

## <ins>Button Properties</ins>

#### type: [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

### Style
- The style the button uses. <ins>**Must**</ins> be a valid [Discord Button Style](https://discord.com/developers/docs/interactions/message-components

### Emoji
- Emoji displayed on the button

### Label
- Text displayed on the button


--- 

## Example:
```js
.setButton("previous", {
  style: "SUCCESS", 
  emoji: "⬅️", 
  label: "back"
});
```

### Result: 

![image](https://user-images.githubusercontent.com/85820415/170090386-3babc322-56ee-4447-ac63-11da14c7402d.png)
