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
   If ``str`` contains ``"start"`` at the beginning of the string return ``"start"``.
   if ``str`` contains ``"end"`` at the end of the string return ``"end"``.
   If ``str`` contains ``"start"`` at the begining and ``"end"`` at the end then return  ``"start_end"``.  
   In all other cases return ``str``.
   For example, ``front_back("Opening time", "Open", "noon")`` returns ``"start"`` and
   ``front_back("Afternoon", "Open", "noon")`` returns ``"end"`` and
   ``front_back("Open at noon", "Open", "noon")`` returns ``"start_end"`` and
   ``front_back("Closed", "Open", "noon")`` returns ``"Closed"``.
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
       return str

.. parsonsprob:: p3dnd-front-back-wd
   :numbered: left
   :adaptive:
   :noindent:

   Create the function ``front_back(str, start, end)``.
   If ``str`` contains ``"start"`` at the beginning of the string return ``"start"``.
   if ``str`` contains ``"end"`` at the end of the string return ``"end"``.
   If ``str`` contains ``"start"`` at the begining and ``"end"`` at the end then return  ``"start_end"``.  
   In all other cases return ``str``.
   For example, ``front_back("Opening time", "Open", "noon")`` returns ``"start"`` and
   ``front_back("Afternoon", "Open", "noon")`` returns ``"end"`` and
   ``front_back("Open at noon", "Open", "noon")`` returns ``"start_end"`` and
   ``front_back("Closed", "Open", "noon")`` returns ``"Closed"``.
   -----
   def front_back(str, start, end):
   =====
       last = len(end) * -1
   =====
       last = len(end) #paired: Use negative indices to index from the end of the string
   =====
       if str.startswith(start) and str[last:] == end:
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
       elif str[last] == end: #paired: use last: to get from last index to end
   =====
           return "end" 
   =====
       return str


.. parsonsprob:: p3dnd-in-back-nd
   :numbered: left
   :adaptive:
   :noindent:

   Create the function ``in_back(str, in, end)``.
   If ``str`` contains ``"in"`` return ``"in"``.
   if ``str`` contains ``"end"`` at the end of the string return ``"end"``.
   If ``str`` contains ``"in"`` and ``"end"`` at the end then return  ``"in_end"``.  
   In all other cases return ``str``.
   For example, ``in_back("We open on time", "open", "noon")`` returns ``"in"`` and
   ``in_back("Close at noon", "open", "noon")`` returns ``"end"`` and
   ``in_back("We open at noon", "open", "noon")`` returns ``"in_end"`` and
   ``in_back("Closed", "open", "noon")`` returns ``"Closed"``.
   -----
   def in_back(str, in, end):
   =====
       last = len(end) * -1
   =====
       if str.contains(in) and str[last:] == end:
   =====
           return "in_end"
   =====
       elif str.contains(in):
   =====
           return "in"
   =====
       elif str[last:] == end:
   =====
           return "end" 
   =====
       return str

.. parsonsprob:: p3dnd-in-back-wd
   :numbered: left
   :adaptive:
   :noindent:

   Create the function ``in_back(str, in, end)``.
   If ``str`` contains ``"in"`` return ``"in"``.
   if ``str`` contains ``"end"`` at the end of the string return ``"end"``.
   If ``str`` contains ``"in"`` and ``"end"`` at the end then return  ``"in_end"``.  
   In all other cases return ``str``.
   For example, ``in_back("We open on time", "open", "noon")`` returns ``"in"`` and
   ``in_back("Close at noon", "open", "noon")`` returns ``"end"`` and
   ``in_back("We open at noon", "open", "noon")`` returns ``"in_end"`` and
   ``in_back("Closed", "open", "noon")`` returns ``"Closed"``.
   -----
   def in_back(str, in, end):
   =====
       last = len(end) * -1
   =====
       last = len(end) #paired: Use negative indices to index from the end of the string
   =====
       if str.contains(in) and str[last:] == end:
   =====
       if str.contains(in) and str[last] == end: #paired: use last: to get from last to the end
   =====
           return "in_end"
   =====
       elif str.contains(in):
   =====
       elif str.has(in): #paired: use contains or find
   =====
           return "in"
   =====
       elif str[last:] == end:
   =====
           return "end" 
   =====
       return str


