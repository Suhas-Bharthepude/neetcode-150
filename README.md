# NeetCode 150 · Day by Day

Start **Mon Oct 19, 2026**. 60 to 90 min a day. Easies and Mediums by **Wed Jan 27, 2027**, then an optional Hard pass.

How this works: every day you open our Claude chat and send `Day N`. I teach, give hints, review your code, and tell you what to re-solve. This document tells you exactly what to create and what to check off.

---

## Part 1 · One-time setup (do this before Day 1, 10 min)

```bash
mkdir neetcode-150 && cd neetcode-150
git init
touch README.md PATTERNS.md reviews.md
code .
```

Paste this whole document into `README.md`. Then your repo grows like this as you go:

```
neetcode-150/
├── README.md          ← this plan. Check boxes as you finish
├── PATTERNS.md        ← one line per problem: signal → pattern. Your cheat sheet
├── reviews.md         ← what to re-solve and when
├── 01-arrays-hashing/
│   ├── notes.md       ← created on the topic's first day. I give you the content
│   ├── problems/
│   │   ├── 0217_contains_duplicate.py
│   │   └── ...one file per problem
│   └── exercises.py   ← created on the topic's last day. Exercises I write for you
├── 02-two-pointers/
│   └── ...same three things
└── ...
```

Only create a folder the day you start that topic. You never have more open than you need today.

Put this in `PATTERNS.md`:

```markdown
# Patterns I've seen
| Problem | The signal in the prompt | Pattern | Why it works (my words) |
|---|---|---|---|
```

Put this in `reviews.md`:

```markdown
# Reviews
Conf 1 = needed the answer. 2 = needed a hint. 3 = solo and could explain it.
Re-solve after: conf 1 → 1 day, conf 2 → 3 days, conf 3 → 7 days. Clean again → double the gap.

| Problem | Date solved | Conf | Next re-solve |
|---|---|---|---|
```

---

## Part 2 · The problem file template

Every problem file starts like this. The top half is filled in BEFORE you write any code. That's the part that stops you from memorizing.

```python
"""
<number>. <name>  [Easy/Medium]
<link>

BEFORE CODING (fill these in, out loud first)
1. Input / output in my words:
2. Constraints → target Big O:
3. Brute force + its Big O:
4. Where is the brute force wasting work?
5. What would I need to know instantly to kill that waste? → pattern / data structure:

AFTER SOLVING
Final Time / Space:
Variation Claude gave me + how my solution would change:
Mistake I made:
"""

class Solution:
    pass


if __name__ == "__main__":
    s = Solution()
    # assert s.method(example_input) == expected
    # assert s.method(my_edge_case) == expected
```

---

## Part 3 · How to actually learn the pattern, not the answer

**The 5 questions (the top of the template).** Every problem, every time, even the easy ones. Question 4 is the important one. You find the repeated or wasted work in the brute force. Question 5 asks what tool removes it. If you can always answer those two, you can solve problems you've never seen.

**The rules for getting help from me:**
1. Try alone first. 15 min for Easy, 25 min for Medium.
2. Then say `hint`. I'll ask you a question, not give you an answer. Each `hint` goes one step further.
3. `SHOW` gets you the full solution. Use it only if you're truly stuck, and log conf 1.

**The variation test.** After you solve each problem I'll change one thing. For example: "what if the array was sorted?", "what if it's a stream?", or "what if you need all pairs, not one?" You tell me how your solution changes without coding it. If you can't answer, you memorized it. That's when we dig in.

**PATTERNS.md.** After each problem, write the signal you saw in the prompt and why the pattern fits. Example: `| Two Sum | "find two numbers that add to target" | hash map of seen values | for each x I need to know instantly whether target - x showed up already |`. By January this file is your whole interview cheat sheet.

**Exercise days.** The last day of each topic has no LeetCode. I give you 4 to 6 fresh problems that use the same pattern but look different. They come with asserts. If you can pass them without opening your old files, you know the topic.

---

## Part 4 · Every-day checklist (same shape every day)

