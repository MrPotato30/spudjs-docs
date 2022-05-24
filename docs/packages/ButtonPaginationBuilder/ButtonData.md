# Button Names and Properties

## ButtonNames

#### type: [String]()

### first
- Only display if `fastSkip` is enabled
- Travel to the first page
- default (emoji: ⏪, style: PRIMARY )

### previous
- Always display
- Travel to the previous page
- default (emoji: ◀️, style: PRIMARY )

### next
- Always display
- Travel to the next page
- default (emoji: ▶️, style: PRIMARY )


### last
- Only display if `fastSkip` is enabled
- Travel to the last page
- default (emoji: ⏩, style: PRIMARY )


### pageTravel
- Only display if `pageTravel` is enabled
- Type in channel the page to travel
- default (emoji: #️⃣, style: SUCCESS )

### pageTravel
- Only display if `trash` is enabled
- deletes the pagination
- default (emoji: ⛔, style: DANGER )

## ButtonProperties

#### type: [Object]()

### style
- must be a valid discord button style

### emoji
- button emoji

### label
- button label


--- 

## Example:
```js
.setButton("previous", {
  style: "SUCCESS", 
  emoji: "⬅️", 
  label: "back"
 })
```

### result: 
- the previous button

![image](https://user-images.githubusercontent.com/85820415/170090386-3babc322-56ee-4447-ac63-11da14c7402d.png)
