# Group Theory Step-by-Step: 8–15 — Cleaned Transcript

*Video: "Group Theory Step-by-Step: 8 - 15" by TheGrayCuber (YouTube, Aug 2, 2025, ~21½ min). Second in the series: the groups of orders 8 through 15, plus group products, quaternions, Cayley diagrams, and the Sylow theorems. Two speakers: the **Host**, who explains, and his **Friend**, who asks questions and snarks. Speaker labels are inferred from context, as in Part 1. Section headings are content-based; YouTube's auto-chapters for this video are Intro (0:00), Groups of Order 8 (2:50), Groups of Order 9 (6:35), Smaller Examples (15:35).*

---

## Intro: Group products (0:00)

**Host:** Welcome back to Group Theory: Step-by-Step! In this episode, we'll look at the groups of order—

**Friend:** Uh… negative 7?

**Host:** That's just a hyphen. It's the groups of order 8 through 15. Then let's start with order 8. And to help us, let's recap the last video. Here are the groups of order 1 through 7 — what do you remember?

**Friend:** Hm. There's the cyclic groups — there was one for every number. So that means we have C8 in order 8, right?

**Host:** Yes. And there are multiple ways to represent the 8-cycle C8. We could use rotations in multiples of 45° — so 135° + 270° equals 45°. We could also use the integers mod 8 — so 3 + 6 = 1 mod 8. Or we could slightly vandalize a stop sign, turning it this much, then this much.

**Friend:** Can you stop and go back to the regular groups?

**Host:** Fine. So there's C8, but there's a bunch of other groups of order 8. What else did we learn last time?

**Friend:** Uh — there was the rectangle group. The one with the German name… grouper?

**Host:** Yeah — it's the symmetries of a rectangle: rotate, vertical flip, and horizontal flip. But this group is also C2 squared.

**Friend:** Wait, you can square a group?

**Host:** Yeah — it's the same as C2 times C2. Multiplying two groups is like putting them into an ordered pair. Each element has a coordinate from the first group and a coordinate from the second. To combine elements, we combine the first coordinates, and then the second ones — the operations work separately.

**Friend:** So — can we multiply any two groups?

**Host:** Hey, don't spoil it — we'll get to that in a minute. First, to tie this back to the rectangle: the horizontal flip is 180° in the first coordinate and neutral in the second. So the first coordinate tells us the rotation around the horizontal axis. And similarly, the second coordinate tells us the rotation around the up-axis.

**Friend:** Wait, what?

**Host:** And we write this as group multiplication, instead of something like group addition, because when groups multiply, their orders multiply too.

**Friend:** Ah — an order 2 group times an order 2 group equals an order 4 group: 2 × 2 is 4. If we wrote this as addition, we would get 2 + 2 = …

**Host:** Well, actually, this is a bad example.

**Friend:** How about 6 and 11?

**Host:** Yes, perfect. With C6 × C11, there are six options for the first coordinate and 11 options for the second — a total of 66 elements. So the product has order 66.

## Groups of order 8 (2:50)

**Friend:** And this idea of group products can help us find groups of order 8!

**Host:** Just like you guessed — we can multiply any two groups.

**Friend:** So if we take an order 4 × an order 2, we'd end up with an order 8?

**Host:** Exactly. To help us, let's pull up that recap.

**Friend:** Okay. So we can do C4 × C2, or V × C2?

**Host:** Yes — these are groups of order 8.

**Friend:** Although this name is weird.

**Host:** Like I said earlier, V is just C2 squared. So this is C2 cubed. And here are the tables for these groups. For easier notation, instead of writing (0, 0), (0, 1), we just write 00, 01. And at order 8, the tables are getting pretty big. Instead, we can visualize them using a Cayley diagram, which is named after Arthur—

**Friend:** Who's Arthur?

**Host:** Each element is a circle. The yellow arrows represent adding (1, 0), which takes us around a four-cycle.

**Friend:** Who is Arthur?

