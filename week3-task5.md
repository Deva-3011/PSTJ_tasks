public static String addStrings(String num1, String num2) {
    int i = num1.length() - 1;
    int j = num2.length() - 1;
    int carry = 0;
    
    StringBuilder sb = new StringBuilder();
    
    while (i >= 0 || j >= 0 || carry != 0) {
        int d1 = (i >= 0) ? num1.charAt(i) - '0' : 0;
        int d2 = (j >= 0) ? num2.charAt(j) - '0' : 0;
        
        int sum = d1 + d2 + carry;
        carry = sum / 10;
        
        sb.append(sum % 10);
        
        i--;
        j--;
    }
    
    return sb.reverse().toString();
}

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/1ddacffe-6169-415e-a431-f436bf39c3ae" />
