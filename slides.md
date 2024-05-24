---
theme: seriph
title: Mathias Ewald
info: |
  Introduction of myself
highlighter: shiki
drawings:
  persist: false
transition: slide-up
mdc: true
layout: cover
---
# About Me
---
layout: two-cols
layoutClass: gap-10
---

<style>
.slidev-layout {
  padding: 0px !important;
}
.slidev-code {
  margin-top: -4px !important;
  overflow-y: auto;
}
</style>

````md magic-move {at:1}
```java {2-4|2-4}
Person me = Person.Builder()
  .firstname("Mathias")
  .lastname("Ewald")
  .picture("data:image/png;base64, MAbE78rH/s676RtuuGHfqWOn3rOyevr22GrujM30lyIw7j179+zZPzMdysO5edFY0vHFqGVTJRKe")
  .build();
```
```java{5-12}
Person me = Person.Builder()
  .firstname("Mathias")
  .lastname("Ewald")
  .picture("data:image/png;base64, MAbE78rH/s...;)")
  .techSpecs(TechSpecs.Builder()
    .birthday(LocalDate.of(1986, 5, 21))
    .height(CENTI(METER).times(203))
    .weight(KILO(GRAM).times(101))
    .eyeColor("#7c3f00")
    .nationality(
      CountryCode.getByCode("DE"))
    .shoeSize("EU_50")
    .build())
  .build();
```
```java{10,13-17}
Person me = Person.Builder()
  .firstname("Mathias")
  .lastname("Ewald")
  .picture("data:image/png;base64, MAbE78rH/s...;)")
  .techSpecs(TechSpecs.Builder()
    .birthday(LocalDate.of(1986, 5, 21))
    .height(CENTI(METER).times(203))
    .weight(KILO(GRAM).times(101))
    .eyeColor("#7c3f00")
    .nationality(CountryCode.getByCode("DE"))
    .shoeSize("EU_50")
    .build())
  .location("48.116725,16.8642415")
  .build();
```
```java{3-14|15-24}
Person me = Person.Builder()
  ...
  .married(true)
  .partner(Person.Builder()
    .firstname("Veronika")
    .lastname("Konova")
    .build())
  .kids(Set.of(
    Kid.Builder()
      .firstname("Elena")
      .lastname("Ewald")
      .birthday(LocalDate.of(2023, 5, 21))
      .build()
  ))
  .pets(List.of(
    Pet.Builder()
      .species(Animals.DOG)
      .breed("Hovawart")
      .name("Zoja"),
    Pet.Builder().species(Animals.CHICKEN),
    Pet.Builder().species(Animals.CHICKEN),
    Pet.Builder().species(Animals.CHICKEN),
    Pet.Builder().species(Animals.CHICKEN)
  ))
  ...
```
```java
Person me = Person.Builder()
  ...
  .hobbies(Set.of(
    "Basketball",
    "Running"
  ))
  .interests(Set.of(
    "AI/ML",
    "ATEM" // Advanced Television Environment Manager
  ))
  ...
```
````

::right::

<div style="display: flex; flex-direction: column; justify-content: start; align-items: center; gap: 24px;">

<v-click at="1">
<img src="/me.png" width="200px" /> 
</v-click>

<v-switch>
<template #1>
<Arrow x1="400" y1="90" x2="650" y2="120"/>
</template>
<template #2>
<Arrow x1="200" y1="170" x2="680" y2="230"/>
<div style="display: flex; flex-direction: column; justify-content: start; align-items: center; gap: 24px;">
<span style="background-color: #7c3f00; padding: 5px;">#7c3f00</span>
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d332104.0750265451!2d10.804097862440315!3d49.43607365304772!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x479f57aeb5b61cd3%3A0xdd5daf85a98c21b7!2sNuremberg%2C%20Germany!5e0!3m2!1sen!2sat!4v1716575105035!5m2!1sen!2sat" width="300" height="200" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
</div>
</template>
<template #3>
<Arrow x1="270" y1="240" x2="580" y2="300"/>
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d42618.61740696384!2d16.8642414523324!3d48.116724970906!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x476cf5a1e636104b%3A0xb7ef635f6118f90b!2s2405%20Bad%20Deutsch-Altenburg!5e0!3m2!1sen!2sat!4v1716575589561!5m2!1sen!2sat" width="300" height="200" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
</template>
<template #4>
  <img src="" width="500px" height="300px" alt="Family Photo"/>
</template>
<template #5>
  <img src="" width="500px" height="300px" alt="Family Photo"/>
</template>
</v-switch>
</div>
---
layout: end
---

---