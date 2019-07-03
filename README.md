# NEAT.js

NeuroEvolution of Augmenting Topologies (NEAT) is a genetic algorithm (GA) for the generation of evolving artificial neural networks.

This library implements this technology in JavaScript.


## Getting Started

In order to add this library in your project you need to add NEAT.js script into your html file:

```html
<script src="/lib/NEAT.js"></script>
```

If you use Node.js you can add this module in your project like this:

```js
const NEAT = require('neat_net-js');
```

## Usage:

```js
var neat = new NEAT([40, 60, 60, 3], 100, .001, 'sigmoid');

// Parameters with order: Network structure, Population size, Mutation rate, Activation function (sigmoid or tanh.)

for (var i = 0; i < [INPUT_LAYER_NODE_COUNT]; i++) {
	neat.setInputs(ARRAY(INPUT_LAYER_NODE_COUNT), i);  // Set inputs for the creature indexed i.
}

neat.predict(); // Predicts the result value of all creatures

neat.doGen(); // Does 1 generation.

// doGen() calls crossover() mutate() to do 1 fast generation 
// you can call them seperately but it's not recommended.

```


## Parsing an existing network:

You can export the existing network and all of its population via:

```js
neat.exportNet();
```
This function will download your network and all of it's population as a JSON file.

Later you can parse the exported network like this:

```js
var neat2 = new NEAT([EXPORTED NETWORK GOES HERE WITHOUT BRACKETS!]);
```

With this method you can continue your training from where you left off.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## License
[MIT](https://choosealicense.com/licenses/mit/)
