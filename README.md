# python-
def happynumber(num, counter, the_list):
    N = adder(num); 
    print ("value of n is {}".format(N));
    if counter == 0:  #THIS IS ADDED
        the_list.append(num); #THIS IS ADDED
    if N == 1: 
        print ("In just {} tries we found that {} is a happy number.".format(counter, number))
        print (num);
    else: 
        counter += 1
        if counter < 11:
            print (counter) 
            happynumber(N, counter, the_list)
        else:
            print ("it took us {} tries and found that the number {} is not a happy number".format(counter, number))
            the_list.pop(); #THIS IS ADDED
            return False       

counter = 0;

happynumber_list = []; #THIS IS ADDED
for i in range(0,100): 
    number = i
    happynumber (number, counter, happynumber_list)
