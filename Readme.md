**My ways to understand rxJava for Android**   
1. **Undertand the concept**   
  a. General concept- in rxJava,      
  b. Observable - the object that emits data.  
  c. Susbcriber - The object receives the data emitted by the Observable  
  d. Operators - Operators are used to manipulate the data emitted by the Observable before  it reaches the subscriber. There are many operators such as map, filter, merge and more.  
  e. Subscription- this object is obtained when a subscriber registers to the observable. It lets us to unregister the subscriber from the observable.
  e. Unscribe - we have to unregister the subscriber from the observable object. It is the best practice to stop the subscriber from receiving emitted item and  release resources (to prevent a possible memory leak).    

2. **Implement a step-by-step example**  
**Example Description:** Take look at the screenshot below. We want to display the text the user enters in the EditText field after clicking the button "Send".  
**RxJva step-by-step usage:**  When user clicks the button "Send", the text is displayed only if the text is not empty. Therefore:  
  1. Create an observable by binding the button to the RxJava    
  2. Use the operator map() to get the text from the EditText      
  4. Get Subscription  by registering subscriber to observable     
  5. Unscribe subscriber from observable
![Scheme](image/displayMessage.png)   
