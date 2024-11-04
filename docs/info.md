<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

```mermaid
graph TD
    A[Multiplicand (A) - Bits: A3, A2, A1, A0]
    B[Multiplier (B) - Bits: B3, B2, B1, B0]

    subgraph Partial_Products_Matrix
        A3B0[A3 * B0] --> A3B1[A3 * B1] --> A3B2[A3 * B2] --> A3B3[A3 * B3]
        A2B0[A2 * B0] --> A2B1[A2 * B1] --> A2B2[A2 * B2] --> A2B3[A2 * B3]
        A1B0[A1 * B0] --> A1B1[A1 * B1] --> A1B2[A1 * B2] --> A1B3[A1 * B3]
        A0B0[A0 * B0] --> A0B1[A0 * B1] --> A0B2[A0 * B2] --> A0B3[A0 * B3]
    end

    Sum[Summing Partial Products]
    Output[Final Product]

    A --> Partial_Products_Matrix
    B --> Partial_Products_Matrix
    Partial_Products_Matrix --> Sum
    Sum --> Output


## How to test

Explain how to use your project

## External hardware

List external hardware used in your project (e.g. PMOD, LED display, etc), if any
