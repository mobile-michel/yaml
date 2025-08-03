---
title: Nested maps
date: 2025-08-03
---
# {title}

```
user_profile:
  # Standard key-value pairs
  id: 12345
  username: johndoe
  email: johndoe@example.com

  # 'address' is a key whose value is another map
  address:
    street: 123 Main St
    city: Anytown
    state: CA
    zip_code: "90210"

  # 'preferences' is another nested map
  preferences:
    theme: dark
    notifications:
      email: true
      sms: false
```

- id: {user_profile.id}
- username: {user_profile.username}
- email: {user_profile.email}
- street: {user_profile.address.street}
- city: {user_profile.address.city}
- state: {user_profile.address.state}
- zip_code: {user_profile.address.zip_code}
- theme: {user_profile.preferences.theme}
- email notifications: {user_profile.preferences.notifications.email}
- sms notifications: {user_profile.preferences.notifications.sms}