# CMPS 6610 Problem Set 03
## Answers

**Name: Qi An Ong


Place all written answers from `problemset-03.md` here for easier grading.




- **1b.**
Both the work and span are $O(n)$




- **1d.**
work is $O(n)$ , Span is $O(log(n))$




- **1e.**
${W(n) = W(n/3) + W(2n/3) + O(1) = O(n)}$
${S(n) = S(2n/3) + O(1) = O(log(n))}$


- **2a.**
```
def dedup(A):
    seen_ele = set()
    ans = []
    for x in A:
        if x not in seen_ele:
            seen_ele.add(x)
            ans.append(x)
    return ans
```

${W(n) = O(n)}$ check each in array element once
${S(n) = O(n)}$


- **2b.**
```
def multi_dedup(A):
    combined_list = [ele for sublist in A for ele in sublist]

    return list(set(combined_list))
```
${W(n) = O(n)}$ let n be total number of elements in all the list. Iterate through all the elements once so O(n).
${S(n) = O(log(n))}$  can merge in parallel in binary tree fashion.
Overall, both multi dedup and dedup have same work asymp time but the span is faster for multi dedup, log(n) instead as it can be done in parallel.

- **2c.**
For dedup, iterate is useful as it can be used to scan through the array and accumulating the results, filter is less useful as it is inefficient unless used with a seen set. Map is also not useful as need to check previous elements. Flatten might be useful if the algo were to spit the array into chunks then deduplicate each chunk seperate.
For multi-dedup, flatten is useful as the algo first flattens all the list into a single one. ITerate is also useful as after, iterate throguh the list to accumulate unique elements. Map might be useful if applied in parallel. Filter is not useful as require a seen set.



- **3b.**
${W(n) = W(n-1) + O(1) = O(n)}$
${S(n) = S(n-1) + O(1) = O(n)}$ 



- **3d.**
map each element in list once using parem map so O(n) to map list
for scan, from the class, work is O(n), span is O(log(n)). Lastly, to check all prefix sums are non negative, parallelized sequences, span takes O(log(n))
${W(n) = O(n)}$
${S(n) = O(log(n))}$ 




- **3f.**
${W(n) = 2W(n/2) + O(1) = O(n)}$
${S(n) = S(n/2) + O(1) = O(log(n))}$




