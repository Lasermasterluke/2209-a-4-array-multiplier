<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

An array multiplier performs binary multiplication by breaking down the multiplicand and multiplier into bits and computing partial products. These partial products are then summed row by row to form the final product.

Here's a visual representation of how an array multiplier works:

```mermaid
graph TD
    A[Multiplicand A - Bits A3 A2 A1 A0]
    B[Multiplier B - Bits B3 B2 B1 B0]

    subgraph Partial_Products
        A3B0[A3 * B0] --> A3B1[A3 * B1] --> A3B2[A3 * B2] --> A3B3[A3 * B3]
        A2B0[A2 * B0] --> A2B1[A2 * B1] --> A2B2[A2 * B2] --> A2B3[A2 * B3]
        A1B0[A1 * B0] --> A1B1[A1 * B1] --> A1B2[A1 * B2] --> A1B3[A1 * B3]
        A0B0[A0 * B0] --> A0B1[A0 * B1] --> A0B2[A0 * B2] --> A0B3[A0 * B3]
    end

    Sum[Sum of Partial Products]
    Output[Final Product]

    A --> Partial_Products
    B --> Partial_Products
    Partial_Products --> Sum
    Sum --> Output
```

## How to test

To test the array multiplier:

1. Set up the multiplier by providing binary inputs for both the multiplicand (A) and the multiplier (B).
2. Run the simulation or test in hardware to verify that each partial product is calculated correctly.
3. Ensure that the partial products are properly shifted and summed to produce the final product.
4. Compare the final output with the expected result from standard binary multiplication to confirm accuracy.

## External hardware

No external hardware is required for this project. The array multiplier can be tested within a simulation environment or with an FPGA setup if hardware verification is needed.
