**m:** Texto plano
**c:** Texto cifrado
**p:** Numero primo
**q:** Numero primo
**n:** Modulo
**e:** Llave publica
**tn:** 
**d:** Llave privada

n = p*q
tn = (p-1)*(q-1)
d = e mod inv tn ---> pow(e,-1,tn)
c = m ^ e mod n ---> pow(m,e,n) 
d = c^d mod n ---> pow(e,d,n)