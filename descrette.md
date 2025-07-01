# Discrete Mathematics: Set Theory Questions for Computer Scientists

## Core Set Operations

### Question 1  
**Q**: Let \( A = \{1, 2, 3\} \) and \( B = \{x \mid x \text{ is prime}\} \). Find \( A \cap B \).  
**A**: \( \{2, 3\} \) *(Primes in A)*.

### Question 2  
**Q**: Compute \( A \Delta B \) (symmetric difference) for \( A = \{1, 2\} \) and \( B = \{2, 3\} \).  
**A**: \( \{1, 3\} \) *(Elements in exactly one set)*.

### Question 3  
**Q**: Simplify \( (A \cup B) \cap (A \cup \overline{B}) \).  
**A**: \( A \) *(Absorption law)*.

---

## Power Sets & Cardinality

### Question 4  
**Q**: If \( |A| = 4 \), what is \( |\mathcal{P}(\mathcal{P}(A))| \)?  
**A**: \( 2^{2^4} = 65,\!536 \) *(Power set of a power set)*.

### Question 5  
**Q**: How many subsets of \( \{1, 2, \dots, n\} \) contain exactly 2 elements?  
**A**: \( \binom{n}{2} \) *(Combinations)*.

### Question 6  
**Q**: What is \( \mathcal{P}(\emptyset) \)?  
**A**: \( \{\emptyset\} \) *(The only subset of the empty set is itself)*.

---

## Infinite Sets & Computability

### Question 7  
**Q**: Is \( \mathbb{N} \) (natural numbers) countably infinite?  
**A**: Yes—it can be put into a bijection with \( \mathbb{Z} \) or \( \mathbb{Q} \).

### Question 8  
**Q**: Prove \( |\mathbb{R}| > |\mathbb{N}| \) (Cantor’s diagonal argument).  
**A**:  
1. Assume a bijection \( f: \mathbb{N} \to \mathbb{R} \).  
2. Construct a real number not in \( f \)’s image by flipping the \( i \)-th digit of \( f(i) \).  
3. Contradiction shows no such bijection exists.

### Question 9  
**Q**: What is the cardinality of the set of all functions \( f: \mathbb{N} \to \{0, 1\} \)?  
**A**: \( 2^{\aleph_0} = \mathfrak{c} \) *(Same as \( \mathbb{R} \))*.

---

## Multisets & Applications

### Question 10  
**Q**: Let \( M = \langle a, a, b \rangle \) and \( N = \langle a, b, b \rangle \). Compute \( M \cup N \).  
**A**: \( \langle a, a, b, b \rangle \) *(Union takes max counts per element)*.

### Question 11  
**Q**: How are multisets used in database systems?  
**A**: For duplicate-tolerant operations (e.g., SQL `UNION ALL`).

### Question 12  
**Q**: What is the multiplicity of \( a \) in \( M \cap N \) for the above multisets?  
**A**: \( 1 \) *(Intersection takes min counts)*.

---

## Sets in Cryptography

### Question 13  
**Q**: How are sets used in Diffie-Hellman key exchange?  
**A**: The protocol operates over a multiplicative group (a set with closure, associativity, etc.).

### Question 14  
**Q**: What set property ensures a hash function is collision-resistant?  
**A**: Large codomain (output space) relative to the domain (input space).

### Question 15  
**Q**: In zero-knowledge proofs, what set operation verifies \( x \in A \) without revealing \( A \)?  
**A**: Set membership proofs (e.g., using Merkle trees).

---

## Algorithmic Complexity

### Question 16  
**Q**: What is the time complexity of computing \( A \times B \) for finite sets?  
**A**: \( O(|A| \cdot |B|) \) *(All possible pairs)*.

### Question 17  
**Q**: How can Bloom filters represent set membership with false positives?  
**A**: Using bit arrays and hash functions (space-efficient but probabilistic).

### Question 18  
**Q**: Why is \( A \Delta B \) useful in version control systems (e.g., Git)?  
**A**: It identifies changes between two states (added/removed elements).

---

## Advanced Proofs

### Question 19  
**Q**: Prove \( A \subseteq B \) iff \( A \cup B = B \).  
**A**:  
- (→) If \( A \subseteq B \), then \( A \cup B = B \).  
- (←) If \( A \cup B = B \), then \( A \subseteq B \).

### Question 20  
**Q**: Show that \( \mathcal{P}(A \cap B) = \mathcal{P}(A) \cap \mathcal{P}(B) \).  
**A**:  
- \( X \in \mathcal{P}(A \cap B) \iff X \subseteq A \cap B \iff X \subseteq A \) and \( X \subseteq B \).

---

## Real-World CS Problems

### Question 21  
**Q**: How would you represent a graph as a set?  
**A**: \( G = (V, E) \), where \( V \) is a set of vertices and \( E \subseteq V \times V \).

### Question 22  
**Q**: In regex, how does character class `[a-z]` relate to set theory?  
**A**: It defines a set of allowed characters (e.g., \( \{a, b, \dots, z\} \)).

### Question 23  
**Q**: What set operation corresponds to SQL’s `JOIN`?  
**A**: Cartesian product followed by selection (a filtered \( \times \)).

---

## Bonus Challenges

### Question 24  
**Q**: Let \( A = \{1, 2, 3\} \). What is \( \bigcup \mathcal{P}(A) \)?  
**A**: \( A \) *(Union of all subsets returns the original set)*.

### Question 25  
**Q**: Compute \( \bigcap_{n=1}^\infty \left(0, \frac{1}{n}\right) \).  
**A**: \( \emptyset \) *(Nested open intervals shrink to nothing)*.

### Question 26  
**Q**: What is the set \( \{f \mid f: \emptyset \to \emptyset\} \)?  
**A**: \( \{ \emptyset \} \) *(The empty function is the only possible function)*.