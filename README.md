# pylcs
This is a fork of [pylcs](https://github.com/Meteorix/pylcs)
The main change is that the `lcs_str2id` accept two arrays rather than two strings. `lcs_str2id` is from [here](https://github.com/Meteorix/pylcs/issues/4) by [Laser-cat](https://github.com/Laser-Cat).
`lcs_str2id` returns the index of the longest common elements of the second array.


Install
-------
Python3 is required.
To install:
```bash
git clone
cd pylcs
python setup.py install --user
```



Python code example
-------------------

```python
import pylcs

#  the original method of lcs
#  finding the longest common subsequence length of string A and string B
A = 'We are shannonai'
B = 'We like shannonai'
pylcs.lcs(A, B)
"""
>>> pylcs.lcs(A, B)
14
"""

# lcs of two arrays
A = list('We are shannonai')
B = list('We like shannonai')
index_LB=pylcs.lcs_of_list(A, B)
index_LA=pylcs.lcs_of_list(B, A)
index_LB
index_LA
"""
>>> index_LB
>>> index_LA
[0, 1, 2, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16]
[0, 1, 2, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]
"""


