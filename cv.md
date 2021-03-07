
# Aliaksei Karzhou

## Contacts

* phone: [+375291043897](tel:+375291043897)
* mail: [alexius90e@gmail.com](mailto:alexius90e@gmail.com)
* telegram: @alexeykarzhov

## Summary

Краткая информация о себе (ваша цель и приоритеты, подчеркните свои сильные стороны, расскажите о своём опыте работы, если опыта работы нет, расскажите о своём стремлении и способности быстро учиться и узнавать новое)

## Technical Skills

* HTML5, CSS, SCSS
* Javascript, jQuery
* Python
* Bootstrap
* React JS

## Code examples

This code creates the class that emulates vigenere ciphering machine.

```
class VigenereCipheringMachine {
  constructor(isDirect = true) {
    this.isDirect = isDirect;
    this.letters = [...'ABCDEFGHIJKLMNOPQRSTUVWXYZ']
  }
  encrypt(message, key) {
    if (message === undefined || key === undefined){
      throw new Error();
    }
    message = message.toUpperCase().split('');
    key = key.toUpperCase()
    .repeat(Math.ceil(message.length / key.length))
    .slice(0, message.length)
    .split('');
    let diff = 0;
    let result = message.map((item, index) => {
      if (this.letters.includes(item)){
        return this.letters[(this.letters.indexOf(item) + this.letters.indexOf(key[index - diff])) % this.letters.length];
      } else {
        diff += 1;
        return item;
      }
    })
    return this.isDirect ? result.join('') : result.reverse().join('');
  }    
  decrypt(message, key) {
    if (message === undefined || key === undefined){
      throw new Error();
    }
    message = message.toUpperCase().split('');
    key = key.toUpperCase()
    .repeat(Math.ceil(message.length / key.length))
    .slice(0, message.length)
    .split('');
    let diff = 0;
    let result = message.map((item, index) => {
      if (this.letters.includes(item)){
        return this.letters[(this.letters.indexOf(item) + this.letters.length - this.letters.indexOf(key[index - diff])) % this.letters.length];
      } else {
        diff += 1;
        return item;
      }
    })
    return this.isDirect ? result.join('') : result.reverse().join('');
  }
}
```

## Experience

2020 IdeaWebLab front-end developer

## Education

Mogilev State University of Food Technologies, speciality: Automation of Technological Processes and Production

## English Level
English Elementary(A2)
