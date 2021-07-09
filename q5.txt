List<BigInteger> a = new List<BigInteger>();
             
for (int b = 2; b < 400; b++) {
    BigInteger value = b;
    for (int e = 2; e < 50; e++) {
        value *= b;
 
        if (DigitSum(value) == b) {
            a.Add(value);            
        }
        if (a.Count > 50) break;                    
    }
    if (a.Count > 50) break;                    
}