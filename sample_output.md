## Puppet noop output for commit: 'stop nginx on fozzie & add episode one'

### Commit [5c31a832dd238407c5d964edea794cdafd81c81f](https://github.braintreeps.com/lollipopman/muppetshow/commit/5c31a832dd238407c5d964edea794cdafd81c81f)

- *Author:* lollipopman (<hathaway@paypal.com>)
- *Message:*
  ```
  stop nginx on fozzie & add episode one
  
  stop nginx on fozzie
  add episode one
  modify wit on statler
  modify poignant on waldor
  modify slapstick on fozzie
  
  ```

### Puppet Resource Changes (noop)

1.  **File[/data/puppet_apply/cast]**
    - *Diff:*
      ```diff
      @@ -1 +1,2 @@
      -Cookie Monster
      +Miss Piggy
      +Rowlf the Dog
      ```
    - *Hosts:* fozzie.example.com, statler.example.com, waldorf.example.com
    - *Define Type:* **Concat[/data/puppet_apply/cast]**
    - *Current State:* {md5}9a21a9ced788104a4f937ebd113c62d3
    - *Desired State:* {md5}65fddd5ddf8227027bc41117b09ada27

2.  **File[/data/puppet_apply/fozzie/slapstick]**
    - *Hosts:* fozzie.example.com
    - *Current State:* file
    - *Desired State:* absent

3.  **File[/data/puppet_apply/laughtrack]**
    - *Diff:*
      ```diff
      @@ -0,0 +1,2 @@
      +Wacka
      +Wacka
      ```
    - *Hosts:* fozzie.example.com, statler.example.com, waldorf.example.com
    - *Define Type:* **Muppetshow::Episode[One]**
    - *Current State:* {md5}d41d8cd98f00b204e9800998ecf8427e
    - *Desired State:* {md5}15d4a7e90a35a1b9d8d69deecbf9f7d0

4.  **File[/data/puppet_apply/statler/wit]**
    - *Diff:*
      ```diff
      @@ -1 +1 @@
      -terrible
      +foul
      ```
    - *Hosts:* statler.example.com
    - *Current State:* {md5}114457bbbd50c0aca9f294e02c4ca712
    - *Desired State:* {md5}0476788129760a948a9b6a0e5275e965

5.  **File[/data/puppet_apply/waldorf/poignant]**
    - *Diff:*
      ```diff
      @@ -1 +1 @@
      -acerbic
      +sour
      ```
    - *Hosts:* waldorf.example.com
    - *Current State:* {md5}2af84c70543edf1599b4eccdc65247c0
    - *Desired State:* {md5}4ac18c74645273475594a9c255e321f0

6.  **Service[nginx]**
    - *Hosts:* fozzie.example.com
    - *Current State:* running
    - *Desired State:* stopped

## Puppet noop output for commit: 'finish the muppet show lyrics'

### Commit [5e224ecda620c68036e9dec6fced35d0b56e0444](https://github.braintreeps.com/lollipopman/muppetshow/commit/5e224ecda620c68036e9dec6fced35d0b56e0444)

- *Author:* lollipopman (<hathaway@paypal.com>)
- *Message:*
  ```
  finish the muppet show lyrics
  
  finish composing the muppet show lyrics
  move index out of muppetshow class into node
  class
  
  ```

### Puppet Resource Changes (noop)

1.  **File[/data/puppet_apply/the_muppet_show]**
    - *Diff:*
      ```diff
      @@ -6,3 +6,14 @@
       It's time to put on make up
       It's time to dress up right
       It's time to raise the curtain on the Muppet Show tonight
      +
      +Why do we always come here
      +I guess we'll never know
      +It's like a kind of torture
      +To have to watch the show
      +
      +But now let's get things started
      +Why don't you get things started
      +It's time to get things started
      +On the most sensational, inspirational, celebrational, muppetational
      +This is what we call the Muppet Show
      ```
    - *Hosts:* fozzie.example.com, statler.example.com, waldorf.example.com
    - *Current State:* {md5}eb554c301d10b04fb72261d721990270
    - *Desired State:* {md5}52a949d5beed1782e28094c8a74b8ac1

2.  **File[/var/www/html/index.html]**
    - *Diff:*
      ```diff
      @@ -1 +1 @@
      -Muppets
      +Fozzie
      ```
    - *Hosts:* fozzie.example.com
    - *Current State:* {md5}e5deafb6425abb47e5a1efef8b969fb8
    - *Desired State:* {md5}a148678410c6e6abb9fe0103391f3692

