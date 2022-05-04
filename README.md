# README

## a) Niveau facile

###### Il y 347 albums
###### L'autheur de la chansson 'White Room' est Eric Clapton
###### La chansson qui dure 188133 ms est 'Perfect'
###### Le groupe qui à sortie l'album "Use Your Illusion II" est Guns N Roses


## b) Niveau moyen

###### Il y as 13 albums dont le titre contient "Great"
###### 4 albums ont été supprimés. Les id sont les suivants : 315, 319, 333, 346
###### Il y a un album "For Those About To Rock We Salute You" écrit par AC/DC dans Album. Mais dans tracks il y as deux albums.
###### Il y as 0 chanson qui durent exactement 158589 ms


## b) Niveau Difficile

###### Question 1
```Ruby
2.7.4 :030 > a = Track.where(artist: "AC/DC")
  Track Load (0.3ms)  SELECT  "tracks".* FROM "tracks" WHERE "tracks"."artist" = ? LIMIT ?  [["artist", "AC/DC"], ["LIMIT", 11]]
 => #<ActiveRecord::Relation [#<Track id: 1, title: "For Those About To Rock (We Salute You)", album: "For Those About To Rock We Salute You", artist: "AC/DC", duration: 343719, size... 
2.7.4 :031 > a.each{|r|puts r.title}
  Track Load (0.8ms)  SELECT "tracks".* FROM "tracks" WHERE "tracks"."artist" = ?  [["artist", "AC/DC"]]
  For Those About To Rock (We Salute You)
  Put The Finger On You
  Lets Get It Up
  Inject The Venom
  Snowballed
  Evil Walks
  C.O.D.
  Breaking The Rules
  Night Of The Long Knives
  Spellbound
  Go Down
  Dog Eat Dog
  Let There Be Rock
  Bad Boy Boogie
  Problem Child
  Overdose
  Hell Aint A Bad Place To Be
  Whole Lotta Rosie
```
###### Question 2
```ruby
2.7.4 :032 > b = Track.where(album: "Let There Be Rock")
  Track Load (0.4ms)  SELECT  "tracks".* FROM "tracks" WHERE "tracks"."album" = ? LIMIT ?  [["album", "Let There Be Rock"], ["LIMIT", 11]]
 => #<ActiveRecord::Relation [#<Track id: 15, title: "Go Down", album: "Let There Be Rock", artist: "AC/DC", duration: 331180, size: 10847611, price: 0.99, created_at: "2022-05-04 08... 
2.7.4 :034 > b.each{|t| puts t.title}
Go Down
Dog Eat Dog
Let There Be Rock
Bad Boy Boogie
Problem Child
Overdose
Hell Aint A Bad Place To Be
Whole Lotta Rosie
```
###### Question 3
Le prix total est de 7.92 $ et la durée total est de 2453259 ms

###### Question 4     
Le cout total de l'intégralité de la discographie de "Deep Purple" est de 90.0899999999999 $