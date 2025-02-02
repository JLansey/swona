# Swona

A Swift port of the lovely [Siilinkari](https://github.com/komu/siilinkari). Swona is a playground for exploring a teeny, Kotlin-ish language and compiler in pure Swift.

## Launch the REPL

`docker-compose run --rm repl`

### Example

```
var a = stringArrayOfSize(3, "")
var done = false
var i = 0

while (!done) { stringArraySet(a, i, "item" + i); i = i + 1; if (i==stringArrayLength(a)) done=true }

stringArrayGet(a, 2)

fun pow(a: Int, n: Int): Int = unless (n == 0 ) a * pow(a, n-1) else 1
pow(2, 8)
```

More in the [Prelude](Resources/prelude.sk).

## Run the tests

`docker-compose run --rm tests`

## Requirements for development
We use [Sourcery](https://github.com/krzysztofzablocki/Sourcery) to generate helpful `Equatables`. After installing Sourcery, from the root of this repo run:    
```cd Swona && sourcery && cd -```

They should then appear in `./Swona/Sources/Swona/Autogenerated/AutoEquatable.generated.swift`


# Acknowledgements

Juha Komulainen and others listed in [LICENSE-THIRD-PARTY](LICENSE-THIRD-PARTY).
