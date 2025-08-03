---
title: Complex data structures
unlisted: true
---
# {title}

[page-list]

## Nested maps

The map "address" is nested within the map "person".

```
people:
  name: John Doe
  age: 30
  address:
    street: 123 Main St.
    city: Anytown
    state: CA
```

## Sequences of maps

The sequence "peoples" contains two maps (two people).

```
peoples:
  - name: John Doe
    age: 30
    address:
      street: 123 Main St.
      city: Anytown
      state: CA
  - name: Jane Doe
    age: 25
    address:
      street: 456 Elm St.
      city: Anytown
      state: CA
```

## Inheritance of maps

The maps "employee" & "student" inherits from the map "default" 

```
people:
  &default
  name: John Doe
  age: 30
  address:
    street: 123 Main St.    
    city: Anytown
    state: CA

  employee:
    <<: *default
    position: Manager
    salary: 50000

  student:
    <<: *default
    course: Computer science
    grade: A
```