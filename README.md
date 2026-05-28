# CERIcompiler

A simple compiler.
From : Pascal-like imperative LL(k) langage
To : 64 bit 80x86 assembly langage (AT&T)

**Download the repository :**

> git clone git@framagit.org:jourlin/cericompiler.git

**Build the compiler and test it :**

> make test

**Have a look at the output :**

> gedit test.s

**Debug the executable :**

> ddd ./test

**Commit the new version :**

> git commit -a -m "What's new..."

**Send to your framagit :**

> git push -u origin master

**Get from your framagit :**

> git pull -u origin master

**This version Can handle :**

// Program := [DeclarationPart] StatementPart
// DeclarationPart := "[" Identifier {"," Identifier} "]"
// StatementPart := Statement {";" Statement} "."
// Statement := AssignementStatement
// AssignementStatement := Identifier ":=" Expression

// Expression := SimpleExpression [RelationalOperator SimpleExpression]
// SimpleExpression := Term {AdditiveOperator Term}
// Term := Factor {MultiplicativeOperator Factor}
// Factor := Number | Letter | "(" Expression ")"| "!" Factor
// Number := Digit{Digit}
// Identifier := Letter {(Letter|Digit)}

// AdditiveOperator := "+" | "-" | "||"
// MultiplicativeOperator := "*" | "/" | "%" | "&&"
// RelationalOperator := "==" | "!=" | "<" | ">" | "<=" | ">="  
// Digit := "0"|"1"|"2"|"3"|"4"|"5"|"6"|"7"|"8"|"9"
// Letter := "a"|...|"z"


## Travail personnel

J'ai implémenté les fonctionnalités suivantes dans compilateur.cpp :

### 1. Boucle FOR avec TO
Permet de répéter une instruction en comptant vers le haut.
Exemple (testfor.p) :
VAR a : INTEGER.
FOR a := 1 TO 5 DO
    DISPLAY a.
Résultat : 12345

### 2. Boucle FOR avec DOWNTO
Permet de répéter une instruction en comptant vers le bas.
Exemple (testdownto.p) :
VAR a : INTEGER.
FOR a := 5 DOWNTO 1 DO
    DISPLAY a.
Résultat : 54321

### 3. Boucle FOR avec STEP
Permet de définir le pas d'incrémentation ou de décrémentation.
Exemple (teststep.p) :
VAR a : INTEGER.
FOR a := 1 TO 10 STEP 2 DO
    DISPLAY a.
Résultat : 13579


