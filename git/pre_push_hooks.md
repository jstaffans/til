# Prevent silliness from reaching origin with pre-push hooks

When coding, I sometimes forget to remove debug printouts (e.g. `#spy` in Clojure)
before pushing stuff to Github. Solution: pre-push hooks that ensure no silly stuff
is in the push.

http://jegtnes.co.uk/blog/use-git-pre-push-hooks-to-stop-test-suite-skips/
