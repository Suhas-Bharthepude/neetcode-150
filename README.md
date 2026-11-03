# Co-op Prep · Core 75 · Day by Day

Start **Wed Nov 4, 2026**. 3 hours a day. Core 75 done by **Thu Dec 10**, all 129 Easies and Mediums by about **Dec 23**.

Every day you send me `Day N` in our chat. I teach, give hints, review your code, and tell you what to re-solve.

## Part 0 · The strategy

**Phase 1: Core 75 (with coaching).** This is the Blind 75 minus its 7 Hards, plus 7 Mediums that show up a lot in co-op interviews: Binary Search, Min Stack, Daily Temperatures, LRU Cache, Kth Largest Element, K Closest Points, and Rotting Oranges. We go topic by topic in roadmap order. You try each problem alone first, then I give hints if you're stuck. After every topic or two there is a checkpoint with fresh exercises, folded into a normal day.

**Phase 2: The other 54 NeetCode 150 Mediums and Easies (solo).** This is your senior's idea, done the right way. You do them alone with a strict timebox: 15 min for Easy, 25 for Medium. Only after the timebox is up can you ask me for a single hint. These problems test whether the patterns actually stuck. Aim for 5 a day.

**Hards are optional.** They're listed at the end in case an interview needs them.

**If an interview lands mid-plan,** tell me the company and date. I'll reorder what's left so the most likely topics come first.

## Part 1 · Repo (already set up)

You already have `README.md`, `PATTERNS.md`, and `reviews.md`. Replace the README with this file. Each topic gets a folder the day you start it:

```
NN-topic/
├── notes.md        ← first day of the topic. I give you the content
├── problems/       ← one .py file per problem
└── exercises.py    ← checkpoint day
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

## Part 4 · What a 3 hour day looks like

| time | what |
|---|---|
| 0:00 to 0:30 | Reviews due in `reviews.md`, cold, from `scratch.py` |
| 0:30 to 2:30 | New problems. Fill BEFORE CODING, timebox (Easy 15, Medium 25), hints only after, paste code to me, get a variation |
| 2:30 to 2:50 | NeetCode video for each new problem (on its page at https://neetcode.io/practice). Note one thing he did differently |
| 2:50 to 3:00 | `PATTERNS.md`, `reviews.md`, commit, push |

On checkpoint or new topic days, those come first and the problem block is shorter. The schedule already accounts for that.

**Split it if you need to.** For example, do 90 min in the morning with reviews and one problem, then 90 in the evening with the rest. Two sessions beat one tired block.

**Interview this week?** Tell me the company and date. That week we swap some new problems for timed mocks on the topics they're likely to ask.

Missed a day? Don't double up. Do the next Day N tomorrow. The end date slides, that's fine.

---

## Part 5 · Phase 1 schedule

## Week 1

### Day 1 · Wed Nov 04 · Arrays & Hashing (new)
- [ ] Send me `Day 1`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] **Start Arrays & Hashing:** create `01-arrays-hashing/notes.md` and `01-arrays-hashing/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Contains Duplicate [Easy] → `01-arrays-hashing/problems/0217_contains_duplicate.py`  
      https://leetcode.com/problems/contains-duplicate/
- [ ] Valid Anagram [Easy] → `01-arrays-hashing/problems/0242_valid_anagram.py`  
      https://leetcode.com/problems/valid-anagram/
- [ ] Two Sum [Easy] → `01-arrays-hashing/problems/0001_two_sum.py`  
      https://leetcode.com/problems/two-sum/
- [ ] Group Anagrams [Medium] → `01-arrays-hashing/problems/0049_group_anagrams.py`  
      https://leetcode.com/problems/group-anagrams/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 2 · Thu Nov 05 · Arrays & Hashing
- [ ] Send me `Day 2`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Top K Frequent Elements [Medium] → `01-arrays-hashing/problems/0347_top_k_frequent_elements.py`  
      https://leetcode.com/problems/top-k-frequent-elements/
- [ ] Encode and Decode Strings [Medium] → `01-arrays-hashing/problems/0271_encode_and_decode_strings.py`  
      https://leetcode.com/problems/encode-and-decode-strings/ (premium, free at https://neetcode.io/practice)
