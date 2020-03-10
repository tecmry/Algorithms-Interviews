# 链表中倒数第K个节点

* **题目描述**

  输入一个链表，输出该链表中倒数第k个结点。

* **Code**

```java
/*
public class ListNode {
    int val;
    ListNode next = null;

    ListNode(int val) {
        this.val = val;
    }
}*/
import java.util.ArrayList;
import java.util.List;
public class Solution {
    public ListNode FindKthToTail(ListNode head,int k ){
          ListNode p1 = head;
          ListNode p2 = head;
          if(k<=0){return null;}
          if(head==null){
              return null;
          }
          for(int i=0;i<k-1;i++){
              if(p1.next==null){return null;}
              p1 = p1.next;
          }
          while(p1.next!=null){
              p1 = p1.next;
              p2 = p2.next;
          }
        return p2;
    }
}
```

