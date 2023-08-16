# What's Message Visibility Timeout?
---

* After a message is polled by a consumer, it becomes **invisible to other consumers**. After the message visibility timeout is over, **the message is “visible” in SQS**
	* By default is **30 seconds**, but can be customized (**1 second - 12 hours**)

![[Pasted image 20230816204739.png]]

# Customized Strategy
---

* If visibility timeout is too low (seconds), we may **get duplicates** since a message is not processed within the visibility timeout
* If visibility timeout is too high (hours), and consumer crashes, **re-processing will take time**