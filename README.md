# Door-Lock-System
Is a circuit design for a PIN based door lock mechanism
The circuit includes 4 major moodules:
1. The input number sequencer and display module
  This module has 10 inputs for the ten digits and uses K mapping to make a schema that sequences between the digits 0-9. It basically 
  does binary operations to decide on the digit pressed, below it is a display unit which shows which digits were pressed. It is connected 
  to the input directly.
2. Registers
  There are three registers connected to the output of the input sequencer that propagate and save the 3 digit pin entered in the keypad via
  the inputs.
3. Comparators
  There are three comparators that compare the values of the three inputs entered from the outputs of the registers to the saved value of the 
  PIN found above. It uses encoder to convert the bits of the saved PIN. The comparator uses basic XOR, NOT and AND gates to compare two inputs.
4. J Flipflops
  The final piece is the J flipflops which hold the number of digits that are allowed to be entered. It resets the count as soon as three digits 
  are entered, the comparator checks the digits and if it is the same, the output LED found just before the flipflops glow, if it is not the same
  then the flipflops reset the circuit.
