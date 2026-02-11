# Prime number checker
Prime number checker with y86-64 x86 logic. The code is quite riddled with comments, but I most likely won't be clearing it up later.

The "step-heaviest" subroutine is modular exponentiation (modexp), and as explained in the comments; by comparing bitmask > exponent whenever suitable, especially in modexp, I managed to reduce runtime from ~18s to ~2s.

Stack is only used modpow and modulo, and it might be possible to start shuffling registers to avoid stack entirely, but considering y86 limited registers, I found it better to use Stack in these instances.
