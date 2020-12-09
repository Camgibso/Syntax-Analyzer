Problem

Develop a lexical analyzer in C or C++ that can identify lexemes and tokens found in a source code file provided
by the user. 

Once the analyzer has identified the lexemes of the language and matched them to a token group, the program should print each lexeme / token pair to the screen.

The source code file provided by the user will be written in a new programming language called “DanC” and is
based upon the following grammar (in BNF):

P ::= S
S ::= V:=E | read(V) | write(V) | while C do S od | S;S
C ::= E < E | E > E | E = E | E <> E | E <= E | E >= E
E ::= T | E + T | E - T
T ::= F | T * F | T / F
F ::= (E) | N | V
V ::= a | b | … | y | z | aV | bV | … | yV | zV
N ::= 0 | 1 | … | 8 | 9 | 0N | 1N | … | 8N | 9N


Your analyzer should accept the source code file as a required command line argument and display an
appropriate error message if the argument is not provided or the file does not exist. The command to run your
application will look something like this:

Form: danc_analyzer <path_to_source_file>
Example: danc_analyzer test_file.danc


Lexeme formation is guided using the BNF rules / grammar above. Your application should output each lexeme
and its associated token. Invalid lexemes should output UNKNOWN as their token group. The following token
names should be used to identify each valid lexeme:

Lexeme Token 		Lexeme Token 		Lexeme Token
:= ASSIGN_OP 		+ ADD_OP 		do KEY_DO
< LESSER_OP 		- SUB_OP 		od KEY_OD
> GREATER_OP 		* MULT_OP		<variable name> IDENT
= EQUAL_OP 		/ DIV_OP 		<integer> INT_LIT
<> NEQUAL_OP 		read KEY_READ 		( LEFT_PAREN
<= LEQUAL_OP 		write KEY_WRITE 	) RIGHT_PAREN
>= GEQUAL_OP 		while KEY_WHILE 	; SEMICOLON
