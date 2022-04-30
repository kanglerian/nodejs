# Learn NodeJS

## Basic

### Membuat project baru

```console
mkdir project
cd project
npm init
```

### Buat file baru `apps.js`

```js
const nama = "Lerian"
console.log(nama)
```

### Run `apps.js`

```console
$ node apps.js
```

## Built-in

## Copy Filesystem

```js
const fs = require('fs')
fs.copyFileSync("teks.txt", "teks2.txt")
console.log("sukses")
```

## Install module eksternal

```console
$ npm install superheroes --save
```

```js
const hero = require('superheroes')

for(let i = 0; i < 10; i++){
    console.log(hero.random())
}
```

## Membuat module sendiri

1. Membuat file `module.js`

```js
exports.tambah = function(a,b){
    return a + b
}
```

2. Tulis di `apps.js`

```js
const sendiri = require('./module')
const pertambahan = sendiri.tambah(10,20)
console.log(pertambahan)
```