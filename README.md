const heart = new mojs.Shape({

shape: 'heart',

fill: 'none',

stroke: 'white',

scale: {0: 3},

strokeWidth: { 50: 0 },

y: 25,

duration: 1000,

delay: delay_2

}).then({

shape: 'heart',

stroke: 'white',

scale: 0,

strokeWidth: 50,

duration: 200

}).then({

shape: 'heart',

fill: 'red',

stroke: 'none',

scale: 2,

strokeWidth: 0,

duration: 600

});

const crazy = new mojs.Burst({

radius: { 10: 1000 },

count: 10,

children: {

shape: 'circle',

delay: delay_2,

duration: 2500

} });

const timeline = new mojs.Timeline({

onComplete: function () {

window.location.href = 'Valentine.html';

}

});

timeline.add(ring1, ring2, ring3, ring4, firstExplosion, firstExplosionBG);

timeline.add(crazy, rect, heart);

timeline.play();

const loveElement= document.getElementById('love'); loveElement.addEventListener('click', function () {

window.location.href = 'Valentine.html';

});
