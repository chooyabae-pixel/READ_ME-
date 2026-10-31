# READ_ME-

Project Title –  Customer Service Queue Management System 

Project Description – A few customers complained that the restaurant did not have a proper queueing system. When customers arrived at the same time, the staff could not tell who came first or last, and customers who arrived late were sometimes served before those who came earlier, which left people frustrated. To solve this, I created a system that registers customers and their concerns, places them in a waiting line, and serves them in the order they arrived (First-In, First-Out). The system can also display and sort the customer records and search for a customer. The program is written in Java, runs in the console, and does not use OOP like what is said in the capstone instructions. It uses static methods, loops, ArrayLists, and a Queue.


Use Cases and Features – 1. Register customers and help them with their concerns using an array list

                         2. Manage the waiting line correctly and by order following the queue 
                         
                         3. Two sorting algorithms was used: Bubble Sort and Selection Sort
                         
                         4. Let staff and workers search for the ID's and be able sort them 
                         
                         5. validate user input so that the user cannot use invalid instances
                         
                         6. Provide a menu that is easy to use and Conscise 
                         
Data Structure Explanation – For the customer records, I used five ArrayLists. They work together, so whatever is at the same index in each list belongs to the same customer. customerIds keeps the ID number, which starts at 1001. customerNames keeps the name, concerns keeps what the customer needs help with, serviceDurations keeps the estimated service time in minutes, and statuses tells us if the customer is still Waiting or already Served.

For example, if index 2 in customerNames is “Gojo satoru,” then index 2 in concerns, serviceDurations, and statuses is also Gojo’s information. To make sure the lists never get mixed up, I add a value to all five lists every time a customer is registered. When the records get sorted, the swapRecords method swaps the same two positions in all five lists, so each customer’s details stay together.

Queue

For the waiting line, I used a Queue<Integer> with a LinkedList. It follows FIFO (First-In, First-Out), meaning the customer who joined the line first is also the first one to be served.

The queue operations are used in different parts of the program. Enqueue uses add() in Option 1, when a customer is registered. Dequeue uses poll() in Option 2, when the next customer is served. Peek uses peek() in Option 3, which is the “Next in line” part. Display is a loop through the queue, also in Option 3, to show everyone who is waiting. Checking if the queue is empty uses isEmpty() in Options 2 and 3, so the program shows a message when nobody is waiting.

One important thing is that the queue stores the customers’ ID numbers and not their positions in the ArrayLists. Sorting moves the records to different positions, but the IDs in the queue stay in the same order. That means sorting never changes who gets served next.


Sorting Algorithm Explanation – I used 2 sorting algorithms 

1. Bubble sort so how this works in the program, It compares neighboring records and swaps them if they are out of order, repeating until no swaps are needed.
because It's purpose is to arrange the records from A to Z so a customer is easy to find. Why it is suitable?, A small restaurant has few  waiting customers, so a simple sort is enough.
Where it is used: Option 4, then choice 1.

2. Selection sort: How this works in the program, It finds the record with the shortest duration in the unsorted part and moves it to the next position, repeating until the list is sorted. Its Purpose is to arrange the records from the shortest to the longest service time. Why it is suitable?, It makes few swaps, which helps because each swap updates all five ArrayLists. Where it is used: Option 4, then choice 2.

How to Run the Program - Using INTELLIJ IDEA
1. Download the file from the repository
2. Open it in INTELLIJ IDEA
3. Open the Main java file
4. Click the green "Run" button or shift + f10
5. Test the Program. 


Note: I had a really hard time finishing this project. 
Extra Note: For the emojis I pasted in the menu I took it from this specific website, along with other emojis
https://emojidb.org/mcdo-emojis?utm_source=user_search
