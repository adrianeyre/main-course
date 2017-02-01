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
`.toBe(true)` = To be true/false
`.not.toBe(true)` = To not be true/false

`.toEqual("result")` = To equal result
`.not.toEqual("result")` = To not equal result

`.toContain(item)` = To contain item
`.not.toContain(item)` To not contain item

`.toMatch(/item/)` = To match item
`.not.toMatch(/bar/)` = To not match item

`.toBeDefined()` = To be defined
`.not.toBeDefined()` = To not be defined

`.toBeUndefined()` = To be undifined
`.not.toBeUndefined()` = To not be undifined

`.toBeNull()` = To be Null
`.not.toBeNull()` = to Not be Null

`.toBeTruthy()` = Result to be a boolean
`.not.toBeTruthy()` = Result not to be a boolean

`.toBeFalsy()` = Result to be a boolean
`.not.toBeFalsy()` = Result not to be a boolean

`.toBeLessThan(value)` = To be less than the value
 `.not.toBeLessThan(value)` = To not be less than the value

`.toBeGreaterThan(value)` = To be greater than the value
`.not.toBeGreaterThan(value)` = To not be greater than the value

`.toBeCloseTo(v1, v2)` = To be close to v1 and v2
`.not.toBeCloseTo(v1, v2)` = To not be close to v1 and v2

 `throw 'error'` = usage
`.toThrow(error)` = To throw error
`.not.toThrow(error)` = To not throw error

`throw new TypeError("error")` = usage
`.toThrowError(error)` = To throw error
`.not.toThrowError(error)` = To not throw error

