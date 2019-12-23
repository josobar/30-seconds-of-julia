---
title:is_anagram
tags:string,intermediate
---

Checks if an array contains any duplicate elements

```jl
function has_duplicates(a::Array)
    return length(Set(a)) != length(a)
end
```
