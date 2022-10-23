1. 'values added: 20'. There shouldn't be any reason why this doesn't print because result is indeed 10 + 10 = 20 and that was successfully stored into
result and then printed to the command line. All good here.
2. 'final added: 20'. In other programming languages, since result is declared inside of the if statement, there should be an error since it's out of scope here, but var allows its value to be hoisted and therefore it can be accessed outside of its scope as long as it's still in the same function scope
3. 'values added: 20'. For the exact same reason, it prints because we are able to successfully store result since it's in the same scope and we can print result.
4. It returns an error. This is because of the fact that let limits itself to the bracket scope so after the if statement terminates, results is deleted and we can't access it.
5. It returns an error. By definition, a const variable is constant, meaning that it cannot be changed ever, so when it's forced to change, it causes an error. Otherwise, it would return 'values added: 0' if we didn't add, which is expected since it was set as 0 earlier on
6. It returns an error. Again, since const has let's scoping, it becomes unavailable after its scope is terminated, so it can't be accessed at line 13
