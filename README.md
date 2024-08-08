# check_shuffle

Helper library that validates two arrays contain equivalent values, but not in any particular order

# Usage

```
use dep::check_shuffle::check_shuffle;

fn good() {
    let a: [Field; 5] = [0,1,2,3,4];
    let b: [Field; 5] = [2,1,4,3,0];
    check_shuffle(a, b); // works
}


fn bad() {
    let a: [Field; 5] = [0,1,2,3,4];
    let b: [Field; 5] = [0,0,2,3,4];
    check_shuffle(a, b); // constraints not satisfied. b is not a shuffled version of a
}
```
