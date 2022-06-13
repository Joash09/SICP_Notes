# About

Collection of notes and exercise attempts from working through Structure and Interpretation of Computer Programs (SICP), a textbook by professors Harold Abelson and Gerald Jay Sussman with Julie Sussman. It is a renowned book within programming circles on the internet, so I thought it would be worth seeing what the fuss was about.

📓 You can find a copy of SICP provided by MIT [here](https://web.mit.edu/6.001/6.037/sicp.pdf)
✏ The notes and attempts are done in with Org mode in [Doom Emacs](https://github.com/doomemacs/doomemacs).
🎾 Code snippets are written in [Racket](https://racket-lang.org/), a dialect of Lisp

# 🌟 Highlights

- Chapter 1: 
    * models for computation:
      - substitution
      - applicative vs normal order
    * different types of recursion: linear (stack grows) and iterative (keeps track of s state) recursion
    * tree recursion (procedure makes two recursive calls which is combined)
    * procedures can be used as arguments
    * procedures can be used as return values
      - accomplished using the lambda keyword
    * In Lisp, procedures are treated as first class elements meaning:
      - can be named by variables
      - passed as arugments
      - used as return values
      - included in data structures
    
- Chapter 2: 
    * What is data? 
      - It is not enough to say data is whatever is implemented with constructors and selectors (i.e. procedures)
      - Data must also include conditions that must be fulfilled in order to be a valid representation (analogous to business logic?)
    * data as functions
      - introduction to lambda calculus 
    * key to organizing programs is to clearly represent the signal flow structure
    * higher order functions: reduce, accumulate, fold
