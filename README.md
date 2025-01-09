# Counting-Words-With-a-Given-Prefix

You are given an array of strings words and a string pref.
Return the number of strings in words that contain pref as a prefix.
A prefix of a string s is any leading contiguous substring of s.

class Solution:

    def prefixCount(self, words: list[str], pref: str) -> int:
        c = 0
        n = len(pref)
        for word in words:
            if len(word) >= n and word[:n] == pref:
                c += 1
        return c
