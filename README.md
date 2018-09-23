# MA6628
# Prj01 (L01)
import numpy as np
x = np.arange(1000,1000000,1)
prime = []
for i in range(0, len(x)):
    for j in range(2,x[i]):
        if x[i]%j == 0:
            count += 1
    if count == 0:
        prime.append(x[i])
    else:    
        count = 0
pair = 0
twin=[]
for i in range(0,len(prime)-1):
    if (prime[i+1] - prime[i]) == 2:
        pair += 1
        twin.append(prime[i])
        twin.append(prime[i+1])
print('The number of twin primes that are bigger than one thousand but smaller than one million is %d'%(pair))
print('The biggest twin prime I could find are %d %d'%(twin[len(twin)-2],twin[len(twin)-1]))
