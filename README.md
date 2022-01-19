# tag-lang
the abstraction game language
```

|> -- outside of the system

[ |> ] -- input

[] -- data

() -- function

(()) = () -- function composition

([]) = [] -- function application

(([])) = ([]) = [] -- the two above

[] = [] -- type conversion

########### tag0 ############

bool: [<0|1>]

0 =0?: [1]
1 =0?: [0]
0 =1?: [0]
1 =1?: [1]

list a: [< a . list a | empty >]

apply0 f: (f 0)
apply1 f: (f 1)

########### tag1 #############

-- curry?

curry 

```

-------

attempt2: tags can only use [] from the same level

```

##### tag0 #####

-- leaves? (base cases)
[] -- nothing
[0] -- false
[1] -- true

-- maybe 
maybe: ( ([00000]) => < [] || just ([00000]) > )   < []| | >

-- isNothing
[=[]?]: ([] -> [1])
[=[]?]: ((just _) -> [0])

-- consToMaybe
[consToMaybe]: (((cons head) _) -> just head)
[consToMaybe]: ([] -> [])

-- in haskell: data forall a. Maybe a = Nothing | Just a
-- forall a. = ([00000]) =>
-- < | > = |
-- just ([00000]) = Just a

-- maybe a = forall b. (a -> b) -> b -> b
-- Just = \x j n -> j x
-- Nothing = \j n -> n
-- isJust = \m -> m (const True) False

-- list
[000]: (([00000]) => < pure  | ([001]  [00000]) > )

-- first/head
[100]: ([] -> [])
[100]: (([00000]) -> )

-- second/tail
[101]: ([] -> [])
[101]: ()

-- id
[111]: (([00000]) -> [00000])

-- bool
[01]: <[0] | [1]>

-- =0?
[10]: ([0] -> [1])
[10]: ([1] -> [0])

-- =1?
[11]: ([0] -> [0])
[11]: ([1] -> [1])


```