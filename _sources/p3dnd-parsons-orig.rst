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
   :noindent:

   Given a string, return the sum of the digits 0-9 that appear in the string,
   ignoring all other characters. Return 0 if there are no digits in the
   string. (Note: Character.isDigit(char) tests if a char is one of the chars
   '0', '1', .. '9'. Integer.parseInt(string) converts a string to an int.)

   sumDigits("aa1bc2d3") → 6
   sumDigits("aa11b33") → 8
   sumDigits("Chocolate") → 0
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
   :noindent:

   Given a string, return the sum of the digits 0-9 that appear in the string,
   ignoring all other characters. Return 0 if there are no digits in the
   string. (Note: Character.isDigit(char) tests if a char is one of the chars
   '0', '1', .. '9'. Integer.parseInt(string) converts a string to an int.)

   * sumDigits("aa1bc2d3") → 6
   * sumDigits("aa11b33") → 8
   * sumDigits("Chocolate") → 0
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
   :noindent:

   Given a string, return the length of the largest "block" in the string. A
   block is a run of adjacent chars that are the same.

   * maxBlock("hoopla") → 2
   * maxBlock("abbCCCddBBBxx") → 3
   * maxBlock("") → 0
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
   :noindent:

   Given a string, return the length of the largest "block" in the string. A
   block is a run of adjacent chars that are the same.

   * maxBlock("hoopla") → 2
   * maxBlock("abbCCCddBBBxx") → 3
   * maxBlock("") → 0
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
   :noindent:

   Return an array that contains the exact same numbers as the given array, but
   rearranged so that all the zeros are grouped at the start of the array. The
   order of the non-zero numbers does not matter. So {1, 0, 0, 1} becomes {0
   ,0, 1, 1}. You may modify and return the given array or make a new array.

   * zeroFront([1, 0, 0, 1]) → [0, 0, 1, 1]
   * zeroFront([0, 1, 1, 0, 1]) → [0, 0, 1, 1, 1]
   * zeroFront([1, 0]) → [0, 1]
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
   :noindent:

   Return an array that contains the exact same numbers as the given array, but
   rearranged so that all the zeros are grouped at the start of the array. The
   order of the non-zero numbers does not matter. So {1, 0, 0, 1} becomes {0
   ,0, 1, 1}. You may modify and return the given array or make a new array.

   * zeroFront([1, 0, 0, 1]) → [0, 0, 1, 1]
   * zeroFront([0, 1, 1, 0, 1]) → [0, 0, 1, 1, 1]
   * zeroFront([1, 0]) → [0, 1]
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
   :noindent:

   Given an array of ints, return true if every 2 that appears in the array is
   next to another 2.

   * twoTwo([4, 2, 2, 3]) → true
   * twoTwo([2, 2, 4]) → true
   * twoTwo([2, 2, 4, 2]) → false
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
   :noindent:

   Given an array of ints, return true if every 2 that appears in the array is next to another 2.

   * twoTwo([4, 2, 2, 3]) → true
   * twoTwo([2, 2, 4]) → true
   * twoTwo([2, 2, 4, 2]) → false

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
   :noindent:

   Return true if the given string contains a "bob" string, but where the
   middle 'o' char can be any char.

   * bobThere("abcbob") → true
   * bobThere("b9b") → true
   * bobThere("bac") → false
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
   :noindent:

   Return true if the given string contains a "bob" string, but where the
   middle 'o' char can be any char.

   * bobThere("abcbob") → true
   * bobThere("b9b") → true
   * bobThere("bac") → false
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

.. parsonsprog:: p3dnd-two-sum-nd
   :numbered: left
   :adaptive:
   :noindent:

   Given an array of integers nums and an integer target, return indices of the
   two numbers such that they add up to target. If no two numbers add up to
   target, return an empty array.

   You may assume that each input would have exactly one solution, and you may
   not use the same element twice.

   For example for nums=[2, 7, 11, 15] and target = 9 will return [0, 1] as
   the numbers at index 0 and 1 add up to 9.
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


.. parsonsprog:: p3dnd-two-sum-wd
   :numbered: left
   :adaptive:
   :noindent:

   Given an array of integers nums and an integer target, return indices of the
   two numbers such that they add up to target. If no two numbers add up to
   target, return an empty array.

   You may assume that each input would have exactly one solution, and you may
   not use the same element twice.

   For example for nums=[2, 7, 11, 15] and target = 9 will return [0, 1] as
   the numbers at index 0 and 1 add up to 9.
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



.. parsonsprog:: p3dnd-palindrome-number-nd
   :numbered: left
   :adaptive:
   :noindent:

   Given an integer x, return true if x is a palindrome , and false otherwise.

   For example, 121 is a palindrome, as well as 888. 678 is not a palindrome.
   Additionally, negative numbers cannot be palindromes.
   -----
   def isPalindrome(x):
   =====
      left = 0
      right = len(string) - 1
   =====
      left = 0
      right = len(string) #paired: right should be one less than the length of the string
   ===== 
      while left < right:
   =====
         if string[left] != string[right]:
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
        



      















