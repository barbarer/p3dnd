Practice Problems
-----------------------------------------------------

Please answer
the following problems to the best of your ability without any
outside help. You can stop working on a problem after you have worked
on it for about five minutes without solving it.

Problems
==============

.. parsonsprob:: p3dnd-has22_nd
       :adaptive:
       :numbered: left

       Create a function ``has22(nums)`` that takes a list of numbers, ``nums`` 
       and returns ``True`` if there are at least two items in the list that are adjacent and both equal to ``2``, otherwise return ``False``. 

       .. table:: 
          :name: p3dnd-has22_nd-table
          :class: longtable
          :align: left
          :width: 80%

          +----------------------------------------------------+-----------------+
          | Example Input                                      | Expected Output |
          +====================================================+=================+
          | ``has22([1, 2, 2])``                               | ``True``        |
          +----------------------------------------------------+-----------------+
          | ``has22([2, 1, 2])``                               | ``False``       |
          +----------------------------------------------------+-----------------+
          | ``has22([2, 2, 8])``                               | ``True``        |
          +----------------------------------------------------+-----------------+
          | ``has22([3, 3, 5])``                               | ``False``       |
          +----------------------------------------------------+-----------------+
       -----
       def has22(nums):
       =====
           for i in range(len(nums) - 1):
       =====
               if nums[i] == 2 and nums[i + 1] == 2:
       =====
                   return True
       =====
           return False

.. parsonsprob:: p3dnd-has22_wd
       :adaptive:
       :numbered: left

       Create a function ``has22(nums)`` that takes a list of numbers, ``nums`` 
       and returns ``True`` if there are at least two items in the list that are adjacent and both equal to ``2``, otherwise return ``False``. 

       .. table:: 
          :name: p3dnd-has22-wd-table
          :class: longtable
          :align: left
          :width: 80%

          +----------------------------------------------------+-----------------+
          | Example Input                                      | Expected Output |
          +====================================================+=================+
          | ``has22([1, 2, 2])``                               | ``True``        |
          +----------------------------------------------------+-----------------+
          | ``has22([2, 1, 2])``                               | ``False``       |
          +----------------------------------------------------+-----------------+
          | ``has22([2, 2, 8])``                               | ``True``        |
          +----------------------------------------------------+-----------------+
          | ``has22([3, 3, 5])``                               | ``False``       |
          +----------------------------------------------------+-----------------+
       -----
       def has22(nums):
       =====
           for i in range(len(nums) - 1):
       =====
           for i in range(len(nums)): #paired: must stop before end to not go out of bounds if comparing current and next value
       =====
               if nums[i] == 2 and nums[i + 1] == 2:
       =====
               if nums[i] == nums[i+1]: #paired: must check if both equal 2 as well
       =====
                   return True
       =====
           return False

.. parsonsprob:: p3dnd-sum13-nd
   :adaptive:
   :numbered: left

   Create a function ``sum13(nums)`` that takes a list of numbers, ``nums`` and 
   returns the sum of the numbers in the list. However, the number 13 is 
   very unlucky, so do not add it or the number that comes immediately 
   after a 13 to the sum.    Return ``0`` if ``nums`` is the empty list. 
   
    .. table:: 
          :name: p3dnd-sum13-nd-table
          :class: longtable
          :align: left
          :width: 80%

          +----------------------------------------------------+-----------------+
          | Example Input                                      | Expected Output |
          +====================================================+=================+
          | ``sum13([13,1,2])``                                | ``2``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([1,13])``                                  | ``1``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([4, 13, 8])``                              | ``4``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([13, 1, 13, 3, 2])``                       | ``2``           |
          +----------------------------------------------------+-----------------+ 
   -----
   def sum_13(nums):
   =====
       total = 0
       found_13 = False
   =====
       for num in nums:
   =====
           if found_13:
   =====
               found_13 = False
   =====
           elif num == 13:
   =====
               found_13 = True
   =====
           else:
   =====
               total += num
   =====
       return total

