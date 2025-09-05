Be careful to use view.getViewTreeObserver()

1)the object could be different from the one in onCreateView and onDestoryView in Fragment
![image](https://github.com/jt-huangk/Android/blob/master/img/31f7f886cf2226d777fa14cbaaa3b267.png)

After attch to window， the object is mAttachInfo.mTreeObserver; otherwise  is mFloatingTreeObserver

could use isAttachedToWindow() to check its status

2)you should check whether the ViewTreeObserver is still alive. Otherwise, you risk an exception or a memory leak.