- [ ] Product of Array Except Self [Medium] → `01-arrays-hashing/problems/0238_product_of_array_except_self.py`  
      https://leetcode.com/problems/product-of-array-except-self/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 3 · Fri Nov 06 · Arrays & Hashing + Checkpoint (Arrays & Hashing) + Two Pointers (new)
- [ ] Send me `Day 3`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Longest Consecutive Sequence [Medium] → `01-arrays-hashing/problems/0128_longest_consecutive_sequence.py`  
      https://leetcode.com/problems/longest-consecutive-sequence/
- [ ] **Checkpoint: Arrays & Hashing.** I give you fresh exercises with asserts. Paste into `01-arrays-hashing/exercises.py`. Pass them without opening old files. Add 3 to 5 sentences of "how I recognize this" to each topic's `notes.md`
- [ ] **Start Two Pointers:** create `02-two-pointers/notes.md` and `02-two-pointers/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 4 · Sat Nov 07 · Two Pointers + Sliding Window (new)
- [ ] Send me `Day 4`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Valid Palindrome [Easy] → `02-two-pointers/problems/0125_valid_palindrome.py`  
      https://leetcode.com/problems/valid-palindrome/
- [ ] 3Sum [Medium] → `02-two-pointers/problems/0015_3sum.py`  
      https://leetcode.com/problems/3sum/
- [ ] Container With Most Water [Medium] → `02-two-pointers/problems/0011_container_with_most_water.py`  
      https://leetcode.com/problems/container-with-most-water/
- [ ] **Start Sliding Window:** create `05-sliding-window/notes.md` and `05-sliding-window/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 5 · Sun Nov 08 · Review + mock day
- [ ] Send me `Day 5`. I pick 4 past problems to re-solve cold
- [ ] Re-solve in `scratch.py`, no notes, no old code
- [ ] One 45 min mock: send me `MOCK` and I act as the interviewer for 2 problems
- [ ] Update `reviews.md`. Re-read `PATTERNS.md`

## Week 2

### Day 6 · Mon Nov 09 · Sliding Window
- [ ] Send me `Day 6`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Best Time to Buy and Sell Stock [Easy] → `05-sliding-window/problems/0121_best_time_to_buy_and_sell_stock.py`  
      https://leetcode.com/problems/best-time-to-buy-and-sell-stock/
- [ ] Longest Substring Without Repeating Characters [Medium] → `05-sliding-window/problems/0003_longest_substring_without_repeating_characters.py`  
      https://leetcode.com/problems/longest-substring-without-repeating-characters/
- [ ] Longest Repeating Character Replacement [Medium] → `05-sliding-window/problems/0424_longest_repeating_character_replacement.py`  
      https://leetcode.com/problems/longest-repeating-character-replacement/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 7 · Tue Nov 10 · Checkpoint (Two Pointers + Sliding Window) + Stack (new)
- [ ] Send me `Day 7`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] **Checkpoint: Two Pointers + Sliding Window.** I give you fresh exercises with asserts. Paste into `02-two-pointers/exercises.py`, `05-sliding-window/exercises.py`. Pass them without opening old files. Add 3 to 5 sentences of "how I recognize this" to each topic's `notes.md`
- [ ] **Start Stack:** create `03-stack/notes.md` and `03-stack/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Valid Parentheses [Easy] → `03-stack/problems/0020_valid_parentheses.py`  
      https://leetcode.com/problems/valid-parentheses/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 8 · Wed Nov 11 · Stack + Binary Search (new)
- [ ] Send me `Day 8`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Min Stack [Medium] → `03-stack/problems/0155_min_stack.py`  
      https://leetcode.com/problems/min-stack/
- [ ] Daily Temperatures [Medium] → `03-stack/problems/0739_daily_temperatures.py`  
      https://leetcode.com/problems/daily-temperatures/
- [ ] **Start Binary Search:** create `04-binary-search/notes.md` and `04-binary-search/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Binary Search [Easy] → `04-binary-search/problems/0704_binary_search.py`  
      https://leetcode.com/problems/binary-search/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 9 · Thu Nov 12 · Binary Search + Checkpoint (Stack + Binary Search)
- [ ] Send me `Day 9`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Find Minimum in Rotated Sorted Array [Medium] → `04-binary-search/problems/0153_find_minimum_in_rotated_sorted_array.py`  
      https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/
- [ ] Search in Rotated Sorted Array [Medium] → `04-binary-search/problems/0033_search_in_rotated_sorted_array.py`  
      https://leetcode.com/problems/search-in-rotated-sorted-array/