**Host:** And then green is adding (0, 1) — just a two-cycle back and forth. This is the diagram for C2 cubed.

**Friend:** It looks like a cube.

**Host:** Yeah — each C2 is another dimension. And then C8 is just a cycle, though we do get some cool patterns by coloring a second element. So now we've seen these groups of order 8, but there are still two more. And these two are not multiples of smaller groups. The first one is the quaternions.

**Friend:** Oh — is that the i-j-k thing you're always talking about?

**Host:** Yes, it is. We have the imaginary number i, and i² is −1. But j² and k² are also −1. And i, j, and k are all different: i × j = k. And that seems like a problem.

**Friend:** Why?

**Host:** Well, let's square both sides and rearrange the left. Then we get i², j², and k² — each of these is −1, so then the left side equals 1.

**Friend:** Wait, what? 1 is not −1! What did you do?

**Host:** I don't know. …You didn't do anything wrong. It was me, when I rearranged. We can't just swap i and j — ij = −ji. The same thing goes for swapping j with k, and k with i: they turn negative. The quaternions are non-commutative — or non-abelian.

**Host:** We saw another non-abelian group in the last video.

**Friend:** Oh yeah — it was the triangle group! Rotate then flip is not the same as flip then rotate.

**Host:** Yes, but you've got yourself flipped — in group theory, we read right to left.

**Friend:** Ugh, I forgot about that.

**Host:** Rotate then flip equals flip then inverse-rotate. The triangle group is called D6, the dihedral group of order 6. But this equation below is true for all the dihedral groups: D8, the symmetries of a square; D10, the symmetries of a regular pentagon; and so on.

**Friend:** So D8 is the last group of order 8.

**Host:** Yes. Here are the diagrams for D8 and the quaternions, or Q8. The diagrams look similar: D8 has rotation, which makes a four-cycle, and the flip inverts it when they swap. Q8 has i, which makes a four-cycle, and then j inverts it when they swap. The big difference is that flip squared is neutral, while j has to go to the fourth power to be neutral. So those are all the groups of order 8.

## Groups of order 9 (6:35)

**Host:** Now to the groups of order 9. They are all abelian, which makes things easy — we can just use the… fun-to-fin-a-g.

**Friend:** The what?

**Host:** The funto.

**Friend:** Can you just talk normal?

**Host:** Uh — we'll do normal subgroups later. This is the fundamental theorem of finite abelian groups.

**Friend:** Of course it is.

**Host:** It tells us that every finite abelian group is made of cycles. We saw this in order 8: they were all the product of cyclic groups, and the products were based on the factorizations of 8. So for order 9, we just need to find the factorizations of 9.

**Friend:** Okay — there's 3 × 3 and 1 × 9. I think that's it.

**Host:** Yes. So we have C3 × C3 and C1 × C9. Although multiplying by C1 doesn't do anything, so this is just the same as C9. So there we are — the groups of order 9. Here are their diagrams.

**Friend:** Woohoo.

**Host:** We see that C9 is just a loop, while C3 × C3 has separate loops that interact.

## Groups of order 10 (7:41)

**Host:** Next: the groups of order 10. Let's find the abelian ones using the funto-fac.

**Friend:** Okay — the factorizations of 10 are 2 × 5, and just 10. So that means we have C2 × C5 and C10. There are two abelian groups.

**Host:** Wrong. There is only one.

**Friend:** What do you mean?

**Host:** These are isomorphic: C10 is the same as C2 × C5.

**Friend:** How was I supposed to know that?

**Host:** Look at the orders of the elements. Let's start with C10: 3 has order 10 — following the three arrow takes us through all 10 elements. But 8 has order 5, since the eight arrow just makes a five-cycle. And 5 has order 2 — it just goes to 5 and then back to 0. Here are the orders for all the elements of C10, and then here for C2 × C5: both groups have one element with order 1, one with order 2, four with order 5, and four with order 10. The counts are the same, so the groups are the same.

**Friend:** What about the groups we saw earlier? Why didn't we check the counts then?