3.  **File[/var/www/html/index.html]**
    - *Diff:*
      ```diff
      @@ -1 +1 @@
      -Muppets
      +Statler
      ```
    - *Hosts:* statler.example.com
    - *Current State:* {md5}e5deafb6425abb47e5a1efef8b969fb8
    - *Desired State:* {md5}2599d35b2c0893c7dea8a07c372b02a0

4.  **File[/var/www/html/index.html]**
    - *Diff:*
      ```diff
      @@ -1 +1 @@
      -Muppets
      +Waldorf
      ```
    - *Hosts:* waldorf.example.com
    - *Current State:* {md5}e5deafb6425abb47e5a1efef8b969fb8
    - *Desired State:* {md5}afc384a68e4fae8b8d257e15cd167a48

5.  **Service[nginx]**
    - *Hosts:* statler.example.com, waldorf.example.com
    - *Logs:*
        - Would have triggered 'refresh' from 1 event

## Puppet noop output for commit: 'add some fun diversions'

### Commit [c0f10fde295abfd720b99e1990fa3441790c086c](https://github.braintreeps.com/lollipopman/muppetshow/commit/c0f10fde295abfd720b99e1990fa3441790c086c)

- *Author:* lollipopman (<hathaway@paypal.com>)
- *Message:*
  ```
  add some fun diversions
  
  add bsdgames on fozzie
  add sl to statler & waldorf
  
  ```

### Puppet Resource Changes (noop)

1.  **Package[bsdgames]**
    - *Hosts:* fozzie.example.com
    - *Current State:* purged
    - *Desired State:* present

2.  **Package[sl]**
    - *Hosts:* statler.example.com, waldorf.example.com
    - *Current State:* purged
    - *Desired State:* present

## Puppet noop output for commit: 'add kermit user, modify sail input'

### Commit [d5a20cb8f8bc07a4d646c74612296f7757ea5749](https://github.braintreeps.com/lollipopman/muppetshow/commit/d5a20cb8f8bc07a4d646c74612296f7757ea5749)

- *Author:* lollipopman (<hathaway@paypal.com>)
- *Message:*
  ```
  add kermit user, modify sail input
  
  add kermit user and muppetshow group
  modify the input to the sail game
  
  ```

### Puppet Resource Changes (noop)

1.  **Exec[sail]**
    - *Hosts:* fozzie.example.com
    - *Logs:*
        - Would have triggered 'refresh' from 1 event

2.  **File[/data/puppet_apply/fozzie/styx]**
    - *Diff:*
      ```diff
      @@ -0,0 +1 @@
      +Come Sail Away
      ```
    - *Hosts:* fozzie.example.com
    - *Current State:* {md5}d41d8cd98f00b204e9800998ecf8427e
    - *Desired State:* {md5}d256d47934e09aa4e80b8e6e5b5519c4

3.  **Group[muppets]**
    - *Hosts:* fozzie.example.com, statler.example.com, waldorf.example.com
    - *Current State:* absent
    - *Desired State:* present

4.  **User[kermit]**
    - *Hosts:* fozzie.example.com, statler.example.com, waldorf.example.com
    - *Current State:* absent
    - *Desired State:* present

## Puppet noop output for commit: 'New Movie'

### Commit [3da5b8e9dbf204096096401923f4781feca89900](https://github.braintreeps.com/lollipopman/muppetshow/commit/3da5b8e9dbf204096096401923f4781feca89900)

- *Author:* lollipopman (<hathaway@paypal.com>)
- *Message:*
  ```
  New Movie
  
  ```

### Puppet Resource Changes (noop)

1.  **File[/data/puppet_apply/fozzie/manhattan]**
    - *Hosts:* fozzie.example.com
    - *Current State:* absent
    - *Desired State:* present

## Puppet noop output for commit: 'Gonzo'

### Commit [12399ce674ff4b4abe4585173ff88360849703b3](https://github.braintreeps.com/lollipopman/muppetshow/commit/12399ce674ff4b4abe4585173ff88360849703b3)

- *Author:* lollipopman (<hathaway@paypal.com>)
- *Message:*
  ```
  Gonzo
  
  ```

### Puppet Resource Changes (noop)

1.  **File[/data/puppet_apply/fozzie/manhattan]**
    - *Hosts:* waldorf.example.com
    - *Current State:* absent
    - *Desired State:* present
