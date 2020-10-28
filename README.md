# bag2_wrappers
This repo contains wrappers for common ideal components which may not be set up correctly in the BAG process setup. In other words, this is _not_ intended for things like ideal amplifiers, filters; this is for things like capacitors, resistors, etc.

## Warning
* Sometimes the BAG cache won't like if you have multiple layers of hierarchy with these components. Be sure to check that your generated schematic has the correct final value.

## Using Components in BAG Schematic Generators
1. Instantiate the component (e.g. `res_ideal`) in your schematic.
2. To specify values for the component in your schematic generator script, it should be `self.instances[<name>].parameters[res_val] = <value>` instead of `self.instances[<name>].design()`
