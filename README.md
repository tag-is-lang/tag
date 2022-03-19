# tag
the abstraction game

## boolean logic module
(xor is all you need, right?)

### bool-textual
![bool.t](/src/txt/bool.t.txt)
```
[bool]: < [0] || [1] > :: |>
[xor]: |> |> ( [0][0]:[0] [1][1]:[0] [1] ) :: ( [bool] |> [bool] |> [bool] )
```

### bool-graphical


![bool.g.png](/src/png/bool.g.png)

## some other syntax concepts that do not have a place yet

### type classes
very ugly but may work graphically... i hope

![numeric.t](/src/txt/numeric.t.tag)
```
[numeric]: |(t)> 
  [ [|(a)> +|(b)>]: [+] [(a)] [(b)]
    [+]: |> |> () :: ( [(t)] |> [(t)] |> [(t)] )
  ]
```
### is that a main?
maybe 

![test.t](/src/txt/test.t.txt)
```
[answer]: [a+b] :: [bool] ::: [bool is numeric]
[a]: [0]
[b]: [1]
[bool.+]: [xor]
[main]: [print answer] :: [io] []
```