.. parsonsprob:: p3dnd-sum13-wd
   :adaptive:
   :numbered: left

   Create a function ``sum13(nums)`` that takes a list of numbers, ``nums`` and 
   returns the sum of the numbers in the list. However, the number 13 is 
   very unlucky, so do not add it or the number that comes immediately 
   after a 13 to the sum.    Return ``0`` if ``nums`` is the empty list. 
   
    .. table:: 
          :name: p3dnd-sum13-wd-table
          :class: longtable
          :align: left
          :width: 80%

          +----------------------------------------------------+-----------------+
          | Example Input                                      | Expected Output |
          +====================================================+=================+
          | ``sum13([13,1,2])``                                | ``2``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([1,13])``                                  | ``1``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([4, 13, 8])``                              | ``4``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([13, 1, 13, 3, 2])``                       | ``2``           |
          +----------------------------------------------------+-----------------+ 
   -----
   def sum_13(nums):
   =====
       total = 0
       found_13 = False
   =====
       total = 0
       found_13 = True #paired: You haven't found a 13 yet so this found_13 should be False
   =====
       for num in nums:
   =====
           if found_13:
   =====
               found_13 = False
   =====
           elif num == 13:
   =====
           elif num = 13: #paired: Use == and not = to test if a variable equals a value
   =====
               found_13 = True
   =====
           else:
   =====
               total += num
   =====
       return total
   =====
       return Total #paired: Case matters and Total is not defined

.. parsonsprob:: p3dnd-front-back-nd
   :numbered: left
   :adaptive:

   Create the function ``front_back(str, start, end)`` that takes three strings and returns 
   a string based on the following conditions.

   * If ``str`` contains ``start`` at the beginning of the string return ``"s"``.
   * if ``str`` contains ``end`` at the end of the string return ``"e"``.
   * If ``str`` contains ``start`` at the begining and ``end`` at the end then return  ``"s_e"``.  
   * Otherwise return ``"n"``.
  
   .. table:: 
      :name: p3dnd-front-back-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      | ``front_back("Opening time", "Open", "noon")``     | ``"s"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("Afternoon", "Open", "noon")``        | ``"e"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("Open at noon", "Open", "noon")``     | ``"s_e"``       |
      +----------------------------------------------------+-----------------+
      | ``front_back("Closed", "Open", "noon")``           | ``"n"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("It is noon now", "open", "noon")``   | ``"n"``         |
      +----------------------------------------------------+-----------------+
   -----
   def front_back(str, start, end):
   =====
       last = len(end) * -1
   =====
       if str.startswith(start) and str[last:] == end:
   =====
           return "s_e"
   =====
       elif str.startswith(start):
   =====
           return "s"
   =====
       elif str[last:] == end:
   =====
           return "e" 
   =====
       return "n"

.. parsonsprob:: p3dnd-front-back-wd
   :numbered: left
   :adaptive:

   Create the function ``front_back(str, start, end)`` that takes three strings and returns 
   a string based on the following conditions.

   * If ``str`` contains ``start`` at the beginning of the string return ``"s"``.
   * if ``str`` contains ``end`` at the end of the string return ``"e"``.
   * If ``str`` contains ``start`` at the begining and ``end`` at the end then return  ``"s_e"``.  
   * Otherwise return ``"n"``.
  
   .. table:: 
      :name: p3dnd-front-back-wd-table
      :widths: 70 30
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      | ``front_back("Opening time", "Open", "noon")``     | ``"s"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("Afternoon", "Open", "noon")``        | ``"e"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("Open at noon", "Open", "noon")``     | ``"s_e"``       |
      +----------------------------------------------------+-----------------+
      | ``front_back("Closed", "Open", "noon")``           | ``"n"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("It is noon now", "open", "noon")``   | ``"n"``         |
      +----------------------------------------------------+-----------------+
   -----
   def front_back(str, start, end):
   =====
       last = len(end) * -1
   =====
       last = len(end) #paired: Use negative indices to index from the end of the string
   =====
       if str.startswith(start) and str[last:] == end:
   =====
           return "s_e"
   =====
       elif str.startswith(start):
   =====
       elif str.starts(start): #paired: use startswith
   =====
           return "s"
   =====
       elif str[last:] == end:
   =====
       elif str[last] == end: #paired: use last: to get from last index to end
   =====
           return "e" 
   =====
       return "n"


