Practice Problems
-----------------------------------------------------

Please answer
the following problems to the best of your ability without any
outside help. You can stop working on a problem after you have worked
on it for about five minutes without solving it.

Problems
==============

.. parsonsprob:: p3dnd-front-back-nd
   :numbered: left
   :adaptive:
   :noindent:

   Create the function ``front_back(str, start, end)``.
   If ``str`` contains ``start`` at the beginning of the string and ``end`` at the end of the string return ``"start_end"``.
   If ``str`` contains ``start`` at the begining but does not contain ``"end"`` at the end then return  ``"start"``.  
   If ``str`` does not contain ``start`` at the begining but does contain ``"end"`` at the end then return  ``"end"``.  
   If ``str`` does not contain ``start`` at the beginning and does not contain ``end`` at the end then return ``None``.
   -----
   def front_back(str, start, end):
   =====
       last = len(end) * -1
   =====
       if str.startswith(start) and str[last:] == end:
   =====
           return "start_end"
   =====
       elif str.startswith(start):
   =====
           return "start"
   =====
       elif str[last:] == end:
   =====
           return "end" 
   =====
       return None

.. parsonsprob:: p3dnd-front-back-wd
   :numbered: left
   :adaptive:
   :noindent:

   Create the function ``front_back(str, start, end)``.
   If ``str`` contains ``start`` at the beginning of the string and ``end`` at the end of the string return ``"start_end"``.
   If ``str`` contains ``start`` at the begining but does not contain ``"end"`` at the end then return  ``"start"``.  
   If ``str`` does not contain ``start`` at the begining but does contain ``"end"`` at the end then return  ``"end"``.  
   If ``str`` does not contain ``start`` at the beginning and does not contain ``end`` at the end then return ``None``.
   -----
   def front_back(str, start, end):
   =====
       last = len(end) * -1
   =====
       last = len(end) #paired: Use negative indices to index from the end of the string
   =====
       if str.startswith(start) and str[last:] == end:
   =====
       if str.startswith(start) and str[last] == end: #paired: need to get a copy (slice) from last to the end
   =====
           return "start_end"
   =====
       elif str.startswith(start):
   =====
       elif str.starts(start): #paired: use startswith
   =====
           return "start"
   =====
       elif str[last:] == end:
   =====
           return "end" 
   =====
       return None

.. parsonsprob:: p3dnd-is-level-pnd
   :numbered: left
   :adaptive:
   :noindent:

   Create the function ``is_level(nums, value)`` that returns ``False``
   if any adjacent values in ``nums`` differ by more than ``value``.  For 
   example, ``is_level([1, 4, 5],2)`` returns ``False`` and ``is_level([1, 3, 5],2)`` returns ``True``.
   -----
   def is_level(nums, value):
   =====
       for i in range(len(nums)-1):
   =====
           curr = nums[i]
           next = nums[i+1]
   =====
           if abs(curr - next) > value:
   =====
               return False
   =====
       return True

.. parsonsprob:: p3dnd-is-level-wnd
   :numbered: left
   :adaptive:
   :noindent:

   Create the function ``is_level(nums, value)`` that returns ``False``
   if any adjacent values in ``nums`` differ by more than ``value``.  For 
   example, ``is_level([1, 4, 5],2)`` returns ``False`` and ``is_level([1, 3, 5],2)`` returns ``True``.
   -----
   def is_level(nums, value):
   =====
       for i in range(len(nums)-1):
   =====
       for i in range(len(nums)): #paired: need to use length minus one.
   =====
           curr = nums[i]
           next = nums[i+1]
   =====
           if abs(curr - next) > value:
   =====
           if abs(curr - next) >= value: #paired: need to use greater than
   =====
               return False
   =====
       return True