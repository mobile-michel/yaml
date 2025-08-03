---
title: Data types
---
# {title}
- scalars: string, numbers, booleans
- sequences: list of values
- maps: key-value pairs

## Scalars example

- name: {name} `{name}`
- age: {age} `{age}`
- employed: {employed} `{employed}`
- e-mail: {email} `{email}`

## Sequence example

[sequence] `[sequence]`

sequence.html file:

```html
<div @name="sequence">
    <p>List of hobbies:</p>
    <ul :for="item in hobbies">
        <li>{item}</li>
    </ul>
</div>
```

## Map example

- street: {address.street} `{address.street}`
- city: {address.city} `{address.city}`
- state: {address.state} `{address.state}`
