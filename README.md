# rust

Site du tuto : https://blog.guillaume-gomez.fr/Rust/

Rust en ligne : https://play.rust-lang.org/

## Hello world

```rust
fn main() {
    println!("Hello, world!");
}
```

Pour compiler ce fichier : `rustc votre_fichier.rs`

## Variables

Toutes les variables sont des constantes par défaut.

```rust
let i = 0;

i = 2; // Erreur !
```

Pour déclarer une variable mutable, il faut utiliser le mot-clé mut :

```
let mut i = 0;

i = 2; // Ok !
```
### les types de variables

Par exemple, pour déclarer un entier de 32 bits, vous ferez :

```rust
let i: i32 = 0;
// ou :
let i = 0i32;
```

Sachez aussi que le compilateur de Rust utilise l'inférence de type. En gros, on n'est pas obligé de déclarer le type d'une variable, il peut généralement le déduire tout seul. Exemple :

```rust
let i = 0; // donc c'est un entier visiblement
let max = 10i32;

if i < max { // max est un i32, donc le compilateur en déduit que i en est un aussi
    println!("i est inférieur à max !");
}
```
voici une petite liste des différents types de base (aussi appelés "primitifs") disponibles :

    i8 : un entier signé de 8 bits
    i16
    i32
    i64
    i128
    u8 : un entier non-signé de 8 bits
    u16
    u32
    u64
    u128
    f32 : un nombre flottant de 32 bits
    f64 : un nombre flottant de 64 bits
    String
    slice (on va y revenir plus loin dans ce chapitre)

