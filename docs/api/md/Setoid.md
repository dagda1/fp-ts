MODULE [Setoid](https://github.com/gcanti/fp-ts/blob/master/src/Setoid.ts)

# Setoid

_type class_

```ts
interface Setoid<A> {
  equals: (x: A, y: A) => boolean
}
```

The `Setoid` type class represents types which support decidable equality.

Instances must satisfy the following laws:

1. Reflexivity: `S.equals(a, a) === true`
2. Symmetry: `S.equals(a, b) === S.equals(b, a)`
3. Transitivity: if `S.equals(a, b) === true` and `S.equals(b, c) === true`, then `S.equals(a, c) === true`
   # setoidBoolean
   _instance_

```ts
setoidBoolean:
```

# setoidNumber

_instance_

```ts
setoidNumber:
```

# setoidString

_instance_

```ts
setoidString:
```

# getArraySetoid

_function_

```ts
<A>(S: Setoid<A>): Setoid<Array<A>>
```

# getProductSetoid

_function_

```ts
<A, B>(SA: Setoid<A>, SB: Setoid<B>): Setoid<[A, B]>
```

# getRecordSetoid

_function_

```ts
<O extends { [key: string]: any }>(
  setoids: { [K in keyof O]: Setoid<O[K]> }
): Setoid<O>
```

# strictEqual

_function_

```ts
<A>(a: A, b: A): boolean
```