.. parsonsprob:: p3dnd-in-back-nd
   :numbered: left
   :adaptive:

   Create the function ``in_back(str, in, end)`` that takes three strings and returns 
   a string based on the following conditions.

   * If ``str`` contains ``in`` return ``"i"``.
   * if ``str`` contains ``end`` at the end of the string return ``"e"``.
   * If ``str`` contains ``in`` and ``end`` at the end then return  ``"i_e"``.  
   * Otherwise return ``"n"``.

   .. table:: 
      :name: p3dnd-in-back-nd
      :widths: 70 30
      :class: longtable
      :align: left
      :width: 80%

      +--------------------------------------------------+-----------------+
      | Example Input                                    | Expected Output |
      +==================================================+=================+
      |``in_back("We open on time", "open", "noon")``    | ``"i"``         |
      +--------------------------------------------------+-----------------+
      | ``in_back("Close at noon", "open", "noon")``     | ``"e"``         |
      +--------------------------------------------------+-----------------+
      | ``in_back("We open at noon", "open", "noon")``   | ``"i_e"``       |
      +--------------------------------------------------+-----------------+
      | ``in_back("Closed", "open", "noon")``            | ``"n"``         |
      +--------------------------------------------------+-----------------+
      | ``in_back("It is noon now", "open", "noon")``    | ``"n"``         |
      +--------------------------------------------------+-----------------+
   -----
   def in_back(str, in, end):
   =====
       last = len(end) * -1
   =====
       if str.contains(in) and str[last:] == end:
   =====
           return "i_e"
   =====
       elif str.contains(in):
   =====
           return "i"
   =====
       elif str[last:] == end:
   =====
           return "e" 
   =====
       return "n"

.. parsonsprob:: p3dnd-in-back-wd
   :numbered: left
   :adaptive:

   Create the function ``in_back(str, in, end)`` that takes three strings and returns 
   a string based on the following conditions.

   * If ``str`` contains ``in`` return ``"i"``.
   * if ``str`` contains ``end`` at the end of the string return ``"e"``.
   * If ``str`` contains ``in`` and ``"end"`` at the end then return  ``"i_e"``.  
   * Otherwise return ``"n"``.

   .. table:: 
      :name: p3dnd-in-back-wd
      :widths: 70 30
      :class: longtable
      :align: left
      :width: 80%

      +--------------------------------------------------+-----------------+
      | Example Input                                    | Expected Output |
      +==================================================+=================+
      |``in_back("We open on time", "open", "noon")``    | ``"i"``         |
      +--------------------------------------------------+-----------------+
      | ``in_back("Close at noon", "open", "noon")``     | ``"e"``         |
      +--------------------------------------------------+-----------------+
      | ``in_back("We open at noon", "open", "noon")``   | ``"i_e"``       |
      +--------------------------------------------------+-----------------+
      | ``in_back("Closed", "open", "noon")``            | ``"n"``         |
      +--------------------------------------------------+-----------------+
      | ``in_back("It is noon now", "open", "noon")``    | ``"n"``         |
      +--------------------------------------------------+-----------------+
       
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
           return "i_e"
   =====
       elif str.contains(in):
   =====
       elif str.has(in): #paired: use contains or find
   =====
           return "i"
   =====
       elif str[last:] == end:
   =====
           return "e" 
   =====
       return "n"


