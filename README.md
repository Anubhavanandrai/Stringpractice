# Stringpractice

Take input:
Scanner sc= new Scanner()
sc.next()---->Just a single word is read
sc.nextLine()-----> whole line is read
StringBuffer sc= new StringBuffer();

For substrings:
String s ="Anubhav";
s.substring(index starting , index ending)
starting index is inclusive and ending is non exclusive.

Split--means spliting a sentence of different basis
\s-->it is wrong because in java \ is refered as stop 
\\s--> means stop and the split on basis of \s


\\,-->on basis of comma
(" ") split on basis of space 
("") split on basis of letter/character becuase "" no space between it.
"[.\\s\\,]" if wants to implement multiple splitting rule.


Conversion	Method
int → String	String.valueOf(i)
String → int	Integer.parseInt(s)

From	To	How
String	StringBuffer	new StringBuffer(s)
StringBuffer	String	sb.toString()
int x =s.charAt(i) - 'a';  this will make character to integer
char an= (char)(z + 'a'); this is reverse


KMP Algorithm:

Only building LPS array is hard generally it has 3 rules which we needs to follow

while (i < n) {
            if (pattern.charAt(i) == pattern.charAt(len)) {
                len++;
                lps[i] = len;
                i++;
            } else {
                if (len != 0) {
                    len = lps[len - 1]; // fallback
                } else {
                    lps[i] = 0;
                    i++;
                }
            }
        }
remember this and you are good to go
