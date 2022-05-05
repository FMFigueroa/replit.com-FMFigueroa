## Simple test with Replit

<h3>🚀 Demo: <a style={{color:"#3385ff"}} href="https://replit.com/@FMFigueroa/juego-de-adivinanzas">Guessing Game</a></h3>

<hr/>

### ![Typing Animation Displays My Roles](https://readme-typing-svg.herokuapp.com?color=%503385ff&lines=🦀+Rust+Language;🦀+source+Code;)

    use rand::Rng;
    use std::cmp::Ordering;
    use std::io;

    fn main() {
    println!("Guess the number!");

    let secret_number = rand::thread_rng().gen_range(1..101);
    println!("The secret number is: {}", secret_number);

    println!("Please input your guess.");
    let mut guess = String::new();

    io::stdin()
        .read_line(&mut guess)
        .expect("Failed to read line");
    let guess: u32 = guess.trim().parse().expect("Please type a number!");

    println!("You guessed: {}", guess);
    match guess.cmp(&secret_number) {
        Ordering::Less => println!("Too small!"),
        Ordering::Greater => println!("Too big!"),
        Ordering::Equal => println!("You win!"),
       }
    }
