# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:

Create a ChatRoom class (mediator) and two users (colleagues) who send and receive messages through it. No direct communication allowed. (Mediator Pattern)


## AIM:

To write a Java program that demonstrates the Mediator Design Pattern by enabling message exchange between users through a chat room.
## ALGORITHM :
1.Start the program and create a ChatRoom class with a method to display messages.

2.Create a User class that stores the user name and a reference to the chat room.

3.Implement a method in User to send messages through the chat room.

4.Read the names of two users from the input.

5.Create a ChatRoom object and two User objects linked to it.

6.Read the number of messages and for each message, read sender, receiver, and message content.

7.Use the sender object to send the message to the receiver via the chat room.

7.Display all messages in the format "sender to receiver: message".

8.End the program.


## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: VIKASH A R
RegisterNumber:  212222040179
*/
```

## SOURCE CODE:

```
import java.util.*;

class ChatRoom {
    public void showMessage(String sender, String receiver, String message) {
        System.out.println(sender + " to " + receiver + ": " + message);
    }
}

class User {
    private String name;
    private ChatRoom chatRoom;

    public User(String name, ChatRoom chatRoom) {
        this.name = name;
        this.chatRoom = chatRoom;
    }

    public String getName() {
        return name;
    }

    public void sendMessage(User receiver, String message) {
        chatRoom.showMessage(this.name, receiver.getName(), message);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String user1Name = sc.nextLine().trim();
        String user2Name = sc.nextLine().trim();
        int n = Integer.parseInt(sc.nextLine().trim());

        ChatRoom chatRoom = new ChatRoom();
        User user1 = new User(user1Name, chatRoom);
        User user2 = new User(user2Name, chatRoom);

        for (int i = 0; i < n; i++) {
            String senderName = sc.nextLine().trim();
            String receiverName = sc.nextLine().trim();
            String message = sc.nextLine();

            if (senderName.equals(user1.getName()) && receiverName.equals(user2.getName())) {
                user1.sendMessage(user2, message);
            } else if (senderName.equals(user2.getName()) && receiverName.equals(user1.getName())) {
                user2.sendMessage(user1, message);
            }
        }

    }
}

```





## OUTPUT:

<img width="1074" height="767" alt="image" src="https://github.com/user-attachments/assets/0954ebf9-cd86-4f20-a233-445b21d92945" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
