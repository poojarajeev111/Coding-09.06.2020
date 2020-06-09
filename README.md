
def isPalindrome(a):  
    flag = True;   
    for i in range(0, len(a)//2):  
        if(a[i] != a[len(a) -i-1]):  
            flag = False;  
            break;  
    return flag;  
      
string = "Wow you own kayak";  
words = [];  
word = "";  
count = 0;  
string = string.lower();  
string = string + " ";  
   
for i in range(0, len(string)):  
    if(string[i] != ' '):  
        word = word + string[i];  
    else:  
        words.append(word);  
        word = "";  

for i in range(0, len(words)):  
    if(isPalindrome(words[i])):  
          
        count = count + 1;  
        if(count == 1):
            smallPalin = bigPalin = words[i];  
              
        else:  
            
            if(len(smallPalin) > len(words[i])):  
                smallPalin = words[i];   
              
            if(len(bigPalin) < len(words[i])):  
                bigPalin = words[i];  
   
if(count == 0):  
    print("No palindrome is present in the given string");  
else:  
    print("Smallest palindromic word: " + smallPalin);  
    print("Biggest palindromic word: " + bigPalin);  
