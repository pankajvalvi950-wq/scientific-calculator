# SciCalc 991 – Online Scientific Calculator

A Casio fx-991ES style scientific calculator that runs in the browser. It is built with plain HTML, CSS and JavaScript, with no libraries and no backend.

**Live demo:** https://pankajvalvi950-wq.github.io/scientific-calculator/

## Features

- Basic operations (+ − × ÷), brackets and implicit multiplication (`2π`, `3(4+1)`)
- Trigonometry: sin, cos, tan, their inverses (SHIFT) and hyperbolic versions (hyp)
- log, ln, 10ˣ, eˣ, x², x³, xʸ, √, ³√, x⁻¹, x!, nPr, nCr, Abs, π, e, Ran#
- DEG / RAD / GRAD angle modes
- ×10ˣ, Ans, RCL, STO, M+ and M−
- S⇔D key to show a decimal answer as a fraction
- Editable expression with a cursor (◀ ▶), DEL and AC
- `Math ERROR` and `Syntax ERROR` messages
- Calculation history (click an entry to reuse it)
- Keyboard support (digits, + − * / ^ ( ), Enter, Backspace, Esc, arrow keys)
- **BASE-N mode (number system converter):** press the BASE key and the keys change to DEC, HEX, BIN, OCT, A–F and logic operations (and, or, xor, xnor, Not, Neg). The result is shown in the chosen base and the other bases appear below it. It works as a 32-bit calculator like a real Casio.

## How to use

1. Open the live demo link above.
2. Use the on-screen keys or your keyboard.
3. Press **SHIFT** to use the yellow functions.
4. Press **BASE** for number-system conversion, and press it again to return to normal mode.

## How it works

The expression is stored as a list of tokens. When you press `=`:

1. A **lexer** converts the tokens into numbers and operators.
2. A **recursive descent parser** evaluates them in the correct order of precedence:
   `+ −` → `× ÷` → `nPr nCr` → `^` → postfix (`!`, `x²`, `x³`, `x⁻¹`).
3. In BASE-N mode, logic operators (`and`, `or`, `xor`, `xnor`) are added with the lowest precedence, and the result is kept in 32-bit range.
4. The result is rounded to 10 significant digits to avoid floating-point errors such as `0.1 + 0.2`.

`eval()` is not used anywhere.

## Technologies

HTML5, CSS3, JavaScript (ES6). Hosted on GitHub Pages.

## Run locally

Download `index.html` and open it in any browser. No installation is needed.

## Contact detail :
- Mail : pankajvalvi@proton.me