**Host:** They were all just different anyway. C9 has six elements of order 9, but C3 × C3 doesn't have any. And the groups of order 8 also have different counts. If we add in the non-abelian groups of order 8, we see that their counts are different, too. But we have to be careful with non-abelian: if groups have different counts, they must be different groups. But what if they have the same counts? If they're abelian, they will be the same. But if they're non-abelian, we can't be so sure — they might still be different. And speaking of non-abelian groups, there is one with order 10. It's part of a family we already saw.

**Friend:** Oh — it's the pentagon group!

**Host:** It's called D10. You're the one who started by calling them the triangle. And here are the diagrams for order 10: they both have the similar five-cycles in yellow, but they differ with the green two-cycles.

## Groups of order 11 and 12 (9:49)

**Host:** Next, order 11 — there's just C11. As we saw last time, if the order is prime, then the group is a cycle. So we'll move on to order 12. And we'll start with the abelian groups, using the fundamental theorem — it's the fto.

**Friend:** That's not a real word.

**Host:** Whatever. These are the factorizations of 12, so we have these groups. Then we count the orders of the elements: the two on the left are the same, and then also the two on the right. So there's just two abelian groups.

**Friend:** Very nice. How about the non-abelian groups? We'd have the hexagon group.

**Host:** It's called D12.

**Friend:** Yes, we know. Um — is that the only one?

**Host:** Nope. There are some more. Let's pull up the non-abelian groups we've seen so far. You knew about D12 because it's part of the dihedral family. But there's also a quaternion family — we have Q12. Instead of i squared being −1, we have zeta cubed as −1. And then, just like j turns i negative when they swap, j turns zeta into its inverse when they swap. This defines Q12. In general, Q4n has zeta to the n equals −1, along with the j-swap equation. The quaternion diagrams look similar to the dihedral, just with that j-loop being longer than the flip loop. Now, there is one more non-abelian group of order 12.

**Friend:** Ooh, I have an idea.

**Host:** Oh, okay — what is it?

**Friend:** So, you said we can multiply any two groups. So — what about D6 × C2?

**Host:** Huh! That's a really good point — but it's not the group I was thinking of.

**Friend:** This must be isomorphic to one of the groups we already saw. Which one?

**Host:** Um…

**Friend:** You don't know.

**Host:** No, I do know! I just think we should leave it as an exercise for the viewer.

**Friend:** Of course you do.

## The tetrahedron group (11:55)

**Host:** The final group of order 12 is the tetrahedron group — the symmetries of a tetrahedron. Let's label the faces 1, 2, 3, and 4. We'll say this is the default position: the neutral element, EINHEIT. To make any element: there are four options for where to put face 1, then there are three remaining options for face 2, and then the whole thing is fixed. So we have four options, then three options — a total of 12 symmetries. Here they are. (1 4 3) means that face 1 goes to face 4, which goes to face 3, which goes back to 1 — and this also means that face 2 just stays in the same spot.

**Friend:** So what does this element mean? …2 goes to 3, which goes to 4, which then goes back to 2?

**Host:** Yes. And then this element means that 1 swaps with 2, and 3 swaps with 4. Let's try doing an operation. What do we get by combining (2 4 3) with (1 4 3)? Hmm — maybe first let's ask: where does 1 end up? Remember, the elements apply right to left. So first, 1 goes to 4, then 4 goes to 3. So overall, we have 1 goes to 3. Now, where does 3 go?

**Friend:** So first it goes back around to 1… and then 1 isn't here, so it's fixed. So 3 goes to 1!

**Host:** 1 and 3 swap with each other. So it must be one of the swaps — this one.

**Friend:** Uh — yeah, it is! 2 and 4 also swap?

**Host:** First 2 is fixed, then it goes to 4; and 4 goes to 3, which then goes to 2. As you just demonstrated, this way of naming helps us: we can see that all of these elements have order 3 — each has three faces going in a cycle. And then these elements have order 2, since they're just swapping back and forth.

**Friend:** And this makes the group weird?

