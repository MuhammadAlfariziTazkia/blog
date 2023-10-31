---
description: Manage the access right of our resource
---

# Encapsulation

Encapsulation is the one of four main pillars in Object Oriented Programming

This is crucial concept that allow programmer to manage and organize the access right of the attribute, method, or even the class.

Main Idea -> restricting direct access to class attribute, and enforce manipulation of class attribute only happened in that class. So another class cannot modify attribute of that class

This is example for bad code

```
class Account {
    Account () {
        amount = 0;
        accountNumber = "123123";
    }
    int amount;
    String accountNumber;
}

class Transaction {
    void createTransaction(int amount) {
        Account myAccount = new Account();
    }
```

## Modifier

<table><thead><tr><th width="233"></th><th width="120">Class</th><th width="125">Package</th><th width="133">Subclass</th><th width="330">World</th></tr></thead><tbody><tr><td>no-modifier</td><td>YES</td><td>YES</td><td></td><td></td></tr><tr><td>public</td><td>YES</td><td>YES</td><td>YES</td><td>YES</td></tr><tr><td>protected</td><td>YES</td><td>YES</td><td>YES</td><td></td></tr><tr><td>private</td><td>YES</td><td></td><td></td><td></td></tr></tbody></table>
