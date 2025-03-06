### 1. mergeStrings

Write `mergeStrings` function such that

- `mergeStrings("abc", "123")` ⇒ `"a1b2c3”`
- `mergeStrings("abcdef", "123")` ⇒ `"a1b2c3def”`
- `mergeStrings("abc", "123456")` ⇒ `"a1b2c3456”`
- `mergeStrings("abc", "123", "xyz")` ⇒ `"a1xb2yc3z”`

### 2. kebabCaseToCamelCase

Write function `kebabCaseToCamelCase` such that

- `kebabCaseToCamelCase(”da-nang”)` ⇒ `"daNang"`
- `kebabCaseToCamelCase(”ho-chi-minh-city”)` ⇒ `"hoChiMinhCity"`

### 3. camelCaseToKebabCase

Write function `camelCaseToKebabCase` such that

- `camelCaseToKebabCase(”daNang”)` ⇒ `"da-nang"`
- `camelCaseToKebabCase(”hoChiMinhCity”)` ⇒ `"ho-chi-minh-city"`

### 4. isUpperCase

Write function `isUpperCase` such that

- `isUpperCase("a")` ⇒ `false`
- `isUpperCase("A")` ⇒ `true`

### 5. upperLower

Write function `upperLower` such that

- `upperLower(" a NiCE  dAY ")` ⇒ `" A nIce  Day "`

### 6. capitalize

Write function `capitalize` such that

- `capitalize(" a NiCE  dAY ")` ⇒ `" A Nice  Day "`

### 7. trim

Write function `trim` such that

- `trim(" a nice  day ")` ⇒ `"a nice  day"`

### 8. trimAll

Write function `trimAll` such that

- `trimAll(" a nice  day ")` ⇒ `"a nice day"`

### 9. formatNumber

Write function `formatNumber` such that

- `formatNumber(1)` ⇒ `"1"`
- `formatNumber(100000)` ⇒ `"100,000"`
- `formatNumber(100000000)` ⇒ `"100,000,000"`

### 10. abba

Write function `abba` such that

- `abba("ab", "cde")` ⇒ `"abcdeba"`
- `abba("Hi", " John ")` ⇒ `"Hi John iH"`

### 11. table

Given this data

```js
const people = [
  { name: "Cuong" },
  { name: "Son Pham" },
  { name: "Son Vu" },
  { name: "Luan" },
  { name: "Anh" },
];
```

Write to screen

```
############
# Cuong    #
# Son Pham #
# ...      #
# Anh      #
############
```

Given this data

```js
const people = [
  { name: "Cuong", status: "Married" },
  { name: "Son Pham", status: "Married" },
  { name: "Son Vu", status: "Married" },
  { name: "Luan", status: "Unmarried" },
];
```

Write to screen

```
########################
# Name     | Status    #
#----------------------#
# Cuong    | Married   #
# Son Pham | Married   #
# ...      | ...       #
# Luan     | Unmarried #
########################
```
