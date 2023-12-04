
# Single Types
---

## Basic Types
---

String, Number, Boolean

## Complicated Types
---

* Arrays E.g. `number[] -> [1, 2]`
* Objects E.g. `{a: number, b: number} -> {a: 1, b: 2}`
* Tuples E.g. `[number, string] -> [2, 'abc']`
* Enums E.g. `Role -> Enum Role { YES, NO, NEUTRAL }`
* Functions E.g. `() => void -> () => console.log('abc')`
	* Usually Used for `callback` function

## Other Types
---

* any
* void
* Unknown -> `Only can be converted to any & use type check for next step`
* never -> `Use for the case that never come back with value E.g. throw error`

# Combined Types
---

* Union Types -> E.g. `string | number`
* Literal Types -> E.g. `'as-text' | 'as-number'`