**Host:** All the other groups of order 12 have elements with at least order 6, but the tetrahedron maxes out at order 3. There aren't any big cycles. So the Cayley diagram doesn't look quite as nice.

**Friend:** Does the tetrahedron group have a letter nickname, like the other ones?

**Host:** Yeah — it's A4.

**Friend:** Four? But it has order 12!

**Host:** The naming doesn't always have to do with the order. It's A4 because the tetrahedron has four faces.

**Friend:** But where does the A come from?

**Host:** Uh… tetrahedron. No — we'll talk about the real reason in a future video.

## Interlude: The groups of order 13 (14:32)

**Host:** It's time that we move on to the groups of order 14.

**Friend:** Wait, what happened to 13?

**Host:** Uh… 7 ate 13.

**Friend:** Come on.

**Host:** They were a little peckish.

**Friend:** Seriously?

**Host:** Sorry — I thought I'd skip 13 since it's prime. So…

**Friend:** Oh, yeah. There's just C13.

## The Sylow theorems (14:53)

**Host:** Yeah. So we'll wrap up with orders 14 and 15. There aren't many groups — just the cyclic and dihedral. And we'll prove why this happens using the Sylow theorems. The Sylow theorems tell us that every group has Sylow p-subgroups — p stands for prime. These are subgroups of the highest prime power. For example, the group C540: the prime factorization is 2² × 3³ × 5, so these are the highest prime powers. The Sylow theorems tell us that there must be subgroups of orders 4, 27, and 5. For a smaller example, let's look at D12. What are the highest prime powers?

**Friend:** 12 is 2² × 3 — so 4 and 3.

**Host:** Yes. So the Sylow theorems tell us there must be subgroups of orders 4 and 3 — here they are. But actually, this one is not the only two-subgroup.

**Friend:** Two-subgroup? You mean four?

**Host:** Uh, it does have order 4, but it's called a two-subgroup since 4 is a power of the prime 2. We name using the primes. D12 has these three two-subgroups, and just a single three-subgroup. Here are the counts for all the groups of order 12. What do you notice about the counts of the two-subgroups?

**Friend:** They're either 1 or 3 — which are both odd.

**Host:** Yes — the count of two-subgroups is always odd: 1 mod 2.

**Friend:** And similarly, the number of three-subgroups is 1 mod 3?

**Host:** Yes. The Sylow theorems tell us that the number of Sylow p-subgroups is 1 mod p. This is very useful — why don't we apply it to the groups of order 14?

## Groups of order 14 (16:46)

**Friend:** Okay — so the highest prime powers are 2 and 7. So we have a subgroup of order 2 — neutral and some a — and then a subgroup of order 7 — neutral, some b, and powers of b.

**Host:** But now let's ask: how many seven-subgroups are there?

**Friend:** 1 mod 7.

**Host:** Yes, but what are some values that equal 1 mod 7?

**Friend:** 1… and then 8… and then we can just stop there.

**Host:** 8 won't work — and neither will any higher number. If there are 8, then we will have b and its powers, c and its powers, and so on — for 8 subgroups. They all share the neutral element, EINHEIT, but all the other elements must be unique.

**Friend:** Wait, why?

**Host:** Uh — let's say b³ = c⁴. We can find that c is a power of b, so every power of c is also a power of b — meaning that these subgroups are the same. Because 7 is prime, the different subgroups must have different elements.

**Friend:** So 8 different subgroups, each with 6 unique elements, totals 48 elements — which is a problem, because there are only 14 elements.

**Host:** Exactly. So there must be only one 7-subgroup. We have b with order 7. And remember, we also have a from the two-subgroup — it has order 2. What if they combine? What's the order of ab?

**Friend:** The order must divide 14 — so it can be 1, 2, 7, or 14.

**Host:** But 7 won't work, because that would put ab in the 7-subgroup — meaning that it's a power of b. But that would mean that a is a power of b, which it's not. The order also can't be 1, for the same reason. So it's either 2 or 14. If it's 14, then the powers of ab form a 14-cycle — it's C14.

