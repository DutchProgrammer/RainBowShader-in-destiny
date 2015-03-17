# Rainbow shader and emblem

How to get a rainbow shader and emblem in [Destiny](https://bungie.com)

  - [Get FireFox](https://www.mozilla.org/nl/firefox/new/)
  - [Download firebug add-on for Firefox](https://addons.mozilla.org/nl/firefox/addon/firebug/)

### How to
1. Go to the [Destiny](https://bungie.com) website.
2. Login with your Destiny account and go to you profile and click on gear
3. Then copy the javascript like i have added below at section 'Javascript'
4. Change "var equipePiece      = 'shader';"  shader to emblem for emblem rainbow
5. Check if you emblem or shader is changing and check in game and have fun ;-)

>>> For the Tutorial Video check
[Youtube how to Video](http://youtu.be/gSn9Bedxa7g)


### Javascript (shader)
```js
var shaderEquipTimer = 2500;
var emblemEquipTimer = 2500;
var equipePiece      = 'shader';//use 'shader' or 'emblem'




function randomShader() {
	var total              = $('.gear .BUCKET_SHADER .bucketItem:not(.equipped) .itemAction').length;
	var selectRandomShader = Math.floor(Math.random() * total);
  
  $('.gear .BUCKET_SHADER .unequipped.bucketItem:not(.equipped) .itemAction').eq(selectRandomShader).click();
  
  
 waitForEquip(randomShader, shaderEquipTimer);
}

function randomEmblem() {
	var total              = $('.gear .BUCKET_EMBLEM .bucketItem:not(.equipped) .itemAction').length;
	var selectRandomEmblem = Math.floor(Math.random() * total);
  
  $('.gear .BUCKET_EMBLEM .unequipped.bucketItem:not(.equipped) .itemAction').eq(selectRandomEmblem).click();
  
  
 waitForEquip(randomEmblem, emblemEquipTimer);
}

function waitForEquip(callback, timer) {
  if ($('.equipItem').length == 1) {
    $('.equipItem').click();

    setTimeout(callback, parseInt(timer+1000));
  } else {
    setTimeout(function () {
    	waitForEquip(callback, timer);
    }, 100);
  }
  
}


if (equipePiece === 'shader') {
	setTimeout(randomShader, shaderEquipTimer);
} else {
	setTimeout(randomEmblem, emblemEquipTimer);
}
```


### Javascript emblem rainbow
```js
var shaderEquipTimer = 2500;
var emblemEquipTimer = 2500;
var equipePiece      = 'emblem';//use 'shader' or 'emblem'




function randomShader() {
	var total              = $('.gear .BUCKET_SHADER .bucketItem:not(.equipped) .itemAction').length;
	var selectRandomShader = Math.floor(Math.random() * total);
  
  $('.gear .BUCKET_SHADER .unequipped.bucketItem:not(.equipped) .itemAction').eq(selectRandomShader).click();
  
  
 waitForEquip(randomShader, shaderEquipTimer);
}

function randomEmblem() {
	var total              = $('.gear .BUCKET_EMBLEM .bucketItem:not(.equipped) .itemAction').length;
	var selectRandomEmblem = Math.floor(Math.random() * total);
  
  $('.gear .BUCKET_EMBLEM .unequipped.bucketItem:not(.equipped) .itemAction').eq(selectRandomEmblem).click();
  
  
 waitForEquip(randomEmblem, emblemEquipTimer);
}

function waitForEquip(callback, timer) {
  if ($('.equipItem').length == 1) {
    $('.equipItem').click();

    setTimeout(callback, parseInt(timer+1000));
  } else {
    setTimeout(function () {
    	waitForEquip(callback, timer);
    }, 100);
  }
  
}


if (equipePiece === 'shader') {
	setTimeout(randomShader, shaderEquipTimer);
} else {
	setTimeout(randomEmblem, emblemEquipTimer);
}
```

### Version
1.0.0

