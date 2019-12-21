# Using `label` and `input`

> stackoverflow - https://stackoverflow.com/questions/774054/should-i-put-input-elements-inside-a-label-element  
> From w3: The label itself may be positioned before, after or around the associated control. 

```html
<label for="lastname">Last Name</label>
<input type="text" id="lastname" />
```

or

```html
<input type="text" id="lastname" />
<label for="lastname">Last Name</label>
```

or

```html
<label>
   <input type="text" name="lastname" />
   Last Name
</label>
```

> **If you include the input tag in the label tag, you don't need to use the 'for' attribute.**    
That said, I don't like to include the input tag in my labels because I think they're separate, not containing, entities.