**Friend:** Yep.

**Host:** And if the order is 2, then ab squared is neutral. Multiply by a and cancel out a², then by b inverse, and we get ba = a b⁻¹. If we rename to flip and rotate, we get the equations of a dihedral group — it's D14.

**Friend:** So a group of order 14 is either dihedral or cyclic. And the same thing happened with order 10 and order 6.

**Host:** These are 2 × a prime. That proof applies to any order that's 2 × a prime — but not to order 15. We need a different proof.

## Groups of order 15 (19:27)

**Host:** 5 is a highest prime power, so there is a 5-subgroup — and there's only one. 6 is 1 mod 5, but there can't be 6 subgroups.

**Friend:** Why not? That would be too many elements.

**Host:** Yes — 6 subgroups, each with 4 unique elements, is 24 elements, but there are only 15. So we have this one subgroup of 5 elements, and that means that there must be 10 other elements. They can't have order 5, since that would put them in the 5-subgroup. And they can't have order 1, since that would mean they are neutral. So they must have orders 3 or 15 — and at least one of them has order 15. Otherwise, if they were all order 3, they would split into 5 different 3-subgroups — but 5 is not 1 mod 3, so that breaks the Sylow theorems. So there's at least one element of order 15, meaning that we get a 15-cycle. C15 is the only possible group of order 15. Its diagram just makes a cycle. But we can get some other cool shapes by switching the arrows to different elements. And you can try this out yourself.

**Friend:** Okay.

**Host:** No, I meant the viewer.

**Friend:** Oh — but yeah, go ahead.

**Host:** I made this group explorer website where you can view tables and diagrams for all these groups. I'll make a full video to show how it works soon, but for now, play around and leave a comment if there's a feature you'd like me to add. If you enjoy the channel, check out my page on Ko-fi, where I post more casual behind-the-scenes videos about other projects I'm working on. And join us next time for the groups of order 16 — and then the groups of order 17, and then… no, it's just going to be order 16 in the next video. There are a lot of them.

**Friend:** I was just trying to join in on the bit you did last time.

**Host:** Oh, okay.

---

## Cleanup notes

1. **Source:** Auto-generated captions, pulled from the video's transcript panel (184 caption segments). The duplicated timestamp markers ("0:05 | 5 seconds") were stripped; section start times are kept in the headings.
2. **Speakers:** Split into **Host** (teaching) and **Friend** (questioning/snarking), as in Part 1. Attribution of the shortest interjections is inferred from context.
3. **Garbled names fixed:** "quatronians" → quaternions; "kay diagram" / "kali diagram" → Cayley diagram (named after Arthur Cayley); "CEO theorems" / "clo theorems" → Sylow theorems; "tetrahedrin" → tetrahedron; "isomeorphic" → isomorphic; "coffee" → Ko-fi; "uptaxis" → up-axis; "height" and "finite" → EINHEIT (the recurring German joke for the neutral element).
4. **Dropped negatives restored (the math requires them):** j² and k² are also −1; "1 is not −1"; swapping i and j turns them negative (ij = −ji); for Q4n, zeta-to-the-n equals −1 (not 1); "(ab)² is neutral" when ab has order 2; "the powers of ab" (not of a) form the 14-cycle; "instead of i squared being −1."
5. **Running gag:** The Host's made-up abbreviation for the fundamental theorem of finite abelian groups is rendered as heard: "fun-to-fin-a-g," "the funto," "the funto-fac," and "the fto." The Friend's "grouper" mangling of "Vierergruppe" is kept (it's the joke).
6. **Jokes decoded:** "7 81 13" is the classic "7 ate 13" pun; "8 - 15" read as "negative 7" mirrors Part 1's "negative six" bit.
7. **Notation:** "C6 * C1" corrected to C6 × C11; "C2 cub" → C2 cubed; cycle notation formatted as (1 4 3) and (2 4 3); the element-pair shorthand "(0, 0) → 00" reconstructed from garbled captions.