.. parsonsprob:: p3dnd-three-four-wd
   :numbered: left
   :adaptive:

   Create the function ``three_four(nums)`` that takes a list of numbers, ``nums``.
   Return a new list with the same numbers in ``nums`` except 
   with the following changes.

   * replace numbers that are multiples of three with ``"three"``
   * replace numbers that are multiples of four with ``"four"`` and 
   * replace numbers that are multiples of both three and four with ``"three_four"``.

   .. table:: 
      :name: p3dnd-three-four-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``three-four([2, 3])``            | ``[2, "three"]``                      |
      +----------------------------------+---------------------------------------+
      | ``three-four([2, 8])``           | ``[2, "four"]``                       |
      +----------------------------------+---------------------------------------+
      | ``three-four([6, 4, 5, 12])``    | ``["three", "four", 5 "three_four"]`` |
      +----------------------------------+---------------------------------------+
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

   Create the function ``three_four(nums)`` that takes a list of numbers, ``nums``.
   Return a new list with the same numbers in ``nums`` except 
   with the following changes.

   * replace numbers that are multiples of three with ``"three"``
   * replace numbers that are multiples of four with ``"four"`` and 
   * replace numbers that are multiples of both three and four with ``"three_four"``.

   .. table:: 
      :name: p3dnd-three-four-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``three-four([2, 3])``            | ``[2, "three"]``                      |
      +----------------------------------+---------------------------------------+
      | ``three-four([2, 8])``           | ``[2, "four"]``                       |
      +----------------------------------+---------------------------------------+
      | ``three-four([6, 4, 5, 12])``    | ``["three", "four", 5 "three_four"]`` |
      +----------------------------------+---------------------------------------+
 
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

   Create the function ``is_level(nums, value)`` that takes a list of numbers, ``nums``, and a number ``value``.
   
   * It should return ``False`` if any adjacent numbers in ``nums`` differ by more than ``value`` 
   * Otherwise it should return ``True``

   .. table:: 
      :name: p3dnd-is-level-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``is_level([1, 4, 5], 2)``        | ``False``                             |
      +----------------------------------+---------------------------------------+
      |``is_level([9, 4, 6], 3)``        | ``False``                             |
      +----------------------------------+---------------------------------------+
      |``is_level([1, 3, 5], 2)``        | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``is_level([5, 2, 4], 3)``        | ``True``                              |
      +----------------------------------+---------------------------------------+
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

   Create the function ``is_level(nums, value)`` that takes a list of numbers, ``nums``, and a number ``value``.
   
   * It should return ``False`` if any adjacent numbers in ``nums`` differ by more than ``value`` 
   * Otherwise it should return ``True``

   .. table:: 
      :name: p3dnd-is-level-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``is_level([1, 4, 5], 2)``        | ``False``                             |
      +----------------------------------+---------------------------------------+
      |``is_level([9, 4, 6], 3)``        | ``False``                             |
      +----------------------------------+---------------------------------------+
      |``is_level([1, 3, 5], 2)``        | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``is_level([5, 2, 4], 3)``        | ``True``                              |
      +----------------------------------+---------------------------------------+
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

   Create the ``total89(nums)`` function below that takes a list of numbers, 
   ``nums``, and returns the total of the numbers in ``nums`` except for all numbers 
   between an 8 and a 9 (inclusive). 

   .. table:: 
      :name: p3dnd-total-eight-nine-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``total89([1,2])``                | ``3``                                 |
      +----------------------------------+---------------------------------------+
      |``total89([2, 8, 3, 9, 2])``      | ``4``                                 |
      +----------------------------------+---------------------------------------+
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

   Create the ``total89(nums)`` function below that takes a list of numbers, 
   ``nums``, and returns the total of the numbers in ``nums`` except for all numbers 
   between an 8 and a 9 (inclusive). 

   .. table:: 
      :name: p3dnd-total-eight-nine-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``total89([1,2])``                | ``3``                                 |
      +----------------------------------+---------------------------------------+
      |``total89([2, 8, 3, 9, 2])``      | ``4``                                 |
      +----------------------------------+---------------------------------------+
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
               break #paired: use continue
   =====
           else:
   =====
               sum += num
   =====
       return sum

.. parsonsprob:: p3dnd-sum-digits-nd
   :numbered: left
   :adaptive:

   Create the ``sumDigits(str)`` function that takes a string, ``str``, and returns a number based on the following conditions.
   
   * return the sum of the digits 0-9 ignoring all other characters
   * return 0 if there are no digits in the string.

   .. table:: 
      :name: p3dnd-sum-digits-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``sumDigits("aa1bc2d3")``         | ``6``                                 |
      +----------------------------------+---------------------------------------+
      |``sumDigits("aa11b33")``          | ``8``                                 |
      +----------------------------------+---------------------------------------+
      |``sumDigits("Chocolate")``        | ``0``                                 |
      +----------------------------------+---------------------------------------+
   -----
   def sumDigits(string):
   =====
       total = 0
   =====
       for character in string:
   =====
           if chatracter >= '0' and character <= '9':
   =====
               digit = int(character)
   =====
               total += digit
   =====
      return total
   

.. parsonsprob:: p3dnd-sum-digits-wd
   :numbered: left
   :adaptive:
 
   Create the ``sumDigits(str)`` function that takes a string, ``str``, and returns a number based on the following conditions.
   
   * return the sum of the digits 0-9 ignoring all other characters
   * return 0 if there are no digits in the string.

   .. table:: 
      :name: p3dnd-sum-digits-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``sumDigits("aa1bc2d3")``         | ``6``                                 |
      +----------------------------------+---------------------------------------+
      |``sumDigits("aa11b33")``          | ``8``                                 |
      +----------------------------------+---------------------------------------+
      |``sumDigits("Chocolate")``        | ``0``                                 |
      +----------------------------------+---------------------------------------+
   -----
   def sumDigits(string):
   =====
       total = 0
   =====
       for character in string:
   =====
           if chatracter >= '0' and character <= '9':
   =====
           if chatracter < '0' and character > '9': #paired: need to check if character is within that range not outside it.
   =====
               total += int(character)
   =====
               total += character #paired: need to convert to int
   =====
      return total
   =====
      print(total) #paired: need to return not print