- [ ] **Checkpoint: Stack + Binary Search.** I give you fresh exercises with asserts. Paste into `03-stack/exercises.py`, `04-binary-search/exercises.py`. Pass them without opening old files. Add 3 to 5 sentences of "how I recognize this" to each topic's `notes.md`
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 10 · Fri Nov 13 · Linked List (new)
- [ ] Send me `Day 10`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] **Start Linked List:** create `06-linked-list/notes.md` and `06-linked-list/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Reverse Linked List [Easy] → `06-linked-list/problems/0206_reverse_linked_list.py`  
      https://leetcode.com/problems/reverse-linked-list/
- [ ] Merge Two Sorted Lists [Easy] → `06-linked-list/problems/0021_merge_two_sorted_lists.py`  
      https://leetcode.com/problems/merge-two-sorted-lists/
- [ ] Linked List Cycle [Easy] → `06-linked-list/problems/0141_linked_list_cycle.py`  
      https://leetcode.com/problems/linked-list-cycle/
- [ ] Reorder List [Medium] → `06-linked-list/problems/0143_reorder_list.py`  
      https://leetcode.com/problems/reorder-list/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 11 · Sat Nov 14 · Linked List + Checkpoint (Linked List)
- [ ] Send me `Day 11`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Remove Nth Node From End of List [Medium] → `06-linked-list/problems/0019_remove_nth_node_from_end_of_list.py`  
      https://leetcode.com/problems/remove-nth-node-from-end-of-list/
- [ ] LRU Cache [Medium] → `06-linked-list/problems/0146_lru_cache.py`  
      https://leetcode.com/problems/lru-cache/
- [ ] **Checkpoint: Linked List.** I give you fresh exercises with asserts. Paste into `06-linked-list/exercises.py`. Pass them without opening old files. Add 3 to 5 sentences of "how I recognize this" to each topic's `notes.md`
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 12 · Sun Nov 15 · Review + mock day
- [ ] Send me `Day 12`. I pick 4 past problems to re-solve cold
- [ ] Re-solve in `scratch.py`, no notes, no old code
- [ ] One 45 min mock: send me `MOCK` and I act as the interviewer for 2 problems
- [ ] Update `reviews.md`. Re-read `PATTERNS.md`

## Week 3

### Day 13 · Mon Nov 16 · Trees (new)
- [ ] Send me `Day 13`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] **Start Trees:** create `07-trees/notes.md` and `07-trees/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Invert Binary Tree [Easy] → `07-trees/problems/0226_invert_binary_tree.py`  
      https://leetcode.com/problems/invert-binary-tree/
- [ ] Maximum Depth of Binary Tree [Easy] → `07-trees/problems/0104_maximum_depth_of_binary_tree.py`  
      https://leetcode.com/problems/maximum-depth-of-binary-tree/
- [ ] Same Tree [Easy] → `07-trees/problems/0100_same_tree.py`  
      https://leetcode.com/problems/same-tree/
- [ ] Subtree of Another Tree [Easy] → `07-trees/problems/0572_subtree_of_another_tree.py`  
      https://leetcode.com/problems/subtree-of-another-tree/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 14 · Tue Nov 17 · Trees
- [ ] Send me `Day 14`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Lowest Common Ancestor of a BST [Medium] → `07-trees/problems/0235_lowest_common_ancestor_of_a_binary_search_tree.py`  
      https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/
- [ ] Binary Tree Level Order Traversal [Medium] → `07-trees/problems/0102_binary_tree_level_order_traversal.py`  
      https://leetcode.com/problems/binary-tree-level-order-traversal/
- [ ] Validate Binary Search Tree [Medium] → `07-trees/problems/0098_validate_binary_search_tree.py`  
      https://leetcode.com/problems/validate-binary-search-tree/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 15 · Wed Nov 18 · Trees + Checkpoint (Trees)
- [ ] Send me `Day 15`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Kth Smallest Element in a BST [Medium] → `07-trees/problems/0230_kth_smallest_element_in_a_bst.py`  
      https://leetcode.com/problems/kth-smallest-element-in-a-bst/
- [ ] Construct Binary Tree from Preorder and Inorder [Medium] → `07-trees/problems/0105_construct_binary_tree_from_preorder_and_inorder_traversal.py`  
      https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/
