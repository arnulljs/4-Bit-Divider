# 🔢 4-Bit Binary Divider (Restoring Division Logic)

This project implements a **4-bit binary divider** using **restoring division** logic in a digital circuit, built using basic TTL components like multiplexers, shift registers, full adders, counters, and 7-segment displays.
This project was made in fulfillment of CPE 2301 Logic Circuits and Design Comprehensive Design Project output. 

## 📂 Project Contents

- `Circuit_Simulation/`
- `Documentation/`
- `README.md`

## ⚙️ How It Works

The divider performs **unsigned integer division** by repeatedly subtracting the divisor from the remainder and counting how many valid subtractions occur. It uses:
- A **multiplexer with selection logic** to choose between initial dividend and subtraction results
- A **shift register** to store and shift the remainder
- A **full adder** for subtraction (via 2’s complement)
- A **counter** to accumulate the quotient
- A **display module** to output the final quotient

## 📌 Limitations

- ❌ **No remainder output** – Only the quotient is shown  
- ❌ **No division-by-zero handling** – The circuit does not protect against a `0000` divisor  
- 🔢 **Integer-only results** – No support for fractions or floating-point division  

## 🧪 Test Cases Included

The documentation includes a wide range of test cases:
- Perfect division (e.g. 12 ÷ 3 = 4)
- Division with remainder (e.g. 13 ÷ 2 = 6)
- Divisor larger than dividend (e.g. 3 ÷ 14 = 0)
- Maximum division (e.g. 15 ÷ 1 = 15)
- Division by zero behavior (undefined)

Simulation screenshots and logic diagrams are provided for validation.

##NOTE: This uses a gated clock, which is not advisable. During checking, instructor found an alternate solution with JK Flip Flops connected to the CKA of counter and CLK of Shift Register.