.. parsonsprob:: p3dnd-max-block-nd
   :numbered: left
   :adaptive:

   Create the function ``maxBlock(str)`` that takes a string, ``str``, and 
   returns the length of the largest "block" in the string. A
   block is a run of adjacent chars that are the same.

   .. table:: 
      :name: p3dnd-max-block-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``maxBlock("hoopla")``            | ``2``                                 |
      +----------------------------------+---------------------------------------+
      |``maxBlock("abbCCCCddBBBxx")``    | ``4``                                 |
      +----------------------------------+---------------------------------------+
      |``maxBlock("")``                  | ``0``                                 |
      +----------------------------------+---------------------------------------+
   -----
   def maxBlock(string):
   =====
       max = 0
   =====
       for i in range(len(string)):
   =====
           count = 1
   =====
           for j in range(i+1, len(string)):
   =====
               if string[i] == string[j]:
   =====
                   count += 1
   =====
               else:
   =====
                   break
   =====
           if count > max:
   =====
               max = count
   =====
       return max

.. parsonsprob:: p3dnd-max-block-wd
   :numbered: left
   :adaptive:

   Create the function ``maxBlock(str)`` that takes a string, ``str``, and 
   returns the length of the largest "block" in the string. A
   block is a run of adjacent chars that are the same.

   .. table:: 
      :name: p3dnd-max-block-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``maxBlock("hoopla")``            | ``2``                                 |
      +----------------------------------+---------------------------------------+
      |``maxBlock("abbCCCCddBBBxx")``    | ``4``                                 |
      +----------------------------------+---------------------------------------+
      |``maxBlock("")``                  | ``0``                                 |
      +----------------------------------+---------------------------------------+
   -----
   def maxBlock(string):
   =====
       max = 0
   =====
       for i in range(len(string)):
   =====
       for i in range(string): #paired: need to iterate over the length of the string not the string itself
   =====
           count = 1
   =====
           for j in range(i+1, len(string)):
   =====
               if string[i] == string[j]:
   =====
                   count += 1
   =====
               else:
   =====
                   break
   =====
                   continue #paired: should break out of the loop as we are done with this block
   =====
           if count > max:
   =====
           if count < max: #paired: need to check if count is greater than max not less than
   =====
               max = count
   =====
       return max

.. parsonsprob:: p3dnd-zero-front-nd
   :numbered: left
   :adaptive:

   Create the function ``zeroFront(nums)`` that takes a list of numbers, ``nums``
   and returns a list with the numbers
   rearranged so that all of the zeros are grouped at the start of the list. 

   .. table:: 
      :name: p3dnd-zero-front-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``zeroFront([1, 0, 0, 1])``       | ``[0, 0, 1, 1]``                      |          
      +----------------------------------+---------------------------------------+
      |``zeroFront([0, 1, 1, 0, 1])``    | ``[0, 0, 1, 1, 1]``                   |              
      +----------------------------------+---------------------------------------+
      |``zeroFront([1, 0])``             | ``[0, 1]``                            |
      +----------------------------------+---------------------------------------+
   -----
   def zeroFront(nums):
   =====
       zero_idx = 0 
   =====
       for i in range(len(nums)):
   =====
           if nums[i] == 0:
   =====
              tmp = nums[i]
   =====
              nums[i] = nums[zero_idx]
   =====
              nums[zero_idx] = tmp
   =====
              zero_idx += 1
   =====
       return nums
          
.. parsonsprob:: p3dnd-zero-front-wd
   :numbered: left
   :adaptive:

   Create the function ``zeroFront(nums)`` that takes a list of numbers, ``nums``
   and returns a list with the numbers
   rearranged so that all of the zeros are grouped at the start of the list. 

   .. table:: 
      :name: p3dnd-zero-front-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``zeroFront([1, 0, 0, 1])``       | ``[0, 0, 1, 1]``                      |          
      +----------------------------------+---------------------------------------+
      |``zeroFront([0, 1, 1, 0, 1])``    | ``[0, 0, 1, 1, 1]``                   |              
      +----------------------------------+---------------------------------------+
      |``zeroFront([1, 0])``             | ``[0, 1]``                            |
      +----------------------------------+---------------------------------------+
   -----
   def zeroFront(nums):
   =====
       zero_idx = 0 
   =====
       for i in range(len(nums)):
   =====
       for i in nums: #paired: need to iterate over the length of the array not the array itself
   =====
           if nums[i] == 0:
   =====
           if nums[i] != 0: #paired: need to check if the number is not zero
   =====
              tmp = nums[i]
   =====
              nums[i] = nums[zero_idx]
   =====
              nums[zero_idx] = tmp
   =====
              zero_idx += 1
   =====
              zero_idx + 1 #paired: need to set the zero_idx variable when incrementing
   =====
       return nums


