# Classify battery health

This assignment consists of two parts:

1. Computing the state-of-health (SoH) of a battery
2. Classifying batteries as Healthy, Replace or Failed

## Computing health

As batteries age, they lose their capacity to store charge.

The state-of-health (SoH) of a battery compares a used battery and a fresh battery. It is a measure of aging, expressed as a percentage:

`SoH% = 100 * present_capacity / rated_capacity`

`present_capacity` =  The charge available in the battery, after a full charge.
`rated_capacity` = The rated capacity of a new battery.

For example, the rated capacity of a battery is `120 Ah`. It now gives only `105 Ah` after charging - that is its present capacity. Then, its SoH is calculated as:

`SoH% = 100 * 105 / 120 = 87.5%`

## Classifying batteries by SoH

Input is the present capacity of a bunch of batteries. Assume all of them have a rated capacity of 120 Ah.

You need to count how many are `healthy`, how many can `exchange`, and how many have already `failed`, as per the criteria below.

Batteries are classified by SoH:

- SoH more than `80%`, up to `100%`: classified as `healthy`
- SoH between `80%` and `62%`: classified as `exchange`
- SoH below `62%`: classified as `failed`

The code needs to:
1. Convert present capacity to SoH
1. Classify using the above ranges
1. Count the number of batteries falling under each classification.

The code in this repository already has a function to do this. However, this function is not yet implemented.

There is also a test function in the code.
The asserts express what's needed from the code. Do not change or remove the asserts.
Feel free to add more asserts, though.

Of course, the function isn't implemented yet, and returns wrong values. Hence the condition in the assert fails and it aborts the program.

Implement the function to count correctly and pass the test.

## Evaluation criteria

- Readability of variable names, code-flow, usage of comments only when necessary
- Improvements to existing code and tests
- Precision: adding new tests (such as boundary conditions)
