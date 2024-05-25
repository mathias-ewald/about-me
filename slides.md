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
.slidev-code {
  overflow-y: auto;
}
</style>

````md magic-move {at:1}
```java {2-4}
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
```java {3-6}
Person me = Person.Builder()
  ...
  .hobbies(Set.of(
    "Basketball",
    "Running"
  ))
  ...
```
```java {7-10}
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
```java {11-14|11-14}
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
  .projects(Set.of(
    "meanstream.io",
    "Flock AI"
  ))
  ...
```
````

::right::

<div style="display: flex; flex-direction: column; justify-content: start; align-items: center; gap: 24px;">
  <v-switch>
    <template #0>
      <img src="/me.png" width="200px" /> 
      <Arrow x1="490" y1="110" x2="650" y2="120"/>
    </template>
    <template #1>
      <Arrow x1="240" y1="200" x2="670" y2="60"/>
      <div style="display: flex; flex-direction: column; justify-content: start; align-items: center; gap: 24px;">
      <span style="background-color: #7c3f00; padding: 5px;">#7c3f00</span>
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d332104.0750265451!2d10.804097862440315!3d49.43607365304772!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x479f57aeb5b61cd3%3A0xdd5daf85a98c21b7!2sNuremberg%2C%20Germany!5e0!3m2!1sen!2sat!4v1716575105035!5m2!1sen!2sat" width="300" height="200" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
    </template>
    <template #2>
      <Arrow x1="320" y1="275" x2="550" y2="200"/>
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d42618.61740696384!2d16.8642414523324!3d48.116724970906!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x476cf5a1e636104b%3A0xb7ef635f6118f90b!2s2405%20Bad%20Deutsch-Altenburg!5e0!3m2!1sen!2sat!4v1716575589561!5m2!1sen!2sat" width="300" height="200" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </template>
    <template #3>
      <Carousel width="400px" :interval="2000" :sources="['/private/20240414_192500.jpg', '/private/20240414_192529.jpg', '/private/20240424_192010.png', '/private/20240501_154311.jpg', '/private/20240504_170406.jpg', '/private/20240524_163017.jpg']"></Carousel>
    </template>
    <template #4>
      <Carousel width="400px" :interval="2000" :sources="['/private/20240414_192500.jpg', '/private/20240414_192529.jpg', '/private/20240424_192010.png', '/private/20240501_154311.jpg', '/private/20240504_170406.jpg', '/private/20240524_163017.jpg']"></Carousel>
    </template>
    <template #5>
      <div style="display: flex; flex-direction: row; gap: 10px; justify-content: center; align-items: start;">
        <img src="/running.jpg" width="200px">
        <img src="/bball.png" width="200px" height="100px">
      </div>
    </template>
    <template #6>
      <SlidevVideo autoplay style="width: 100%">
        <source src="/switcher.hd.1080p.mp4" type="video/mp4" />
        <p>
          Your browser does not support videos. You may download it
          <a href="/switcher.hd.1080p.mp4">here</a>.
        </p>
      </SlidevVideo>
    </template>
    <template #7>
    <div style="margin-left: -300px; margin-top: 150px; display: flex; flex-direction: row; justify-content: center; align-items: start;">
      <div style="position: relative; width: 700px; height: 250px;">
        <img style="position: absolute; z-index: 0; width: 700px; left: 50%; top: 50%; transform: rotate(1deg) translate(-50%, -50%);" src="/meanstream.png">
      </div>
    </div>
    </template>
    <template #8>
    <div style="margin-left: -300px; margin-top: 150px; display: flex; flex-direction: row; justify-content: center; align-items: start;">
      <div style="position: relative; width: 700px; height: 250px;">
        <img style="position: absolute; z-index: 0; width: 700px; left: 50%; top: 50%; transform: rotate(1deg) translate(-50%, -50%);" src="/meanstream.png">
        <img style="position: absolute; z-index: 1; width: 700px; left: 50%; top: 50%; transform: rotate(-1deg) translate(-50%, -50%);" src="/flockai.png">
      </div>
    </div>
    </template>
  </v-switch>
</div>
---
layout: end
---

---