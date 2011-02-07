Signals for Node.js
===================

Node.js version of JS Signals by Miller Medeiros. For documentation read [JS Signals documentation](http://millermedeiros.github.com/js-signals/).


Example
-------

	var signals = require('./signals');
	
	//custom object that dispatch a `started` signal
	var myObject = {
	  started : new signals.Signal()
	};
	function onStarted(param1, param2){
	  console.log(param1 + param2);
	}
	myObject.started.add(onStarted); //add listener
	myObject.started.dispatch('foo', 'bar'); //dispatch signal passing custom parameters
	myObject.started.remove(onStarted); //remove a single listener

License
-------
Released under MIT License. Enjoy and Fork!