- [ ] **Checkpoint: Trees.** I give you fresh exercises with asserts. Paste into `07-trees/exercises.py`. Pass them without opening old files. Add 3 to 5 sentences of "how I recognize this" to each topic's `notes.md`
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 16 · Thu Nov 19 · Tries (new)
- [ ] Send me `Day 16`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] **Start Tries:** create `08-tries/notes.md` and `08-tries/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Implement Trie (Prefix Tree) [Medium] → `08-tries/problems/0208_implement_trie_prefix_tree.py`  
      https://leetcode.com/problems/implement-trie-prefix-tree/
- [ ] Design Add and Search Words [Medium] → `08-tries/problems/0211_design_add_and_search_words_data_structure.py`  
      https://leetcode.com/problems/design-add-and-search-words-data-structure/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 17 · Fri Nov 20 · Heap / Priority Queue (new)
- [ ] Send me `Day 17`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] **Start Heap / Priority Queue:** create `09-heap/notes.md` and `09-heap/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] K Closest Points to Origin [Medium] → `09-heap/problems/0973_k_closest_points_to_origin.py`  
      https://leetcode.com/problems/k-closest-points-to-origin/
- [ ] Kth Largest Element in an Array [Medium] → `09-heap/problems/0215_kth_largest_element_in_an_array.py`  
      https://leetcode.com/problems/kth-largest-element-in-an-array/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 18 · Sat Nov 21 · Checkpoint (Tries + Heap / Priority Queue) + Backtracking (new)
- [ ] Send me `Day 18`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] **Checkpoint: Tries + Heap / Priority Queue.** I give you fresh exercises with asserts. Paste into `08-tries/exercises.py`, `09-heap/exercises.py`. Pass them without opening old files. Add 3 to 5 sentences of "how I recognize this" to each topic's `notes.md`
- [ ] **Start Backtracking:** create `10-backtracking/notes.md` and `10-backtracking/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Combination Sum [Medium] → `10-backtracking/problems/0039_combination_sum.py`  
      https://leetcode.com/problems/combination-sum/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 19 · Sun Nov 22 · Review + mock day
- [ ] Send me `Day 19`. I pick 4 past problems to re-solve cold
- [ ] Re-solve in `scratch.py`, no notes, no old code
- [ ] One 45 min mock: send me `MOCK` and I act as the interviewer for 2 problems
- [ ] Update `reviews.md`. Re-read `PATTERNS.md`

## Week 4

### Day 20 · Mon Nov 23 · Backtracking + Checkpoint (Backtracking) + Graphs (new)
- [ ] Send me `Day 20`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Word Search [Medium] → `10-backtracking/problems/0079_word_search.py`  
      https://leetcode.com/problems/word-search/
- [ ] **Checkpoint: Backtracking.** I give you fresh exercises with asserts. Paste into `10-backtracking/exercises.py`. Pass them without opening old files. Add 3 to 5 sentences of "how I recognize this" to each topic's `notes.md`
- [ ] **Start Graphs:** create `11-graphs/notes.md` and `11-graphs/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 21 · Tue Nov 24 · Graphs
- [ ] Send me `Day 21`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Number of Islands [Medium] → `11-graphs/problems/0200_number_of_islands.py`  
      https://leetcode.com/problems/number-of-islands/
- [ ] Clone Graph [Medium] → `11-graphs/problems/0133_clone_graph.py`  
      https://leetcode.com/problems/clone-graph/
- [ ] Rotting Oranges [Medium] → `11-graphs/problems/0994_rotting_oranges.py`  
      https://leetcode.com/problems/rotting-oranges/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 22 · Wed Nov 25 · Graphs
- [ ] Send me `Day 22`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Pacific Atlantic Water Flow [Medium] → `11-graphs/problems/0417_pacific_atlantic_water_flow.py`  
      https://leetcode.com/problems/pacific-atlantic-water-flow/
- [ ] Course Schedule [Medium] → `11-graphs/problems/0207_course_schedule.py`  
      https://leetcode.com/problems/course-schedule/
- [ ] Graph Valid Tree [Medium] → `11-graphs/problems/0261_graph_valid_tree.py`  
      https://leetcode.com/problems/graph-valid-tree/ (premium, free at https://neetcode.io/practice)
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Thu Nov 26 · OFF (Thanksgiving)

