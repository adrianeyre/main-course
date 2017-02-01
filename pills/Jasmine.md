# Jasmine Test Framework

## Test Example
```
describe("Description of the test", function() {
  beforeEach(function() {

  });

  it("test outcome", function() {
    expect(true).toBe(true);
  });
});
```

## Expect syntax
`.toBe(true)` = To be true/false<br>
`.not.toBe(true)` = To not be true/false<br>
##
`.toEqual("result")` = To equal result<br>
`.not.toEqual("result")` = To not equal result<br>
##
`.toContain(item)` = To contain item<br>
`.not.toContain(item)` To not contain item<br>
##
`.toMatch(/item/)` = To match item<br>
`.not.toMatch(/bar/)` = To not match item<br>
##
`.toBeDefined()` = To be defined<br>
`.not.toBeDefined()` = To not be defined<br>
##
`.toBeUndefined()` = To be undifined<br>
`.not.toBeUndefined()` = To not be undifined<br>
##
`.toBeNull()` = To be Null<br>
`.not.toBeNull()` = to Not be Null<br>
##
`.toBeTruthy()` = Result to be a boolean<br>
`.not.toBeTruthy()` = Result not to be a boolean<br>
##
`.toBeFalsy()` = Result to be a boolean<br>
`.not.toBeFalsy()` = Result not to be a boolean<br>
##
`.toBeLessThan(value)` = To be less than the value<br>
 `.not.toBeLessThan(value)` = To not be less than the value<br>
##
`.toBeGreaterThan(value)` = To be greater than the value<br>
`.not.toBeGreaterThan(value)` = To not be greater than the value<br>
##
`.toBeCloseTo(v1, v2)` = To be close to v1 and v2<br>
`.not.toBeCloseTo(v1, v2)` = To not be close to v1 and v2<br>
##
 `throw 'error'` = usage<br>
`.toThrow(error)` = To throw error<br>
`.not.toThrow(error)` = To not throw error<br>
##
`throw new TypeError("error")` = usage<br>
`.toThrowError(error)` = To throw error<br>
`.not.toThrowError(error)` = To not throw error<br>
##
`.toHaveBeenCalled()` = function has been called<br>
`.not.toHaveBeenCalled()` = function has not been called<br>
##
`.toHaveBeenCalledWith(value)` = function has been called with value<br>
`.not.toHaveBeenCalledWith(value)` = function has not been called with value<br>
##

## Stubbing functions
```spyOn(function, "functionName").and.returnValue(value)```

```spyOn(function, 'functionName').and.callThrough()```

```spyOn(function, "functionName").and.callFake(function(arguments, can, be, received)```
