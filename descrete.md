# Discrete Mathematics: Set Theory for Computer Scientists

## Table of Contents
- [Core Set Operations](#core-set-operations)
- [Power Sets & Cardinality](#power-sets--cardinality)
- [Infinite Sets & Computability](#infinite-sets--computability)
- [Multisets & Applications](#multisets--applications)
- [Sets in Cryptography](#sets-in-cryptography)
- [Algorithmic Complexity](#algorithmic-complexity)
- [Advanced Proofs](#advanced-proofs)
- [Real-World CS Problems](#real-world-cs-problems)
- [Bonus Challenges](#bonus-challenges)

---

## Core Set Operations

### Q1: Basic Union
**Q**: Given \( A = \{1, 2, 3\} \) and \( B = \{3, 4, 5\} \), what is \( A \cup B \)?  
**A**: 
$$ \{1, 2, 3, 4, 5\} $$

*Key Concept*: Union combines all unique elements from both sets.

---

### Q2: Intersection
**Q**: For \( A = \{1, 2, 3\} \) and \( B = \{x \mid x \text{ is prime}\} \), find \( A \cap B \).  
**A**: 
$$ \{2, 3\} $$

*CS Application*: Used in database `INNER JOIN` operations.

---

### Q3: Set Difference
**Q**: Compute \( A \setminus B \) where \( A = \{1, 2, 3\} \) and \( B = \{2, 3, 4\} \).  
**A**: 
$$ \{1\} $$

*Algorithm Use*: Finding elements in one dataset but not another.

---

## Power Sets & Cardinality

### Q4: Power Set Size
**Q**: If \( |A| = 4 \), what is \( |\mathcal{P}(A)| \)?  
**A**: 
$$ 2^4 = 16 $$

*Relevance*: Determines state space in finite automata.

---

### Q5: Subset Counting
**Q**: How many 3-element subsets exist in \( \{1, 2, \dots, 10\} \)?  
**A**: 
$$ \binom{10}{3} = 120 $$

*Optimization*: Critical in combinatorial algorithms.

---

## Infinite Sets & Computability

### Q6: Countability
**Q**: Is the set of rational numbers \( \mathbb{Q} \) countably infinite?  
**A**: Yes – can be enumerated via diagonalization.

---

### Q7: Uncountability Proof
**Q**: Sketch why \( (0,1) \subseteq \mathbb{R} \) is uncountable.  
**A**:  
1. Assume a complete list \( \{x_1, x_2, \dots\} \) exists.  
2. Construct \( y \) where \( n \)-th digit differs from \( x_n \).  
3. \( y \) is not in the list → contradiction.

*CS Connection*: Halting problem reducibility.

---

## Multisets & Applications

### Q8: Multiset Union
**Q**: For multisets \( M = \langle a, a, b \rangle \) and \( N = \langle a, b, b \rangle \), find \( M \cup N \).  
**A**: 
$$ \langle a, a, b, b \rangle $$

*Use Case*: Bag-of-words models in NLP.

---

## Sets in Cryptography

### Q9: Group Theory
**Q**: Why must the keyspace in AES form a group under XOR?  
**A**: Ensures invertibility (decryption) and closure.

---

## Algorithmic Complexity

### Q10: Bloom Filters
**Q**: What set operation does a Bloom filter approximate?  
**A**: Membership testing with false positives.

*Complexity*: \( O(k) \) for \( k \) hash functions.

---

## Advanced Proofs

### Q11: De Morgan's Law
**Q**: Prove \( \overline{A \cap B} = \overline{A} \cup \overline{B} \).  
**Proof**:  
1. Let \( x \in \overline{A \cap B} \).  
2. Then \( x \notin A \) **or** \( x \notin B \).  
3. Thus \( x \in \overline{A} \cup \overline{B} \).

---

## Real-World CS Problems

### Q12: Graph Representation
**Q**: Express an undirected graph as sets.  
**A**: 
$$ G = (V, E) \text{ where } E \subseteq \{\{u,v\} \mid u,v \in V\} $$

---

## Bonus Challenges

### Q13: Cartesian Product
**Q**: What is \( \{1, 2\} \times \{a, b\} \)?  
**A**: 
$$ \{(1,a), (1,b), (2,a), (2,b)\} $$

*Database Link*: Foundation for relational joins.

---

### Q14: Infinite Intersection
**Q**: Compute \( \bigcap_{n=1}^\infty \left(0, \frac{1}{n}\right) \).  
**A**: 
$$ \emptyset $$

*Topology Connection*: Shows limits of open sets.