### Day 23 · Fri Nov 27 · Graphs + Checkpoint (Graphs) + 1-D Dynamic Programming (new)
- [ ] Send me `Day 23`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Number of Connected Components [Medium] → `11-graphs/problems/0323_number_of_connected_components_in_an_undirected_graph.py`  
      https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/ (premium, free at https://neetcode.io/practice)
- [ ] **Checkpoint: Graphs.** I give you fresh exercises with asserts. Paste into `11-graphs/exercises.py`. Pass them without opening old files. Add 3 to 5 sentences of "how I recognize this" to each topic's `notes.md`
- [ ] **Start 1-D Dynamic Programming:** create `12-1d-dp/notes.md` and `12-1d-dp/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 24 · Sat Nov 28 · 1-D Dynamic Programming
- [ ] Send me `Day 24`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Climbing Stairs [Easy] → `12-1d-dp/problems/0070_climbing_stairs.py`  
      https://leetcode.com/problems/climbing-stairs/
- [ ] House Robber [Medium] → `12-1d-dp/problems/0198_house_robber.py`  
      https://leetcode.com/problems/house-robber/
- [ ] House Robber II [Medium] → `12-1d-dp/problems/0213_house_robber_ii.py`  
      https://leetcode.com/problems/house-robber-ii/
- [ ] Longest Palindromic Substring [Medium] → `12-1d-dp/problems/0005_longest_palindromic_substring.py`  
      https://leetcode.com/problems/longest-palindromic-substring/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 25 · Sun Nov 29 · Review + mock day
- [ ] Send me `Day 25`. I pick 4 past problems to re-solve cold
- [ ] Re-solve in `scratch.py`, no notes, no old code
- [ ] One 45 min mock: send me `MOCK` and I act as the interviewer for 2 problems
- [ ] Update `reviews.md`. Re-read `PATTERNS.md`

## Week 5

### Day 26 · Mon Nov 30 · 1-D Dynamic Programming
- [ ] Send me `Day 26`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Palindromic Substrings [Medium] → `12-1d-dp/problems/0647_palindromic_substrings.py`  
      https://leetcode.com/problems/palindromic-substrings/
- [ ] Decode Ways [Medium] → `12-1d-dp/problems/0091_decode_ways.py`  
      https://leetcode.com/problems/decode-ways/
- [ ] Coin Change [Medium] → `12-1d-dp/problems/0322_coin_change.py`  
      https://leetcode.com/problems/coin-change/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 27 · Tue Dec 01 · 1-D Dynamic Programming
- [ ] Send me `Day 27`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Maximum Product Subarray [Medium] → `12-1d-dp/problems/0152_maximum_product_subarray.py`  
      https://leetcode.com/problems/maximum-product-subarray/
- [ ] Word Break [Medium] → `12-1d-dp/problems/0139_word_break.py`  
      https://leetcode.com/problems/word-break/
- [ ] Longest Increasing Subsequence [Medium] → `12-1d-dp/problems/0300_longest_increasing_subsequence.py`  
      https://leetcode.com/problems/longest-increasing-subsequence/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 28 · Wed Dec 02 · Checkpoint (1-D Dynamic Programming) + Intervals (new)
- [ ] Send me `Day 28`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] **Checkpoint: 1-D Dynamic Programming.** I give you fresh exercises with asserts. Paste into `12-1d-dp/exercises.py`. Pass them without opening old files. Add 3 to 5 sentences of "how I recognize this" to each topic's `notes.md`
- [ ] **Start Intervals:** create `13-intervals/notes.md` and `13-intervals/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Insert Interval [Medium] → `13-intervals/problems/0057_insert_interval.py`  
      https://leetcode.com/problems/insert-interval/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 29 · Thu Dec 03 · Intervals
- [ ] Send me `Day 29`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Merge Intervals [Medium] → `13-intervals/problems/0056_merge_intervals.py`  
      https://leetcode.com/problems/merge-intervals/
- [ ] Non-overlapping Intervals [Medium] → `13-intervals/problems/0435_non_overlapping_intervals.py`  
      https://leetcode.com/problems/non-overlapping-intervals/
- [ ] Meeting Rooms [Easy] → `13-intervals/problems/0252_meeting_rooms.py`  
      https://leetcode.com/problems/meeting-rooms/ (premium, free at https://neetcode.io/practice)
- [ ] Meeting Rooms II [Medium] → `13-intervals/problems/0253_meeting_rooms_ii.py`  
      https://leetcode.com/problems/meeting-rooms-ii/ (premium, free at https://neetcode.io/practice)
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 30 · Fri Dec 04 · Greedy (new)
- [ ] Send me `Day 30`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] **Start Greedy:** create `14-greedy/notes.md` and `14-greedy/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Maximum Subarray [Medium] → `14-greedy/problems/0053_maximum_subarray.py`  
      https://leetcode.com/problems/maximum-subarray/
- [ ] Jump Game [Medium] → `14-greedy/problems/0055_jump_game.py`  
      https://leetcode.com/problems/jump-game/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 31 · Sat Dec 05 · Checkpoint (Intervals + Greedy) + 2-D Dynamic Programming (new)
- [ ] Send me `Day 31`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] **Checkpoint: Intervals + Greedy.** I give you fresh exercises with asserts. Paste into `13-intervals/exercises.py`, `14-greedy/exercises.py`. Pass them without opening old files. Add 3 to 5 sentences of "how I recognize this" to each topic's `notes.md`
- [ ] **Start 2-D Dynamic Programming:** create `16-2d-dp/notes.md` and `16-2d-dp/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Unique Paths [Medium] → `16-2d-dp/problems/0062_unique_paths.py`  
      https://leetcode.com/problems/unique-paths/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 32 · Sun Dec 06 · Review + mock day
