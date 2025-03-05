---
title: How to Use Blockchain to Generate Fair Random Numbers
---

The fairness of a lottery is always the most questioned aspect of such activities. Since it involves the selection of random numbers, online lotteries can hardly ensure fairness, as it is difficult to guarantee that the winning numbers are generated randomly rather than being manually selected.

To address the issue of lottery fairness and eliminate the possibility of manipulation, we have specifically designed the following process for generating random numbers.

# What Makes a Random Number Fair?

The random numbers (which are actually pseudo-random numbers) used in a fair lottery process should have the following characteristics:

- 1. The generation of random numbers does not rely on trust in the lottery organizer or any third party.
- 2. Unpredictable in advance.
- 3. Verifiable and publicly accessible afterward.
- 4. Statistically satisfies a uniform distribution.

To ensure properties 1 to 3, we choose to use Bitcoin block hashes as our random number seed; property 4 can be guaranteed by selecting a commonly used hash function.

# The Algorithm

- 1. Select the hash value of the first Bitcoin block mined after a specified time (the lottery time), denoted as S.
- 2. Calculate the hash value H of S using the SHA-256 algorithm, then convert H into a long integer L as a hexadecimal number.
- 3. Use L as the random number seed to generate N unique random numbers, where N is the required number of random numbers.

The generated random numbers will have the following characteristics:

- 1. No Reliance on Trust: The process does not depend on trusting the lottery organizer or any third party. By using the hash of a Bitcoin block, which is uncontrollable data source, the process ensures that no one can influence the outcome.
- 2. Unpredictability: The hash of the Bitcoin block at a specific time is inherently unpredictable before the block is mined. This ensures that the random number cannot be anticipated or manipulated in advance.
- 3. Transparency and Verifiability: The hash values used are publicly accessible. After the lottery, anyone can verify the block hash and the resulting random number, ensuring the process is transparent and accountable.
- 4. Uniform Distribution: The use of a standard hash function like SHA-256, which is designed to produce uniformly distributed outputs, ensures that the random numbers generated have a uniform distribution, satisfying the requirement for fairness.

# Summary

In this blog, we explore how to generate fair random numbers using blockchain technology. Traditional lottery systems often face skepticism regarding their fairness due to the unpredictability and potential for manipulation. To overcome these challenges, we propose a method that leverages Bitcoin block hashes as seeds for generating pseudo-random numbers. This approach ensures that the random numbers are unbiased, verifiable, and statistically uniform. By using a widely accepted hash function and a transparent process, we address concerns about trust and predictability, providing a robust solution for fair lottery systems.