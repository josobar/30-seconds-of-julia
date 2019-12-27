---
title: lucas
tags: math,intermediate
---

Returns an array of Lucas numbers with a length of ```n```

Initialize an array `l` with elements ```[2,1]```. For each number from 3 to ```n```,
use ```append!``` to join `l` with the sum of its two latest elements. 

```jl
function lucas(n)
  l = [2,1]
  if n <= 2 && n > 0
    return l[n]
  end
  for i in 3:n
    append!(l, l[i-2] + l[i-1])
  end
  return l
end
```

```jl
lucas(1) #[1]
lucas(5) #[2,1,3,4,7]
```