- [ ] Send me `Day 32`. I pick 4 past problems to re-solve cold
- [ ] Re-solve in `scratch.py`, no notes, no old code
- [ ] One 45 min mock: send me `MOCK` and I act as the interviewer for 2 problems
- [ ] Update `reviews.md`. Re-read `PATTERNS.md`

## Week 6

### Day 33 · Mon Dec 07 · 2-D Dynamic Programming + Math & Geometry (new)
- [ ] Send me `Day 33`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Longest Common Subsequence [Medium] → `16-2d-dp/problems/1143_longest_common_subsequence.py`  
      https://leetcode.com/problems/longest-common-subsequence/
- [ ] **Start Math & Geometry:** create `18-math-geometry/notes.md` and `18-math-geometry/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Rotate Image [Medium] → `18-math-geometry/problems/0048_rotate_image.py`  
      https://leetcode.com/problems/rotate-image/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 34 · Tue Dec 08 · Math & Geometry + Bit Manipulation (new)
- [ ] Send me `Day 34`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Spiral Matrix [Medium] → `18-math-geometry/problems/0054_spiral_matrix.py`  
      https://leetcode.com/problems/spiral-matrix/
- [ ] Set Matrix Zeroes [Medium] → `18-math-geometry/problems/0073_set_matrix_zeroes.py`  
      https://leetcode.com/problems/set-matrix-zeroes/
- [ ] **Start Bit Manipulation:** create `17-bit-manipulation/notes.md` and `17-bit-manipulation/problems/`. I teach the pattern and give you notes. Answer my 3 check questions
- [ ] Number of 1 Bits [Easy] → `17-bit-manipulation/problems/0191_number_of_1_bits.py`  
      https://leetcode.com/problems/number-of-1-bits/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 35 · Wed Dec 09 · Bit Manipulation
- [ ] Send me `Day 35`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] Counting Bits [Easy] → `17-bit-manipulation/problems/0338_counting_bits.py`  
      https://leetcode.com/problems/counting-bits/
- [ ] Reverse Bits [Easy] → `17-bit-manipulation/problems/0190_reverse_bits.py`  
      https://leetcode.com/problems/reverse-bits/
- [ ] Missing Number [Easy] → `17-bit-manipulation/problems/0268_missing_number.py`  
      https://leetcode.com/problems/missing-number/
- [ ] Sum of Two Integers [Medium] → `17-bit-manipulation/problems/0371_sum_of_two_integers.py`  
      https://leetcode.com/problems/sum-of-two-integers/
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

### Day 36 · Thu Dec 10 · Checkpoint (2-D Dynamic Programming + Math & Geometry + Bit Manipulation)
- [ ] Send me `Day 36`
- [ ] Warm up: re-solve anything due in `reviews.md` (max 3)
- [ ] **Checkpoint: 2-D Dynamic Programming + Math & Geometry + Bit Manipulation.** I give you fresh exercises with asserts. Paste into `16-2d-dp/exercises.py`, `18-math-geometry/exercises.py`, `17-bit-manipulation/exercises.py`. Pass them without opening old files. Add 3 to 5 sentences of "how I recognize this" to each topic's `notes.md`
- [ ] Rows in `PATTERNS.md` + `reviews.md`. Commit and push

---

## Part 6 · Phase 2: solo pass (starts Fri Dec 11)

Same folders, same file template. Strict timebox first, then one hint at most. Log your honest confidence in `reviews.md`. About 5 a day at 3 hours gets you through it in under 2 weeks. Keep Sundays as review + mock days.


**Arrays & Hashing** → `01-arrays-hashing/problems/`
- [ ] Valid Sudoku [Medium] https://leetcode.com/problems/valid-sudoku/

**Two Pointers** → `02-two-pointers/problems/`
- [ ] Two Sum II [Medium] https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/

**Sliding Window** → `05-sliding-window/problems/`
- [ ] Permutation in String [Medium] https://leetcode.com/problems/permutation-in-string/

**Stack** → `03-stack/problems/`
- [ ] Evaluate Reverse Polish Notation [Medium] https://leetcode.com/problems/evaluate-reverse-polish-notation/
- [ ] Generate Parentheses [Medium] https://leetcode.com/problems/generate-parentheses/
- [ ] Car Fleet [Medium] https://leetcode.com/problems/car-fleet/

**Binary Search** → `04-binary-search/problems/`
- [ ] Search a 2D Matrix [Medium] https://leetcode.com/problems/search-a-2d-matrix/
- [ ] Koko Eating Bananas [Medium] https://leetcode.com/problems/koko-eating-bananas/
- [ ] Time Based Key-Value Store [Medium] https://leetcode.com/problems/time-based-key-value-store/

**Linked List** → `06-linked-list/problems/`
- [ ] Copy List with Random Pointer [Medium] https://leetcode.com/problems/copy-list-with-random-pointer/
- [ ] Add Two Numbers [Medium] https://leetcode.com/problems/add-two-numbers/
- [ ] Find the Duplicate Number [Medium] https://leetcode.com/problems/find-the-duplicate-number/

**Trees** → `07-trees/problems/`
- [ ] Diameter of Binary Tree [Easy] https://leetcode.com/problems/diameter-of-binary-tree/
- [ ] Balanced Binary Tree [Easy] https://leetcode.com/problems/balanced-binary-tree/
- [ ] Binary Tree Right Side View [Medium] https://leetcode.com/problems/binary-tree-right-side-view/
- [ ] Count Good Nodes in Binary Tree [Medium] https://leetcode.com/problems/count-good-nodes-in-binary-tree/

**Heap / Priority Queue** → `09-heap/problems/`
- [ ] Kth Largest Element in a Stream [Easy] https://leetcode.com/problems/kth-largest-element-in-a-stream/
- [ ] Last Stone Weight [Easy] https://leetcode.com/problems/last-stone-weight/
- [ ] Task Scheduler [Medium] https://leetcode.com/problems/task-scheduler/
- [ ] Design Twitter [Medium] https://leetcode.com/problems/design-twitter/

**Backtracking** → `10-backtracking/problems/`
- [ ] Subsets [Medium] https://leetcode.com/problems/subsets/
- [ ] Combination Sum II [Medium] https://leetcode.com/problems/combination-sum-ii/
- [ ] Permutations [Medium] https://leetcode.com/problems/permutations/
- [ ] Subsets II [Medium] https://leetcode.com/problems/subsets-ii/
- [ ] Palindrome Partitioning [Medium] https://leetcode.com/problems/palindrome-partitioning/
- [ ] Letter Combinations of a Phone Number [Medium] https://leetcode.com/problems/letter-combinations-of-a-phone-number/

**Graphs** → `11-graphs/problems/`
- [ ] Max Area of Island [Medium] https://leetcode.com/problems/max-area-of-island/
- [ ] Walls and Gates [Medium] https://leetcode.com/problems/walls-and-gates/ (premium, free at https://neetcode.io/practice)
- [ ] Surrounded Regions [Medium] https://leetcode.com/problems/surrounded-regions/
- [ ] Course Schedule II [Medium] https://leetcode.com/problems/course-schedule-ii/
- [ ] Redundant Connection [Medium] https://leetcode.com/problems/redundant-connection/

**1-D Dynamic Programming** → `12-1d-dp/problems/`
- [ ] Min Cost Climbing Stairs [Easy] https://leetcode.com/problems/min-cost-climbing-stairs/
- [ ] Partition Equal Subset Sum [Medium] https://leetcode.com/problems/partition-equal-subset-sum/

**Greedy** → `14-greedy/problems/`
- [ ] Jump Game II [Medium] https://leetcode.com/problems/jump-game-ii/
- [ ] Gas Station [Medium] https://leetcode.com/problems/gas-station/
- [ ] Hand of Straights [Medium] https://leetcode.com/problems/hand-of-straights/
- [ ] Merge Triplets to Form Target Triplet [Medium] https://leetcode.com/problems/merge-triplets-to-form-target-triplet/
- [ ] Partition Labels [Medium] https://leetcode.com/problems/partition-labels/
- [ ] Valid Parenthesis String [Medium] https://leetcode.com/problems/valid-parenthesis-string/

**2-D Dynamic Programming** → `16-2d-dp/problems/`
- [ ] Best Time to Buy and Sell Stock with Cooldown [Medium] https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-cooldown/
- [ ] Coin Change II [Medium] https://leetcode.com/problems/coin-change-ii/
- [ ] Target Sum [Medium] https://leetcode.com/problems/target-sum/
- [ ] Interleaving String [Medium] https://leetcode.com/problems/interleaving-string/
- [ ] Edit Distance [Medium] https://leetcode.com/problems/edit-distance/

**Math & Geometry** → `18-math-geometry/problems/`
- [ ] Happy Number [Easy] https://leetcode.com/problems/happy-number/
- [ ] Plus One [Easy] https://leetcode.com/problems/plus-one/
- [ ] Pow(x, n) [Medium] https://leetcode.com/problems/powx-n/
- [ ] Multiply Strings [Medium] https://leetcode.com/problems/multiply-strings/
- [ ] Detect Squares [Medium] https://leetcode.com/problems/detect-squares/

**Bit Manipulation** → `17-bit-manipulation/problems/`
- [ ] Single Number [Easy] https://leetcode.com/problems/single-number/
- [ ] Reverse Integer [Medium] https://leetcode.com/problems/reverse-integer/

---

## Part 7 · Hards (optional)

- [ ] Trapping Rain Water [Two Pointers] https://leetcode.com/problems/trapping-rain-water/
- [ ] Minimum Window Substring [Sliding Window] https://leetcode.com/problems/minimum-window-substring/
- [ ] Sliding Window Maximum [Sliding Window] https://leetcode.com/problems/sliding-window-maximum/
- [ ] Largest Rectangle in Histogram [Stack] https://leetcode.com/problems/largest-rectangle-in-histogram/
- [ ] Median of Two Sorted Arrays [Binary Search] https://leetcode.com/problems/median-of-two-sorted-arrays/
- [ ] Merge K Sorted Lists [Linked List] https://leetcode.com/problems/merge-k-sorted-lists/
- [ ] Reverse Nodes in K-Group [Linked List] https://leetcode.com/problems/reverse-nodes-in-k-group/
- [ ] Binary Tree Maximum Path Sum [Trees] https://leetcode.com/problems/binary-tree-maximum-path-sum/
- [ ] Serialize and Deserialize Binary Tree [Trees] https://leetcode.com/problems/serialize-and-deserialize-binary-tree/
- [ ] Word Search II [Tries] https://leetcode.com/problems/word-search-ii/
- [ ] Find Median from Data Stream [Heap / Priority Queue] https://leetcode.com/problems/find-median-from-data-stream/
- [ ] N-Queens [Backtracking] https://leetcode.com/problems/n-queens/
- [ ] Word Ladder [Graphs] https://leetcode.com/problems/word-ladder/
- [ ] Minimum Interval to Include Each Query [Intervals] https://leetcode.com/problems/minimum-interval-to-include-each-query/
- [ ] Longest Increasing Path in a Matrix [2-D Dynamic Programming] https://leetcode.com/problems/longest-increasing-path-in-a-matrix/
- [ ] Distinct Subsequences [2-D Dynamic Programming] https://leetcode.com/problems/distinct-subsequences/
- [ ] Burst Balloons [2-D Dynamic Programming] https://leetcode.com/problems/burst-balloons/
- [ ] Regular Expression Matching [2-D Dynamic Programming] https://leetcode.com/problems/regular-expression-matching/