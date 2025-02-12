# [392. Is Subsequence](https://leetcode.com/problems/is-subsequence)

[中文文档](/solution/0300-0399/0392.Is%20Subsequence/README.md)

## Description

<p>Given two strings <code>s</code> and <code>t</code>, check if <code>s</code> is a <strong>subsequence</strong> of <code>t</code>.</p>

<p>A <strong>subsequence</strong> of a string is a new string that is formed from the original string by deleting some (can be none) of the characters without disturbing the relative positions of the remaining characters. (i.e., <code>&quot;ace&quot;</code> is a subsequence of <code>&quot;abcde&quot;</code> while <code>&quot;aec&quot;</code> is not).</p>

<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>
<pre><strong>Input:</strong> s = "abc", t = "ahbgdc"
<strong>Output:</strong> true
</pre><p><strong>Example 2:</strong></p>
<pre><strong>Input:</strong> s = "axc", t = "ahbgdc"
<strong>Output:</strong> false
</pre>
<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>0 &lt;= s.length &lt;= 100</code></li>
	<li><code>0 &lt;= t.length &lt;= 10<sup>4</sup></code></li>
	<li><code>s</code> and <code>t</code>&nbsp;consist&nbsp;only of lowercase English letters.</li>
</ul>

<p>&nbsp;</p>
<strong>Follow up:</strong> If there are lots of incoming <code>s</code>, say <code>s<sub>1</sub>, s<sub>2</sub>, ..., s<sub>k</sub></code> where <code>k &gt;= 10<sup>9</sup></code>, and you want to check one by one to see if <code>t</code> has its subsequence. In this scenario, how would you change your code?

## Solutions

<!-- tabs:start -->

### **Python3**

```python
class Solution:
    def isSubsequence(self, s: str, t: str) -> bool:
        m, n = len(s), len(t)
        i = j = 0
        while i < m and j < n:
            if s[i] == t[j]:
                i += 1
            j += 1
        return i == m
```

### **Java**

```java
class Solution {
    public boolean isSubsequence(String s, String t) {
        int m = s.length(), n = t.length();
        int i = 0, j = 0;
        while (i < m && j < n) {
            if (s.charAt(i) == t.charAt(j)) {
                ++i;
            }
            ++j;
        }
        return i == m;
    }
}
```

### **C++**

```cpp
class Solution {
public:
    bool isSubsequence(string s, string t) {
        int m = s.size(), n = t.size();
        int i = 0, j = 0;
        while (i < m && j < n) {
            if (s[i] == t[j]) {
                ++i;
            }
            ++j;
        }
        return i == m;
    }
};
```

### **Go**

```go
func isSubsequence(s string, t string) bool {
	i, j, m, n := 0, 0, len(s), len(t)
	for i < m && j < n {
		if s[i] == t[j] {
			i++
		}
		j++
	}
	return i == m
}
```

### **...**

```

```

<!-- tabs:end -->
