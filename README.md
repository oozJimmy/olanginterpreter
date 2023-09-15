# olanginterpreter
Built in Programming Languages class at Oneonta, this is a C based interpreter for a very basic programming lanugage called OLang.

The syntax in EBNF follows:

<program>  -> Prog: Start <statements> Finish
<statements> -> <statement>{<statement>}
<statement>  ->   <printstatement>| <statusstatement> | <assign>
<printstatement> -> print identifier{, indentifier};
<statusstatement> -> status; 
<assign>-> identifier=<expression>;
<expression> -> <term> {(+ | - ) <term>}
<term> -> <factor> {(* | /) <factor>}
<factor> -> identifier | int_constant | '('<expression>')' 

<statement>  ->   <printstatement> | <statusstatement> | <assign> | <conditional>
<conditional> -> if (<relationalexpression>) do <assign>
<relationalexpression> -> <expression>(>|<|==|!=)<expression>
