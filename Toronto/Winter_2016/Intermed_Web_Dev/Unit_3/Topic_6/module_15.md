<section class="module-section" name="Completing This Challenge">&nbsp;</section>

## Completing This Challenge

Test your code by making 5 Red Audi TTs. If you log your car factory to the console in Chrome, it should look similar to the following:

	    CarFactory {
	    	brand: "Audi", 
	    	numberOfCars: 5, 
	    	carsAvailable: Array[5]
	    		0: Car
	    			make: "Audi"
	    			model: "TT"
	    			color: "Red"
	    			__proto__: Car
	    		1: Car1: Car
	    		2: Car2: Car
	    		3: Car3: Car
	    		4: Car4: Car
	    		length: 5
	    		__proto__: Array[0]
	    		manufacture: () {
	    		numberOfCars: 5
	    		__proto__: CarFactory
	    }

If you log it to the console in Sublime, it might look something like this:

	    { brand: 'Audi',
	      numberOfCars: 5,
	      carsAvailable: 
	       [ { make: 'Audi', model: 'TT', color: 'red' },
	         { make: 'Audi', model: 'TT', color: 'red' },
	         { make: 'Audi', model: 'TT', color: 'red' },
	         { make: 'Audi', model: 'TT', color: 'red' },
	         { make: 'Audi', model: 'TT', color: 'red' } ],
	      manufacture: [Function] }