.. parsonsprob:: p3dnd-three-four-wd
   :numbered: left
   :adaptive:
   :noindent:

   Create the function ``three_four(nums)``.
   Return a new list with the same numbers in ``nums`` except
   replace numbers that are multiples of three with ``"three"``
   and multiples of four with ``"four"`` and 
   multiples of both three and four with ``"three_four"``.
   For example ``three-four([2, 3])`` returns ``[2, "three"]``
   and ``three-four([2, 8])`` returns ``[2, "four"]`` and
   ``three-four([6, 4, 5, 12])`` returns ``["three", "four", 5 "three_four"]``.
   -----
   def three_four(nums):
   =====
       out = []
   =====
       for num in nums:
   =====
           if num % 3 == 0 and num % 4 == 0:
   =====
           if num % 3 == 0 && num % 4 == 0: #paired: in Python use and not &&
   =====
               out.append("three_four")
   =====
           elif num % 3 == 0:
   =====
           elif num % 3 = 0: #paired: use == not = to test for equality
   =====
               out.append("three")
   =====
           elif num % 4 == 0:
   =====
               out.append("four")
   =====
           else:
   =====
               out.append(num)
   =====
           return out

.. parsonsprob:: p3dnd-three-four-nd
   :numbered: left
   :adaptive:
   :noindent:

   Create the function ``three_four(nums)``.
   Return a new list with the same numbers in ``nums`` except
   replace numbers that are multiples of three with ``"three"``
   and multiples of four with ``"four"`` and 
   multiples of both three and four with ``"three_four"``.
   For example ``three-four([2, 3])`` returns ``[2, "three"]``
   and ``three-four([2, 8])`` returns ``[2, "four"]`` and
   ``three-four([6, 4, 5, 12])`` returns ``["three", "four", 5 "three_four"]``.
   -----
   def three_four(nums):
   =====
       out = []
   =====
       for num in nums:
   =====
           if num % 3 == 0 and num % 4 == 0:
   =====
               out.append("three_four")
   =====
           elif num % 3 == 0:
   =====
               out.append("three")
   =====
           elif num % 4 == 0:
   =====
               out.append("four")
   =====
           else:
   =====
               out.append(num)
   =====
           return out

.. parsonsprob:: p3dnd-is-level-nd
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

.. parsonsprob:: p3dnd-is-level-wd
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

.. parsonsprob:: p3dnd-total-eight-nine-nd
   :numbered: left
   :adaptive:
   :noindent:

   Create the ``total89(nums)`` function below that takes a list and returns 
   the total of the items in ``nums`` except for all the numbers 
   between an 8 and a 9 (inclusive). For example, total89([1,2]) 
   should return 3 and total89([2, 8, 3, 9, 2]) should return 4.
   -----
   def total89(nums):
   =====
       sum = 0
       found8 = False
   =====
       for num in nums:
   =====
           if num == 8:
   =====
               found8 = True
   =====
           elif found8 and num == 9:
   =====
               found8 = False
   =====
           elif found8:
   =====
               continue
   =====
           else:
   =====
               sum += num
   =====
       return sum

.. parsonsprob:: p3dnd-total-eight-nine-wd
   :numbered: left
   :adaptive:
   :noindent:

   Create the ``total89(nums)`` function below that takes a list and returns 
   the total of the items in ``nums`` except for all the numbers 
   between an 8 and a 9 (inclusive). For example, total89([1,2]) 
   should return 3 and total89([2, 8, 3, 9, 2]) should return 4.
   -----
   def total89(nums):
   =====
       sum = 0
       found8 = False
   =====
       for num in nums:
   =====
           if num == 8:
   =====
               found8 = True
   =====
           elif found8 and num == 9:
   =====
           elif found8 && num == 9: #paired: use and not && in Python
   =====
               found8 = False
   =====
           elif found8:
   =====
               continue
   =====
               break :paired: use continue
   =====
           else:
   =====
               sum += num
   =====
       return sum

    