.. parsonsprob:: p3dnd-two-two-nd
   :numbered: left
   :adaptive:

   Create the function ``twoTwo(nums)`` that takes a list of numbers, ``nums``
   and returns true if every 2 that appears in the list is
   next to another 2. Otherwise it returns ``False``.

   .. table:: 
      :name: p3dnd-two-two-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``twoTwo([4, 2, 2, 3])``          | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``twoTwo([2, 2, 4])``             | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``twoTwo([2, 2, 4, 2])``          | ``False``                             |
      +----------------------------------+---------------------------------------+
   -----
   def twoTwo(nums):
   =====
     for i in range(len(nums)):
   =====
        if nums[i] == 2:
   =====
           if i > 0 and nums[i-1] == 2:
   =====
               continue
   =====
           elif i < len(nums) - 1 and nums[i+1] == 2:
   =====
               continue
   =====
           else:
   =====
               return False
   =====
     return True

.. parsonsprob:: p3dnd-two-two-wd
   :numbered: left
   :adaptive:

   Create the function ``twoTwo(nums)`` that takes a list of numbers, ``nums``
   and returns ``True`` if every 2 that appears in the list is
   next to another 2. Otherwise it returns ``False``.

   .. table:: 
      :name: p3dnd-two-two-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``twoTwo([4, 2, 2, 3])``          | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``twoTwo([2, 2, 4])``             | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``twoTwo([2, 2, 4, 2])``          | ``False``                             |
      +----------------------------------+---------------------------------------+
   -----
   def twoTwo(nums):
   =====
       for i in range(len(nums)):
   =====
         if nums[i] == 2:
   =====
           if i > 0 and nums[i-1] == 2:
   =====
           if nums[i-1] == 2: #paired: This fails to check if we are at the beginning of the array before checking the previous element
   =====
               continue
   =====
               break #paired: if we break we may end before checking all the 2s
   =====
           elif i < len(nums) - 1 and nums[i+1] == 2:
   =====
           elif nums[i+1] == 2: #paired: This fails to check if we are at the end of the array before checking the next element
   =====
               continue
   =====
               break #paired: if we break we may end before checking all the 2s
   =====
           else:
   =====
               return False
   =====
     return True


.. parsonsprob:: p3dnd-bob-there-nd
   :numbered: left
   :adaptive:

   Create a function, ``bobThere(str)`` that takes a string, ``str``. It returns ``True`` if ``str`` contains 
   a "bob" string, but where the
   middle 'o' char can be any char. Otherwise it returns ``False``.

   .. table:: 
      :name: p3dnd-bob-there-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``bobThere("abcbob")``            | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``bobThere("b9b")``               | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``bobThere("bac")``               | ``False``                             |
      +----------------------------------+---------------------------------------+
   -----
   def bobThere(str):
   =====
       for i in range(len(str)-2):
   =====
           if str[i] == 'b' and str[i+2] == 'b':
   =====
               return True
   =====
       return False

.. parsonsprob:: p3dnd-bob-there-wd
   :numbered: left
   :adaptive:

   Create a function, ``bobThere(str)`` that takes a string, ``str``. It returns ``True`` if ``str`` contains 
   a "bob" string, but where the
   middle 'o' char can be any char. Otherwise it returns ``False``.

   .. table:: 
      :name: p3dnd-bob-there-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``bobThere("abcbob")``            | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``bobThere("b9b")``               | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``bobThere("bac")``               | ``False``                             |
      +----------------------------------+---------------------------------------+
   -----
   def bobThere(str):
   =====
       for i in range(len(str)-2):
   =====
       for i in range(len(str)): #paired: need to interate over the length minus 2 so as not to go out of bounds
   =====
           if str[i] == 'b' and str[i+2] == 'b':
   =====
           if str[i] == 'b' and str[i] == 'b': #paired: Needs to check if hte first and last letter are b
   =====
               return True
   =====
       return False

