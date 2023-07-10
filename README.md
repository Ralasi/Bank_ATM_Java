# Bank_ATM_Java

The Java Bank ATM code showcases multi-threading and synchronization concepts. It implements a multi-threaded environment where multiple account holders can perform withdrawals concurrently. The synchronized method ensures thread safety, preventing simultaneous access to shared resources and potential data conflicts. The use of threads improves efficiency and responsiveness by allowing parallel execution of transactions. Additionally, the code demonstrates the handling of concurrency issues, such as preventing overdrawn accounts. Overall, it demonstrates proficiency in multi-threading, synchronization, and concurrent programming in Java, highlighting the ability to design and implement efficient and secure multi-threaded applications.

Sample Output
![Screenshot (275)](https://github.com/Ralasi/Bank_ATM_Java/assets/128724283/1cfd9fcd-ee95-4c2d-a12d-7008ed1892eb)

This section defines the Account class, which represents a bank account. It has a private instance variable balance that holds the current balance of the account. The class provides two methods: getBalance() returns the current balance, and withdraw(int amount) deducts the specified amount from the balance.

In this section, the ClientTest class is defined. It creates an instance of the Account class and an instance of the AccountHolder class, passing the Account object as a parameter. Two threads t1 and t2 are created, both using the same AccountHolder object. The threads are named "Ralasi" and "Joya" respectively. Finally, the threads are started by calling their start() method.

This section defines the AccountHolder class, which implements the Runnable interface to be executed as a thread. It has a reference to the Account object that it will be operating on.

The run() method is the entry point of the thread. In this case, it loops four times and calls the makeWithdrawal(int withdrawAmount) method each time, passing 2000 as the withdrawal amount. If the account balance becomes negative after the withdrawal, it prints a message indicating that the account is overdrawn.

The makeWithdrawal(int withdrawAmount) method is declared as synchronized, which means that only one thread can execute this method at a time. It first checks if the account balance is sufficient to cover the withdrawal amount. If so, it prints a message indicating the withdrawal is in progress, sleeps for 3 seconds (to simulate some processing time), updates the account balance by calling account.withdraw(withdrawAmount), and prints a completion message. If the balance is insufficient, it prints a message indicating that there are not enough funds in the account.
