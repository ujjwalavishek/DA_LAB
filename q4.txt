collatz.chain <- function(n) {
    chain <- vector()
    i <- 1
    while (n != 1) {
        if (n%%2 == 0)
            n <- n / 2
        else
        n <- 3 * n + 1
        chain[i] <- n
        i <- i + 1
    }
    return(chain)
}
answer <- 0
collatz.max <- 0
for (n in 1:1E6) {
    collatz.length <- length(collatz.chain(n))
    if (collatz.length > collatz.max) {
        answer <- n
        collatz.max <- collatz.length
    }
}
print(answer)