- [ ] Send me `Day N`
- [ ] Warm up: re-solve anything due in `reviews.md` from a blank `scratch.py` (max 2, then delete the file)
- [ ] New topic day: create the folder and `notes.md`, paste in my notes, answer my 3 check questions
- [ ] For each problem: create the file, fill BEFORE CODING, solve, run your asserts, submit on LeetCode
- [ ] Paste your code to me. I review it and give you a variation
- [ ] Watch the NeetCode video for the problem (its page at https://neetcode.io/practice). Note one thing he did differently
- [ ] Fill AFTER SOLVING. Add a row to `PATTERNS.md` and `reviews.md`
- [ ] `git add -A && git commit -m "day N"`

Missed a day? Don't double up. Just do the next Day N on the next day and the end date slides back. That's fine.

---

## Part 5 · The schedule

## Week 1

### Day 1 · Mon Oct 19 · Arrays & Hashing (new topic)
- [ ] Message me `Day 1`
- [ ] Create `01-arrays-hashing/notes.md` and `01-arrays-hashing/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Contains Duplicate [Easy] → `01-arrays-hashing/problems/0217_contains_duplicate.py`  
      https://leetcode.com/problems/contains-duplicate/
- [ ] Valid Anagram [Easy] → `01-arrays-hashing/problems/0242_valid_anagram.py`  
      https://leetcode.com/problems/valid-anagram/
- [ ] Two Sum [Easy] → `01-arrays-hashing/problems/0001_two_sum.py`  
      https://leetcode.com/problems/two-sum/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 2 · Tue Oct 20 · Arrays & Hashing
- [ ] Message me `Day 2`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Group Anagrams [Medium] → `01-arrays-hashing/problems/0049_group_anagrams.py`  
      https://leetcode.com/problems/group-anagrams/
- [ ] Top K Frequent Elements [Medium] → `01-arrays-hashing/problems/0347_top_k_frequent_elements.py`  
      https://leetcode.com/problems/top-k-frequent-elements/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 3 · Wed Oct 21 · Arrays & Hashing
- [ ] Message me `Day 3`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Encode and Decode Strings [Medium] → `01-arrays-hashing/problems/0271_encode_and_decode_strings.py`  
      https://leetcode.com/problems/encode-and-decode-strings/ (premium, use https://neetcode.io/practice)
- [ ] Product of Array Except Self [Medium] → `01-arrays-hashing/problems/0238_product_of_array_except_self.py`  
      https://leetcode.com/problems/product-of-array-except-self/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 4 · Thu Oct 22 · Arrays & Hashing
- [ ] Message me `Day 4`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Valid Sudoku [Medium] → `01-arrays-hashing/problems/0036_valid_sudoku.py`  
      https://leetcode.com/problems/valid-sudoku/
- [ ] Longest Consecutive Sequence [Medium] → `01-arrays-hashing/problems/0128_longest_consecutive_sequence.py`  
      https://leetcode.com/problems/longest-consecutive-sequence/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 5 · Fri Oct 23 · Arrays & Hashing exercises (topic checkpoint)
- [ ] Message me `Day 5`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `01-arrays-hashing/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `01-arrays-hashing/notes.md`
- [ ] `git commit`

### Day 6 · Sat Oct 24 · Two Pointers (new topic)
- [ ] Message me `Day 6`
- [ ] Create `02-two-pointers/notes.md` and `02-two-pointers/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Valid Palindrome [Easy] → `02-two-pointers/problems/0125_valid_palindrome.py`  
      https://leetcode.com/problems/valid-palindrome/
- [ ] Two Sum II [Medium] → `02-two-pointers/problems/0167_two_sum_ii_input_array_is_sorted.py`  
      https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 7 · Sun Oct 25 · Review day
- [ ] Message me `Day 7` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 2

### Day 8 · Mon Oct 26 · Two Pointers
- [ ] Message me `Day 8`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] 3Sum [Medium] → `02-two-pointers/problems/0015_3sum.py`  
      https://leetcode.com/problems/3sum/
- [ ] Container With Most Water [Medium] → `02-two-pointers/problems/0011_container_with_most_water.py`  
      https://leetcode.com/problems/container-with-most-water/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 9 · Tue Oct 27 · Two Pointers exercises (topic checkpoint)
- [ ] Message me `Day 9`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `02-two-pointers/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `02-two-pointers/notes.md`
- [ ] Optional boss problem if you finish early: Trapping Rain Water. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 10 · Wed Oct 28 · Stack (new topic)
- [ ] Message me `Day 10`
- [ ] Create `03-stack/notes.md` and `03-stack/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Valid Parentheses [Easy] → `03-stack/problems/0020_valid_parentheses.py`  
      https://leetcode.com/problems/valid-parentheses/
- [ ] Min Stack [Medium] → `03-stack/problems/0155_min_stack.py`  
      https://leetcode.com/problems/min-stack/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 11 · Thu Oct 29 · Stack
- [ ] Message me `Day 11`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Evaluate Reverse Polish Notation [Medium] → `03-stack/problems/0150_evaluate_reverse_polish_notation.py`  
      https://leetcode.com/problems/evaluate-reverse-polish-notation/
- [ ] Generate Parentheses [Medium] → `03-stack/problems/0022_generate_parentheses.py`  
      https://leetcode.com/problems/generate-parentheses/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 12 · Fri Oct 30 · Stack
- [ ] Message me `Day 12`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Daily Temperatures [Medium] → `03-stack/problems/0739_daily_temperatures.py`  
      https://leetcode.com/problems/daily-temperatures/
- [ ] Car Fleet [Medium] → `03-stack/problems/0853_car_fleet.py`  
      https://leetcode.com/problems/car-fleet/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 13 · Sat Oct 31 · Stack exercises (topic checkpoint)
- [ ] Message me `Day 13`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `03-stack/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `03-stack/notes.md`
- [ ] Optional boss problem if you finish early: Largest Rectangle in Histogram. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 14 · Sun Nov 01 · Review day
- [ ] Message me `Day 14` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 3

### Day 15 · Mon Nov 02 · Binary Search (new topic)
- [ ] Message me `Day 15`
- [ ] Create `04-binary-search/notes.md` and `04-binary-search/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Binary Search [Easy] → `04-binary-search/problems/0704_binary_search.py`  
      https://leetcode.com/problems/binary-search/
- [ ] Search a 2D Matrix [Medium] → `04-binary-search/problems/0074_search_a_2d_matrix.py`  
      https://leetcode.com/problems/search-a-2d-matrix/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 16 · Tue Nov 03 · Binary Search
- [ ] Message me `Day 16`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Koko Eating Bananas [Medium] → `04-binary-search/problems/0875_koko_eating_bananas.py`  
      https://leetcode.com/problems/koko-eating-bananas/
- [ ] Find Minimum in Rotated Sorted Array [Medium] → `04-binary-search/problems/0153_find_minimum_in_rotated_sorted_array.py`  
      https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 17 · Wed Nov 04 · Binary Search
- [ ] Message me `Day 17`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Search in Rotated Sorted Array [Medium] → `04-binary-search/problems/0033_search_in_rotated_sorted_array.py`  
      https://leetcode.com/problems/search-in-rotated-sorted-array/
- [ ] Time Based Key-Value Store [Medium] → `04-binary-search/problems/0981_time_based_key_value_store.py`  
      https://leetcode.com/problems/time-based-key-value-store/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 18 · Thu Nov 05 · Binary Search exercises (topic checkpoint)
- [ ] Message me `Day 18`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `04-binary-search/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `04-binary-search/notes.md`
- [ ] Optional boss problem if you finish early: Median of Two Sorted Arrays. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 19 · Fri Nov 06 · Sliding Window (new topic)
- [ ] Message me `Day 19`
- [ ] Create `05-sliding-window/notes.md` and `05-sliding-window/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Best Time to Buy and Sell Stock [Easy] → `05-sliding-window/problems/0121_best_time_to_buy_and_sell_stock.py`  
      https://leetcode.com/problems/best-time-to-buy-and-sell-stock/
- [ ] Longest Substring Without Repeating Characters [Medium] → `05-sliding-window/problems/0003_longest_substring_without_repeating_characters.py`  
      https://leetcode.com/problems/longest-substring-without-repeating-characters/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 20 · Sat Nov 07 · Sliding Window
- [ ] Message me `Day 20`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Longest Repeating Character Replacement [Medium] → `05-sliding-window/problems/0424_longest_repeating_character_replacement.py`  
      https://leetcode.com/problems/longest-repeating-character-replacement/
- [ ] Permutation in String [Medium] → `05-sliding-window/problems/0567_permutation_in_string.py`  
      https://leetcode.com/problems/permutation-in-string/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 21 · Sun Nov 08 · Review day
- [ ] Message me `Day 21` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 4

### Day 22 · Mon Nov 09 · Sliding Window exercises (topic checkpoint)
- [ ] Message me `Day 22`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `05-sliding-window/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `05-sliding-window/notes.md`
- [ ] Optional boss problem if you finish early: Minimum Window Substring, Sliding Window Maximum. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 23 · Tue Nov 10 · Linked List (new topic)
- [ ] Message me `Day 23`
- [ ] Create `06-linked-list/notes.md` and `06-linked-list/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Reverse Linked List [Easy] → `06-linked-list/problems/0206_reverse_linked_list.py`  
      https://leetcode.com/problems/reverse-linked-list/
- [ ] Merge Two Sorted Lists [Easy] → `06-linked-list/problems/0021_merge_two_sorted_lists.py`  
      https://leetcode.com/problems/merge-two-sorted-lists/
- [ ] Linked List Cycle [Easy] → `06-linked-list/problems/0141_linked_list_cycle.py`  
      https://leetcode.com/problems/linked-list-cycle/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 24 · Wed Nov 11 · Linked List
- [ ] Message me `Day 24`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Reorder List [Medium] → `06-linked-list/problems/0143_reorder_list.py`  
      https://leetcode.com/problems/reorder-list/
- [ ] Remove Nth Node From End of List [Medium] → `06-linked-list/problems/0019_remove_nth_node_from_end_of_list.py`  
      https://leetcode.com/problems/remove-nth-node-from-end-of-list/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 25 · Thu Nov 12 · Linked List
- [ ] Message me `Day 25`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Copy List with Random Pointer [Medium] → `06-linked-list/problems/0138_copy_list_with_random_pointer.py`  
      https://leetcode.com/problems/copy-list-with-random-pointer/
- [ ] Add Two Numbers [Medium] → `06-linked-list/problems/0002_add_two_numbers.py`  
      https://leetcode.com/problems/add-two-numbers/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 26 · Fri Nov 13 · Linked List
- [ ] Message me `Day 26`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Find the Duplicate Number [Medium] → `06-linked-list/problems/0287_find_the_duplicate_number.py`  
      https://leetcode.com/problems/find-the-duplicate-number/
- [ ] LRU Cache [Medium] → `06-linked-list/problems/0146_lru_cache.py`  
      https://leetcode.com/problems/lru-cache/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 27 · Sat Nov 14 · Linked List exercises (topic checkpoint)
- [ ] Message me `Day 27`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `06-linked-list/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `06-linked-list/notes.md`
- [ ] Optional boss problem if you finish early: Merge K Sorted Lists, Reverse Nodes in K-Group. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 28 · Sun Nov 15 · Review day
- [ ] Message me `Day 28` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 5

### Day 29 · Mon Nov 16 · Trees (new topic)
- [ ] Message me `Day 29`
- [ ] Create `07-trees/notes.md` and `07-trees/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Invert Binary Tree [Easy] → `07-trees/problems/0226_invert_binary_tree.py`  
      https://leetcode.com/problems/invert-binary-tree/
- [ ] Maximum Depth of Binary Tree [Easy] → `07-trees/problems/0104_maximum_depth_of_binary_tree.py`  
      https://leetcode.com/problems/maximum-depth-of-binary-tree/
- [ ] Diameter of Binary Tree [Easy] → `07-trees/problems/0543_diameter_of_binary_tree.py`  
      https://leetcode.com/problems/diameter-of-binary-tree/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 30 · Tue Nov 17 · Trees
- [ ] Message me `Day 30`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Balanced Binary Tree [Easy] → `07-trees/problems/0110_balanced_binary_tree.py`  
      https://leetcode.com/problems/balanced-binary-tree/
- [ ] Same Tree [Easy] → `07-trees/problems/0100_same_tree.py`  
      https://leetcode.com/problems/same-tree/
- [ ] Subtree of Another Tree [Easy] → `07-trees/problems/0572_subtree_of_another_tree.py`  
      https://leetcode.com/problems/subtree-of-another-tree/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 31 · Wed Nov 18 · Trees
- [ ] Message me `Day 31`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Lowest Common Ancestor of a BST [Medium] → `07-trees/problems/0235_lowest_common_ancestor_of_a_binary_search_tree.py`  
      https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/
- [ ] Binary Tree Level Order Traversal [Medium] → `07-trees/problems/0102_binary_tree_level_order_traversal.py`  
      https://leetcode.com/problems/binary-tree-level-order-traversal/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 32 · Thu Nov 19 · Trees
- [ ] Message me `Day 32`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Binary Tree Right Side View [Medium] → `07-trees/problems/0199_binary_tree_right_side_view.py`  
      https://leetcode.com/problems/binary-tree-right-side-view/
- [ ] Count Good Nodes in Binary Tree [Medium] → `07-trees/problems/1448_count_good_nodes_in_binary_tree.py`  
      https://leetcode.com/problems/count-good-nodes-in-binary-tree/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 33 · Fri Nov 20 · Trees
- [ ] Message me `Day 33`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Validate Binary Search Tree [Medium] → `07-trees/problems/0098_validate_binary_search_tree.py`  
      https://leetcode.com/problems/validate-binary-search-tree/
- [ ] Kth Smallest Element in a BST [Medium] → `07-trees/problems/0230_kth_smallest_element_in_a_bst.py`  
      https://leetcode.com/problems/kth-smallest-element-in-a-bst/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 34 · Sat Nov 21 · Trees
- [ ] Message me `Day 34`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Construct Binary Tree from Preorder and Inorder [Medium] → `07-trees/problems/0105_construct_binary_tree_from_preorder_and_inorder_traversal.py`  
      https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 35 · Sun Nov 22 · Review day
- [ ] Message me `Day 35` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 6

### Day 36 · Mon Nov 23 · Trees exercises (topic checkpoint)
- [ ] Message me `Day 36`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `07-trees/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `07-trees/notes.md`
- [ ] Optional boss problem if you finish early: Binary Tree Maximum Path Sum, Serialize and Deserialize Binary Tree. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 37 · Tue Nov 24 · Tries (new topic)
- [ ] Message me `Day 37`
- [ ] Create `08-tries/notes.md` and `08-tries/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Implement Trie (Prefix Tree) [Medium] → `08-tries/problems/0208_implement_trie_prefix_tree.py`  
      https://leetcode.com/problems/implement-trie-prefix-tree/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 38 · Wed Nov 25 · Tries
- [ ] Message me `Day 38`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Design Add and Search Words [Medium] → `08-tries/problems/0211_design_add_and_search_words_data_structure.py`  
      https://leetcode.com/problems/design-add-and-search-words-data-structure/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Thu Nov 26 · OFF (Thanksgiving)

### Day 39 · Fri Nov 27 · Tries exercises (topic checkpoint)
- [ ] Message me `Day 39`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `08-tries/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `08-tries/notes.md`
- [ ] Optional boss problem if you finish early: Word Search II. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 40 · Sat Nov 28 · Heap / Priority Queue (new topic)
- [ ] Message me `Day 40`
- [ ] Create `09-heap/notes.md` and `09-heap/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Kth Largest Element in a Stream [Easy] → `09-heap/problems/0703_kth_largest_element_in_a_stream.py`  
      https://leetcode.com/problems/kth-largest-element-in-a-stream/
- [ ] Last Stone Weight [Easy] → `09-heap/problems/1046_last_stone_weight.py`  
      https://leetcode.com/problems/last-stone-weight/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 41 · Sun Nov 29 · Review day
- [ ] Message me `Day 41` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 7

### Day 42 · Mon Nov 30 · Heap / Priority Queue
- [ ] Message me `Day 42`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] K Closest Points to Origin [Medium] → `09-heap/problems/0973_k_closest_points_to_origin.py`  
      https://leetcode.com/problems/k-closest-points-to-origin/
- [ ] Kth Largest Element in an Array [Medium] → `09-heap/problems/0215_kth_largest_element_in_an_array.py`  
      https://leetcode.com/problems/kth-largest-element-in-an-array/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 43 · Tue Dec 01 · Heap / Priority Queue
- [ ] Message me `Day 43`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Task Scheduler [Medium] → `09-heap/problems/0621_task_scheduler.py`  
      https://leetcode.com/problems/task-scheduler/
- [ ] Design Twitter [Medium] → `09-heap/problems/0355_design_twitter.py`  
      https://leetcode.com/problems/design-twitter/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 44 · Wed Dec 02 · Heap / Priority Queue exercises (topic checkpoint)
- [ ] Message me `Day 44`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `09-heap/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `09-heap/notes.md`
- [ ] Optional boss problem if you finish early: Find Median from Data Stream. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 45 · Thu Dec 03 · Backtracking (new topic)
- [ ] Message me `Day 45`
- [ ] Create `10-backtracking/notes.md` and `10-backtracking/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Subsets [Medium] → `10-backtracking/problems/0078_subsets.py`  
      https://leetcode.com/problems/subsets/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 46 · Fri Dec 04 · Backtracking
- [ ] Message me `Day 46`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Combination Sum [Medium] → `10-backtracking/problems/0039_combination_sum.py`  
      https://leetcode.com/problems/combination-sum/
- [ ] Combination Sum II [Medium] → `10-backtracking/problems/0040_combination_sum_ii.py`  
      https://leetcode.com/problems/combination-sum-ii/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 47 · Sat Dec 05 · Backtracking
- [ ] Message me `Day 47`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Permutations [Medium] → `10-backtracking/problems/0046_permutations.py`  
      https://leetcode.com/problems/permutations/
- [ ] Subsets II [Medium] → `10-backtracking/problems/0090_subsets_ii.py`  
      https://leetcode.com/problems/subsets-ii/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 48 · Sun Dec 06 · Review day
- [ ] Message me `Day 48` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 8

### Day 49 · Mon Dec 07 · Backtracking
- [ ] Message me `Day 49`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Word Search [Medium] → `10-backtracking/problems/0079_word_search.py`  
      https://leetcode.com/problems/word-search/
- [ ] Palindrome Partitioning [Medium] → `10-backtracking/problems/0131_palindrome_partitioning.py`  
      https://leetcode.com/problems/palindrome-partitioning/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 50 · Tue Dec 08 · Backtracking
- [ ] Message me `Day 50`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Letter Combinations of a Phone Number [Medium] → `10-backtracking/problems/0017_letter_combinations_of_a_phone_number.py`  
      https://leetcode.com/problems/letter-combinations-of-a-phone-number/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 51 · Wed Dec 09 · Backtracking exercises (topic checkpoint)
- [ ] Message me `Day 51`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `10-backtracking/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `10-backtracking/notes.md`
- [ ] Optional boss problem if you finish early: N-Queens. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 52 · Thu Dec 10 · Graphs (new topic)
- [ ] Message me `Day 52`
- [ ] Create `11-graphs/notes.md` and `11-graphs/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Number of Islands [Medium] → `11-graphs/problems/0200_number_of_islands.py`  
      https://leetcode.com/problems/number-of-islands/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 53 · Fri Dec 11 · Graphs
- [ ] Message me `Day 53`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Max Area of Island [Medium] → `11-graphs/problems/0695_max_area_of_island.py`  
      https://leetcode.com/problems/max-area-of-island/
- [ ] Clone Graph [Medium] → `11-graphs/problems/0133_clone_graph.py`  
      https://leetcode.com/problems/clone-graph/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 54 · Sat Dec 12 · Graphs
- [ ] Message me `Day 54`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Walls and Gates [Medium] → `11-graphs/problems/0286_walls_and_gates.py`  
      https://leetcode.com/problems/walls-and-gates/ (premium, use https://neetcode.io/practice)
- [ ] Rotting Oranges [Medium] → `11-graphs/problems/0994_rotting_oranges.py`  
      https://leetcode.com/problems/rotting-oranges/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 55 · Sun Dec 13 · Review day
- [ ] Message me `Day 55` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 9

### Day 56 · Mon Dec 14 · Graphs
- [ ] Message me `Day 56`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Pacific Atlantic Water Flow [Medium] → `11-graphs/problems/0417_pacific_atlantic_water_flow.py`  
      https://leetcode.com/problems/pacific-atlantic-water-flow/
- [ ] Surrounded Regions [Medium] → `11-graphs/problems/0130_surrounded_regions.py`  
      https://leetcode.com/problems/surrounded-regions/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 57 · Tue Dec 15 · Graphs
- [ ] Message me `Day 57`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Course Schedule [Medium] → `11-graphs/problems/0207_course_schedule.py`  
      https://leetcode.com/problems/course-schedule/
- [ ] Course Schedule II [Medium] → `11-graphs/problems/0210_course_schedule_ii.py`  
      https://leetcode.com/problems/course-schedule-ii/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 58 · Wed Dec 16 · Graphs
- [ ] Message me `Day 58`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Graph Valid Tree [Medium] → `11-graphs/problems/0261_graph_valid_tree.py`  
      https://leetcode.com/problems/graph-valid-tree/ (premium, use https://neetcode.io/practice)
- [ ] Number of Connected Components [Medium] → `11-graphs/problems/0323_number_of_connected_components_in_an_undirected_graph.py`  
      https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/ (premium, use https://neetcode.io/practice)
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 59 · Thu Dec 17 · Graphs
- [ ] Message me `Day 59`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Redundant Connection [Medium] → `11-graphs/problems/0684_redundant_connection.py`  
      https://leetcode.com/problems/redundant-connection/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 60 · Fri Dec 18 · Graphs exercises (topic checkpoint)
- [ ] Message me `Day 60`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `11-graphs/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `11-graphs/notes.md`
- [ ] Optional boss problem if you finish early: Word Ladder. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 61 · Sat Dec 19 · 1-D Dynamic Programming (new topic)
- [ ] Message me `Day 61`
- [ ] Create `12-1d-dp/notes.md` and `12-1d-dp/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Climbing Stairs [Easy] → `12-1d-dp/problems/0070_climbing_stairs.py`  
      https://leetcode.com/problems/climbing-stairs/
- [ ] Min Cost Climbing Stairs [Easy] → `12-1d-dp/problems/0746_min_cost_climbing_stairs.py`  
      https://leetcode.com/problems/min-cost-climbing-stairs/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 62 · Sun Dec 20 · Review day
- [ ] Message me `Day 62` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 10

### Day 63 · Mon Dec 21 · 1-D Dynamic Programming
- [ ] Message me `Day 63`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] House Robber [Medium] → `12-1d-dp/problems/0198_house_robber.py`  
      https://leetcode.com/problems/house-robber/
- [ ] House Robber II [Medium] → `12-1d-dp/problems/0213_house_robber_ii.py`  
      https://leetcode.com/problems/house-robber-ii/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 64 · Tue Dec 22 · 1-D Dynamic Programming
- [ ] Message me `Day 64`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Longest Palindromic Substring [Medium] → `12-1d-dp/problems/0005_longest_palindromic_substring.py`  
      https://leetcode.com/problems/longest-palindromic-substring/
- [ ] Palindromic Substrings [Medium] → `12-1d-dp/problems/0647_palindromic_substrings.py`  
      https://leetcode.com/problems/palindromic-substrings/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 65 · Wed Dec 23 · 1-D Dynamic Programming
- [ ] Message me `Day 65`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Decode Ways [Medium] → `12-1d-dp/problems/0091_decode_ways.py`  
      https://leetcode.com/problems/decode-ways/
- [ ] Coin Change [Medium] → `12-1d-dp/problems/0322_coin_change.py`  
      https://leetcode.com/problems/coin-change/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 66 · Thu Dec 24 · 1-D Dynamic Programming
- [ ] Message me `Day 66`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Maximum Product Subarray [Medium] → `12-1d-dp/problems/0152_maximum_product_subarray.py`  
      https://leetcode.com/problems/maximum-product-subarray/
- [ ] Word Break [Medium] → `12-1d-dp/problems/0139_word_break.py`  
      https://leetcode.com/problems/word-break/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 67 · Fri Dec 25 · 1-D Dynamic Programming
- [ ] Message me `Day 67`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Longest Increasing Subsequence [Medium] → `12-1d-dp/problems/0300_longest_increasing_subsequence.py`  
      https://leetcode.com/problems/longest-increasing-subsequence/
- [ ] Partition Equal Subset Sum [Medium] → `12-1d-dp/problems/0416_partition_equal_subset_sum.py`  
      https://leetcode.com/problems/partition-equal-subset-sum/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 68 · Sat Dec 26 · 1-D Dynamic Programming exercises (topic checkpoint)
- [ ] Message me `Day 68`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `12-1d-dp/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `12-1d-dp/notes.md`
- [ ] `git commit`

### Day 69 · Sun Dec 27 · Review day
- [ ] Message me `Day 69` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 11

### Day 70 · Mon Dec 28 · Intervals (new topic)
- [ ] Message me `Day 70`
- [ ] Create `13-intervals/notes.md` and `13-intervals/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Insert Interval [Medium] → `13-intervals/problems/0057_insert_interval.py`  
      https://leetcode.com/problems/insert-interval/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 71 · Tue Dec 29 · Intervals
- [ ] Message me `Day 71`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Merge Intervals [Medium] → `13-intervals/problems/0056_merge_intervals.py`  
      https://leetcode.com/problems/merge-intervals/
- [ ] Non-overlapping Intervals [Medium] → `13-intervals/problems/0435_non_overlapping_intervals.py`  
      https://leetcode.com/problems/non-overlapping-intervals/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 72 · Wed Dec 30 · Intervals
- [ ] Message me `Day 72`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Meeting Rooms [Easy] → `13-intervals/problems/0252_meeting_rooms.py`  
      https://leetcode.com/problems/meeting-rooms/ (premium, use https://neetcode.io/practice)
- [ ] Meeting Rooms II [Medium] → `13-intervals/problems/0253_meeting_rooms_ii.py`  
      https://leetcode.com/problems/meeting-rooms-ii/ (premium, use https://neetcode.io/practice)
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 73 · Thu Dec 31 · Intervals exercises (topic checkpoint)
- [ ] Message me `Day 73`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `13-intervals/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `13-intervals/notes.md`
- [ ] Optional boss problem if you finish early: Minimum Interval to Include Each Query. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 74 · Fri Jan 01 · Greedy (new topic)
- [ ] Message me `Day 74`
- [ ] Create `14-greedy/notes.md` and `14-greedy/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Maximum Subarray [Medium] → `14-greedy/problems/0053_maximum_subarray.py`  
      https://leetcode.com/problems/maximum-subarray/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 75 · Sat Jan 02 · Greedy
- [ ] Message me `Day 75`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Jump Game [Medium] → `14-greedy/problems/0055_jump_game.py`  
      https://leetcode.com/problems/jump-game/
- [ ] Jump Game II [Medium] → `14-greedy/problems/0045_jump_game_ii.py`  
      https://leetcode.com/problems/jump-game-ii/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 76 · Sun Jan 03 · Review day
- [ ] Message me `Day 76` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 12

### Day 77 · Mon Jan 04 · Greedy
- [ ] Message me `Day 77`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Gas Station [Medium] → `14-greedy/problems/0134_gas_station.py`  
      https://leetcode.com/problems/gas-station/
- [ ] Hand of Straights [Medium] → `14-greedy/problems/0846_hand_of_straights.py`  
      https://leetcode.com/problems/hand-of-straights/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 78 · Tue Jan 05 · Greedy
- [ ] Message me `Day 78`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Merge Triplets to Form Target Triplet [Medium] → `14-greedy/problems/1899_merge_triplets_to_form_target_triplet.py`  
      https://leetcode.com/problems/merge-triplets-to-form-target-triplet/
- [ ] Partition Labels [Medium] → `14-greedy/problems/0763_partition_labels.py`  
      https://leetcode.com/problems/partition-labels/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 79 · Wed Jan 06 · Greedy
- [ ] Message me `Day 79`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Valid Parenthesis String [Medium] → `14-greedy/problems/0678_valid_parenthesis_string.py`  
      https://leetcode.com/problems/valid-parenthesis-string/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 80 · Thu Jan 07 · Greedy exercises (topic checkpoint)
- [ ] Message me `Day 80`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `14-greedy/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `14-greedy/notes.md`
- [ ] `git commit`

### Day 81 · Fri Jan 08 · Advanced Graphs (new topic)
- [ ] Message me `Day 81`
- [ ] Create `15-advanced-graphs/notes.md` and `15-advanced-graphs/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Network Delay Time [Medium] → `15-advanced-graphs/problems/0743_network_delay_time.py`  
      https://leetcode.com/problems/network-delay-time/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 82 · Sat Jan 09 · Advanced Graphs
- [ ] Message me `Day 82`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Min Cost to Connect All Points [Medium] → `15-advanced-graphs/problems/1584_min_cost_to_connect_all_points.py`  
      https://leetcode.com/problems/min-cost-to-connect-all-points/
- [ ] Cheapest Flights Within K Stops [Medium] → `15-advanced-graphs/problems/0787_cheapest_flights_within_k_stops.py`  
      https://leetcode.com/problems/cheapest-flights-within-k-stops/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 83 · Sun Jan 10 · Review day
- [ ] Message me `Day 83` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 13

### Day 84 · Mon Jan 11 · Advanced Graphs exercises (topic checkpoint)
- [ ] Message me `Day 84`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `15-advanced-graphs/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `15-advanced-graphs/notes.md`
- [ ] Optional boss problem if you finish early: Swim in Rising Water, Reconstruct Itinerary, Alien Dictionary. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 85 · Tue Jan 12 · 2-D Dynamic Programming (new topic)
- [ ] Message me `Day 85`
- [ ] Create `16-2d-dp/notes.md` and `16-2d-dp/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Unique Paths [Medium] → `16-2d-dp/problems/0062_unique_paths.py`  
      https://leetcode.com/problems/unique-paths/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 86 · Wed Jan 13 · 2-D Dynamic Programming
- [ ] Message me `Day 86`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Longest Common Subsequence [Medium] → `16-2d-dp/problems/1143_longest_common_subsequence.py`  
      https://leetcode.com/problems/longest-common-subsequence/
- [ ] Best Time to Buy and Sell Stock with Cooldown [Medium] → `16-2d-dp/problems/0309_best_time_to_buy_and_sell_stock_with_cooldown.py`  
      https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-cooldown/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 87 · Thu Jan 14 · 2-D Dynamic Programming
- [ ] Message me `Day 87`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Coin Change II [Medium] → `16-2d-dp/problems/0518_coin_change_ii.py`  
      https://leetcode.com/problems/coin-change-ii/
- [ ] Target Sum [Medium] → `16-2d-dp/problems/0494_target_sum.py`  
      https://leetcode.com/problems/target-sum/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 88 · Fri Jan 15 · 2-D Dynamic Programming
- [ ] Message me `Day 88`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Interleaving String [Medium] → `16-2d-dp/problems/0097_interleaving_string.py`  
      https://leetcode.com/problems/interleaving-string/
- [ ] Edit Distance [Medium] → `16-2d-dp/problems/0072_edit_distance.py`  
      https://leetcode.com/problems/edit-distance/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 89 · Sat Jan 16 · 2-D Dynamic Programming exercises (topic checkpoint)
- [ ] Message me `Day 89`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `16-2d-dp/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `16-2d-dp/notes.md`
- [ ] Optional boss problem if you finish early: Longest Increasing Path in a Matrix, Distinct Subsequences, Burst Balloons, Regular Expression Matching. Otherwise it waits for the Hard pass
- [ ] `git commit`

### Day 90 · Sun Jan 17 · Review day
- [ ] Message me `Day 90` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 14

### Day 91 · Mon Jan 18 · Bit Manipulation (new topic)
- [ ] Message me `Day 91`
- [ ] Create `17-bit-manipulation/notes.md` and `17-bit-manipulation/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Single Number [Easy] → `17-bit-manipulation/problems/0136_single_number.py`  
      https://leetcode.com/problems/single-number/
- [ ] Number of 1 Bits [Easy] → `17-bit-manipulation/problems/0191_number_of_1_bits.py`  
      https://leetcode.com/problems/number-of-1-bits/
- [ ] Counting Bits [Easy] → `17-bit-manipulation/problems/0338_counting_bits.py`  
      https://leetcode.com/problems/counting-bits/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 92 · Tue Jan 19 · Bit Manipulation
- [ ] Message me `Day 92`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Reverse Bits [Easy] → `17-bit-manipulation/problems/0190_reverse_bits.py`  
      https://leetcode.com/problems/reverse-bits/
- [ ] Missing Number [Easy] → `17-bit-manipulation/problems/0268_missing_number.py`  
      https://leetcode.com/problems/missing-number/
- [ ] Sum of Two Integers [Medium] → `17-bit-manipulation/problems/0371_sum_of_two_integers.py`  
      https://leetcode.com/problems/sum-of-two-integers/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 93 · Wed Jan 20 · Bit Manipulation
- [ ] Message me `Day 93`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Reverse Integer [Medium] → `17-bit-manipulation/problems/0007_reverse_integer.py`  
      https://leetcode.com/problems/reverse-integer/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 94 · Thu Jan 21 · Bit Manipulation exercises (topic checkpoint)
- [ ] Message me `Day 94`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `17-bit-manipulation/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `17-bit-manipulation/notes.md`
- [ ] `git commit`

### Day 95 · Fri Jan 22 · Math & Geometry (new topic)
- [ ] Message me `Day 95`
- [ ] Create `18-math-geometry/notes.md` and `18-math-geometry/problems/`
- [ ] I teach the pattern and give you the notes. Paste them into `notes.md`. Answer my 3 check questions before any problem
- [ ] Rotate Image [Medium] → `18-math-geometry/problems/0048_rotate_image.py`  
      https://leetcode.com/problems/rotate-image/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 96 · Sat Jan 23 · Math & Geometry
- [ ] Message me `Day 96`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Spiral Matrix [Medium] → `18-math-geometry/problems/0054_spiral_matrix.py`  
      https://leetcode.com/problems/spiral-matrix/
- [ ] Set Matrix Zeroes [Medium] → `18-math-geometry/problems/0073_set_matrix_zeroes.py`  
      https://leetcode.com/problems/set-matrix-zeroes/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 97 · Sun Jan 24 · Review day
- [ ] Message me `Day 97` with your review log. I pick 3 problems for you to re-solve from a blank file
- [ ] Re-solve them in `scratch.py` (delete it after). No notes, no looking at old code
- [ ] Update `reviews.md`
- [ ] Re-read every line of `PATTERNS.md` out loud

## Week 15

### Day 98 · Mon Jan 25 · Math & Geometry
- [ ] Message me `Day 98`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Happy Number [Easy] → `18-math-geometry/problems/0202_happy_number.py`  
      https://leetcode.com/problems/happy-number/
- [ ] Plus One [Easy] → `18-math-geometry/problems/0066_plus_one.py`  
      https://leetcode.com/problems/plus-one/
- [ ] Pow(x, n) [Medium] → `18-math-geometry/problems/0050_powx_n.py`  
      https://leetcode.com/problems/powx-n/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 99 · Tue Jan 26 · Math & Geometry
- [ ] Message me `Day 99`
- [ ] Warm up: re-solve whatever `reviews.md` says is due (max 2)
- [ ] Multiply Strings [Medium] → `18-math-geometry/problems/0043_multiply_strings.py`  
      https://leetcode.com/problems/multiply-strings/
- [ ] Detect Squares [Medium] → `18-math-geometry/problems/2013_detect_squares.py`  
      https://leetcode.com/problems/detect-squares/
- [ ] Add one line per problem to `PATTERNS.md` and `reviews.md`, then `git commit`

### Day 100 · Wed Jan 27 · Math & Geometry exercises (topic checkpoint)
- [ ] Message me `Day 100`. I give you exercises that are NOT LeetCode problems you've seen
- [ ] Create `18-math-geometry/exercises.py` and paste them in. Each comes with asserts
- [ ] Make every assert pass without looking at your old problem files
- [ ] Write the 3 to 5 sentence "how I recognize this pattern" section at the bottom of `18-math-geometry/notes.md`
- [ ] `git commit`

---

## Part 6 · Hard pass (optional, starts Thu Jan 28)

One Hard per day. Same template and same rules. Skip any you already beat as a boss problem. Send me `Hard: <name>` to start each one.

- [ ] Trapping Rain Water → `02-two-pointers/problems/0042_trapping_rain_water.py`  
      https://leetcode.com/problems/trapping-rain-water/
- [ ] Largest Rectangle in Histogram → `03-stack/problems/0084_largest_rectangle_in_histogram.py`  
      https://leetcode.com/problems/largest-rectangle-in-histogram/
- [ ] Median of Two Sorted Arrays → `04-binary-search/problems/0004_median_of_two_sorted_arrays.py`  
      https://leetcode.com/problems/median-of-two-sorted-arrays/
- [ ] Minimum Window Substring → `05-sliding-window/problems/0076_minimum_window_substring.py`  
      https://leetcode.com/problems/minimum-window-substring/
- [ ] Sliding Window Maximum → `05-sliding-window/problems/0239_sliding_window_maximum.py`  
      https://leetcode.com/problems/sliding-window-maximum/
- [ ] Merge K Sorted Lists → `06-linked-list/problems/0023_merge_k_sorted_lists.py`  
      https://leetcode.com/problems/merge-k-sorted-lists/
- [ ] Reverse Nodes in K-Group → `06-linked-list/problems/0025_reverse_nodes_in_k_group.py`  
      https://leetcode.com/problems/reverse-nodes-in-k-group/
- [ ] Binary Tree Maximum Path Sum → `07-trees/problems/0124_binary_tree_maximum_path_sum.py`  
      https://leetcode.com/problems/binary-tree-maximum-path-sum/
- [ ] Serialize and Deserialize Binary Tree → `07-trees/problems/0297_serialize_and_deserialize_binary_tree.py`  
      https://leetcode.com/problems/serialize-and-deserialize-binary-tree/
- [ ] Word Search II → `08-tries/problems/0212_word_search_ii.py`  
      https://leetcode.com/problems/word-search-ii/
- [ ] Find Median from Data Stream → `09-heap/problems/0295_find_median_from_data_stream.py`  
      https://leetcode.com/problems/find-median-from-data-stream/
- [ ] N-Queens → `10-backtracking/problems/0051_n_queens.py`  
      https://leetcode.com/problems/n-queens/
- [ ] Word Ladder → `11-graphs/problems/0127_word_ladder.py`  
      https://leetcode.com/problems/word-ladder/
- [ ] Minimum Interval to Include Each Query → `13-intervals/problems/1851_minimum_interval_to_include_each_query.py`  
      https://leetcode.com/problems/minimum-interval-to-include-each-query/
- [ ] Swim in Rising Water → `15-advanced-graphs/problems/0778_swim_in_rising_water.py`  
      https://leetcode.com/problems/swim-in-rising-water/
- [ ] Reconstruct Itinerary → `15-advanced-graphs/problems/0332_reconstruct_itinerary.py`  
      https://leetcode.com/problems/reconstruct-itinerary/
- [ ] Alien Dictionary → `15-advanced-graphs/problems/0269_alien_dictionary.py`  
      https://leetcode.com/problems/alien-dictionary/ (premium, use https://neetcode.io/practice)
- [ ] Longest Increasing Path in a Matrix → `16-2d-dp/problems/0329_longest_increasing_path_in_a_matrix.py`  
      https://leetcode.com/problems/longest-increasing-path-in-a-matrix/
- [ ] Distinct Subsequences → `16-2d-dp/problems/0115_distinct_subsequences.py`  
      https://leetcode.com/problems/distinct-subsequences/
- [ ] Burst Balloons → `16-2d-dp/problems/0312_burst_balloons.py`  
      https://leetcode.com/problems/burst-balloons/
- [ ] Regular Expression Matching → `16-2d-dp/problems/0010_regular_expression_matching.py`  
      https://leetcode.com/problems/regular-expression-matching/