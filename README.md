# SASS list-reverse function
SASS function to reverse the order of a list.
## Usage
```
    list-reverse($list);
    $a: (1,2,3,4);
    list-reverse($a) = (4,3,2,1);
    list-reverse('not a list') = (); // and a @warn
```
## Method
```
  @if(type-of($a) == 'list'){
    $i: length($a);
    $r: ();
    @while($i > 0){
      $r: append($r, nth($a, $i));
      $i: $i - 1; }
    @return $r;
  } @else { 
    @warn "list-reverse: not supplied a list"; 
    @return $a; }
```
## Issues
* None known
