### Properties:


##### id: 202410070013_closure_use_case
##### hubs: [[javascript.md]], [[lexical_env]], [[closure]]
##### source:  https://www.codeguage.com/courses/js/functions-closures

### Content:

**Functions returning other functions** are perhaps one of the most common applications of closures in JavaScript programs. It's highly likely that once you start building complex programs, you'd use them too.


```js
function f1() {
   var a = 'difficult';

   return function() {
      console.log(a);
   };
}

var a = 'easy';
var f2 = f1();

f2();
```

because of the return of anonymous function inside ``f1`` which have lexical env is local ``f1`` env, and the anonymous function still be referenced by ``f2 = f1()`` => the local environment of ``f1()`` isn't garbage collected (still reachable)

[[202410041328_unreachable_definition.md]]
[[202410061918_lexical_env_garbage_collector]]