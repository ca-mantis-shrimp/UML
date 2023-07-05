```
@startuml
title Objects and Interfaces

interface Zzapper <<FooFoo>>  {
  +publicAbc()
  #protectedAbc()
}

object Zzap {
  int a
  int b
  --
  +publicAbc()
  #protectedAbc()
  -privateAbc()
  note: This is an object
  ==
  note: here is a loop
}

object User {
  name = "dummy"
  id = 123
  --
  +userJump(int length)
  +userEat(Food food)
}

object Food {
  int calories
  string name
}

object Store {
  name = "superCat"
  id = 347
}

Zzapper --> Zzap

User --|> Store
User --|> Zzap

Food --* User
Food --o Store
@enduml
```