.. parsonsprob:: p3dnd-two-sum-nd
   :numbered: left
   :adaptive:

   Create a function ``twoSum(nums, target)`` that takes a list of integers
   ``nums`` and an integer ``target`` and returns the indices of the
   two numbers such that they add up to ``target``. If no two numbers add up to
   ``target``, it returns an empty list. Assume that each input has exactly one 
   solution, and you may not use the same element twice.

   .. table:: 
      :name: p3dnd-two-sum-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``twoSum([2,7,11,15], 9)``        | ``[0, 1]``                            |
      +----------------------------------+---------------------------------------+
      |``twoSum([2,7,11,15], 13)``       | ``[0, 2]``                            |
      +----------------------------------+---------------------------------------+
      |``twoSum([2,7,11,15], 5)``        | ``[]``                                |
      +----------------------------------+---------------------------------------+
   -----
   def twoSum(nums, target):
   =====
      for i in range(len(nums)):
   =====
           for j in range(i+1, len(nums)):
   =====
               if nums[i] + nums[j] == target:
   =====
                   return [i, j]
   =====
      return []


.. parsonsprob:: p3dnd-two-sum-wd
   :numbered: left
   :adaptive:

   Create a function ``twoSum(nums, target)`` that takes a list of integers
   ``nums`` and an integer ``target`` and returns the indices of the
   two numbers such that they add up to ``target``. If no two numbers add up to
   ``target``, it returns an empty list. Assume that each input has exactly one 
   solution, and you may not use the same element twice.

   .. table:: 
      :name: p3dnd-two-sum-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``twoSum([2,7,11,15], 9)``        | ``[0, 1]``                            |
      +----------------------------------+---------------------------------------+
      |``twoSum([2,7,11,15], 13)``       | ``[0, 2]``                            |
      +----------------------------------+---------------------------------------+
      |``twoSum([2,7,11,15], 5)``        | ``[]``                                |
      +----------------------------------+---------------------------------------+
   -----
   def twoSum(nums, target):
   =====
      for i in range(len(nums)):
   =====
           for j in range(i+1, len(nums)):
   =====
           for j in range(i, len(nums)): #paired: need to start at i+1 so as not to check the same element twice
   =====
               if nums[i] + nums[j] == target:
   =====
               if nums[i] + nums[i] = target: #paired: need to use comparison operator instead of assignment operator
   =====
                   return [i, j]
   =====
      return []

.. parsonsprob:: p3dnd-palindrome-number-nd
   :numbered: left
   :adaptive:

   Create a function ``isPalindrome(x)`` that takes an integer, ``x``, and returns 
   ``True`` if x is a palindrome , and ``False`` otherwise.   An integer is a palindrome 
   if the digits read the same backwards as forwards.

   .. table:: 
      :name: p3dnd-palindrome-number-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``isPalindrome(121)``             | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``isPalindrome(888)``             | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``isPalindrome(678)``             | ``[]``                                |
      +----------------------------------+---------------------------------------+
   -----
   def isPalindrome(x):
   =====
      strx = str(x)
      left = 0
      right = len(strx) - 1
   =====
      while left < right:
   =====
         if strx[left] != strx[right]:
   =====
              return False
   =====
        left += 1
        right -= 1
   =====
      return True

.. parsonsprob:: p3dnd-palindrome-number-wd
   :numbered: left
   :adaptive:

   Create a function ``isPalindrome(x)`` that takes an integer, ``x``, and returns 
   ``True`` if x is a palindrome , and ``False`` otherwise.  An integer is a palindrome 
   if the digits read the same backwards as forwards.

   .. table:: 
      :name: p3dnd-palindrome-number-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``isPalindrome(121)``             | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``isPalindrome(888)``             | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``isPalindrome(678)``             | ``[]``                                |
      +----------------------------------+---------------------------------------+
   -----
   def isPalindrome(x):
   =====
      strx = str(x)
      left = 0
      right = len(strx) - 1
   =====
      left = 0
      right = len(strx) #paired: right should be one less than the length of the string
   ===== 
      while left < right:
   =====
         if strx[left] != strx[right]:
   =====
              return False
   =====
        left += 1
        right -= 1
   =====
        left -= 1
        right += 1 #paired: left and right should be incremented and decremented respectively
    =====
      return True
        



      















