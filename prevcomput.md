# COCOMO = Constructive Cost Model

* Barry Boehm 1981
* predicts cost, effort & schedule
* Types
	* Organic 
		* Small team with nominal relevant experience
		* Well understood & already solved problem
	* Semi detached
		* Team size, experience & knowledge vary between organic & embedded
	* Embedded
		* Highest complexity, creativity and experience
		* Larger team size with greater experience


## Basic model

Effort  = a * KLOC^b * Person-months
Time = c * Effort^d
Persons = Effort / Time


F = x'y + xyz' 
F' = (x'y)'.(xyz')'
   = (x.y').(x'.y'.z)
   = 0



(((a+b)'+a)' + ((a+b)'+b)')'

((a+b)'+a)'
= a'b' nor a
= (a'.b')'.a'
= (a + b).a'
X= a'.b 

(a+b)' nor b
= a'.b' nor b
= (a'.b')'.b'
= (a + b ).b'
Y= a.b' 

X nor Y
= a'.b nor a.b'
= (a'.b)'.(a.b')'
= (a+b').(a'+b)
= a.a' + a'.b' + b.a + b.b'
= a'.b' + b.a





