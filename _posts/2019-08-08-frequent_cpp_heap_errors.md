---
title: "자주나는 c++ 힙 에러"
categories:
  - Programming
tags:
  - debugging
  - c++
  - heap
---


* Invalid address specified to RtlValidateHeap
<br>
위의 에러메세지가 호출될 경우,
New와 Delete 혹은 malloc과 free과 잘못 Match 되어 있을 가능성이 높다.

Easy rule of thumb: Call free exactly once per every call to malloc/calloc. 
Same applies to delete+new and delete[]+new[].

[참고]
https://stackoverflow.com/questions/33613246/heap-error-invalid-address-specified-to-rtlvalidateheap
<br>
http://egloos.zum.com/saintrv/v/1560122

