# CS210 Programming Assignment
## Monopoly Board Simulator (Spring 2026)

---

## How to Build and Run
### Build

- `g++ -std=c++17 monopoly_board.cpp`
- g++ monopoly_board.cpp -o monopoly_board

### Run
- `./monopoly_board`

---

## Data Structures
- Linked List
  - A linked list was used to construct the monopoly board.
  - A linked list is nodes linked up together using pointers allowing for efficient insertion and deletion without shifting elements.
- Vector
  - A vector was used to house all the MonopolySpace objects before insertion.
  - A vector is like a dynamic array, can house elements and will automatically resize itself when elements are added or removed.

---

## Functions
- Class MonopolySpace
  - isEqual: Compares two MonopolySpaces to check if they're equal. Returns true if they are false if not.
  - print: Prints the attributes of the MonopolySpace. Prints property name, color, value, and rent in that order
- Class CircularLinkedList
  - addSpace: Adds a new MonopolySpace to the end of the board.
  - addMany: Adds multiple Monopoly spaces at once. Uses the addSpace function to add spaces. Has checks to see if the list is full to prevent overflow.
  - movePlayer: Traverses the player through the linked list. Moves a certain number of steps. Checks if player passes Go space. Has checks if the list is empty or if the steps in less than 0.
  - getPassGoCount: Returns the amount of times the player passes Go.
  - printFromPlayer: Prints a count number of spaces from player. Has checks if count or node count is 0.
  - printBoardOnce: Prints entire board once. If board is empty doesn't print anything.
  -mirrorBoard: Reverses the board. So say we have space A -> B -> C, with the player at B, the board is now C -> B -> A, with the next space being A not C. The board still maintains the circular structure.
  - countSpaces: Counts the number of spaces on the board.
  - clear: Clears the board. Deleting all nodes correctly.
  

---
## Traversal and Movement Logic
Traversing through a circular linked list involves visiting each node in the linked list, there is no jumping around nodes unless the position is known.
In this case, the only known positions are headNode, tailNode, and playernode.
Traversing the board changes depending on the current state of the board.
The board, a circular linked list, has an explicit 40-space limit. Attempting to add spaces beyond 40 will not work.
Traversing above 40 however will work as the board is circular. Say you're on the very last space, 
doing playerNode = playerNode->nextNode will complete an entire cycle on the board, sending the player back to the headNode which is Go.
Traversing the middle of the board works like an ordinary singly linked list. Only being able to move forward.
Reversing the board doesn't change the movement logic significantly, you still visit each node, it just changes which node is next.
The player still moves forward but now forward is now the previous node from before the board was reversed.
Furthermore, the head and tail node are now swapped essentially, with the new tail being the oldHead and vice versa.
The key point of the board being a circular linked list is that there is no end to the board. With their being no end to the board,
the headNode and tailNode are very important to maintain the circular structure of the board as the tail has to point to the head.


---




