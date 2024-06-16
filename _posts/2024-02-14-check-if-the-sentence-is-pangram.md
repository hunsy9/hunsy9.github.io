---
title: "[LeetCode] Check if the Sentence is Pangram"
date: 2024-02-14 11:48:00 +/-TTTT
categories: [Algorithm, LeetCode]
tags: [Hashing]     # TAG names should always be lowercase
image:
  path: /assets/img/algorithm/leetcode.png
  alt: LeetCode
---

**문제 설명**:
A pangram is a sentence where every letter of the English alphabet appears at least once.

Given a string ```sentence``` containing only lowercase English letters, return ```true``` if ```sentence``` is a pangram, or ```false``` otherwise.

**제약 조건**
- ```1 <= sentence.length <= 1000```
- ```sentence``` consists of lowercase English letters

**난이도**: ```EASY```

  <br>
  <br>

## 문제 이해
---
- pangram은 모든 영어 알파벳이 적어도 한번 나오는 문장을 의미한다.

<br>

## 문제를 보며 처음 한 생각
---
영어 알파벳을 어떻게 저장하지? -> set

영어 알파벳이 총 몇 개지? -> 26개

위 두 가지 과정을 거쳐서 set에 sentence를 for 문으로 훑으면서 set에 다 넣는다.

그리고 set의 length가 26개면 true 반환, 아니면 false 반환
<br>


## 문제를 해결한 방법
---
처음 한 생각이 맞았어서 코드를 첨부한다.

```python
class Solution:
    def checkIfPangram(self, sentence: str) -> bool:
        checkPangram = set()
        for i in range(len(sentence)):
            checkPangram.add(sentence[i])
        return len(checkPangram) == 26
```

<br>
