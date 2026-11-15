# Group Theory Step-by-Step: 17–23 — Cleaned Transcript

*Video: "Group Theory Step-by-Step: 17 - 23" by TheGrayCuber (YouTube). Two speakers: the **Host**, who explains, and his **Friend**, who asks questions, snarks, and in this episode does a lot of the math himself. There is also a third voice, the **Computer** — the group-explorer website (introduced at the end of Part 2) speaking in robot voice. Speaker labels are inferred from context; a few very short interjections could belong to the other voice.*

---

## Chapter 1: Introduction (0:01)

**Host:** Welcome back to Group Theory: Step-by-Step! Today we'll be looking at the groups of order 18 through 21.

**Friend:** What? That says 17 through 23.

**Host:** Well, yeah — but we don't have to look at every order. We can skip 17, 19, and 23 since they're prime.

**Friend:** Right — so there's only the cyclic group.

**Host:** Yeah. And then 22 is two times a prime. We showed in a previous episode that any double of a prime will just have the cyclic and the dihedral group. So there's only a few interesting cases.

## Chapter 2: The abelian groups (0:36)

**Friend:** Okay. So let's start with order 18 and look at the abelian groups—

**Host:** —using the funag.

**Friend:** That's the fundamental theorem of finite abelian groups.

**Host:** Yeah. Every finite abelian group is the product of cycles.

**Friend:** So we just need to figure out the factorizations of 18. There's an abelian group for each one, but they might not be unique. So we should count the orders of the elements.

**Host:** Hold on, hold on.

**Friend:** What?

**Host:** We don't actually have to check the orders.

**Friend:** Wait, what?

**Host:** It's time that I taught you the true funag.

**Friend:** Why didn't you just do that in the first place?

**Host:** Every finite abelian group is the unique product of p p cycles—

**Friend:** —which means prime power.

**Host:** Yeah, if you want to be boring. Every cycle can be made of p p cycles. Last time we saw that two cycles can multiply into a larger cycle if their orders have no common factor. So the 2 and 9 can combine to make the 18-cycle. What about this case?

**Friend:** The 2 and 3 can combine to make the 6-cycle, and we just carry over the 3.

**Host:** Exactly. We only need the p p groups to create everything else, and they will be unique.

**Friend:** Right. We can't combine the 3s to make 9, since they share a common factor.

**Host:** Yep. So now let's use the true funag for orders 20 and 21. What are their p p factorizations?

**Friend:** 20 has 4 × 5 and 2 × 2 × 5 — so that's two abelian groups. And 21 is just 3 × 7. There's only one.

**Host:** Nice. We now have a straightforward method for finding the abelian groups. Although writing out p p groups takes up a lot of space, so we usually just write the combined version.

**Friend:** Makes sense.

**Host:** All right. Now we never have to find the abelian groups again.

**Friend:** Goodbye, abelian groups.

## Chapter 3: The first nonabelian groups of order 18 (2:31)

**Host:** Now, let's find the nonabelian. We'll start with order 18.

**Friend:** Okay — there's D18, of course, but there's no quaternions since it's not divisible by 4. I'm not sure if there's anything else.

**Host:** I agree.

**Friend:** Wait — you don't know?

**Host:** No, I agree that you're not sure.

**Friend:** Why would you even say that?

**Host:** What if we multiply smaller groups?

**Friend:** Oh, yeah. We could multiply an order 9 × 2, or a 6 × 3.

**Host:** The groups of order 9 and 2 won't work, though — they're all abelian, so any product would also be abelian.

**Friend:** But with 6 × 3, we could do D6 × C3.

**Host:** Yes, that is a new group. Although we should check to see if it's actually different from D18.

**Friend:** Let's count the orders of the elements.

**Host:** Sure, but we'll make the computer do it.

**Computer:** Please input generators.

**Friend:** What — generators?

**Host:** Remember, like from last time: computers use equations, such as R9 = EINHEIT—

**Friend:** —right? And then F2 is EINHEIT, and then FR is R inverse F.

**Computer:** Affirmative. However, we require letter format, such as: R9 = blank, F2 = blank, and FR = R8F.

**Friend:** Okay, I get it. So for the other group, D6 is the symmetries of a triangle. So R3 is blank, and then F2 is blank, and then FR is R inverse F — FR equals R2F, right? And then for C3, we have A3 is blank, and then A commutes with R and F.

**Computer:** Thank you for the equations. Preparing bar charts… Bar chart prepared.

**Host:** So they are different groups. D18 has no elements of order 6 — it's mostly order 2, because of the flips. And then the product has no order 9 — it's mostly order 3.

**Computer:** Please input generators for the following group.

**Friend:** The following group?

**Host:** Yeah, we're not done with order 18. These aren't the only nonabelian groups.

## Chapter 4: The semidirect product (4:39)

**Friend:** But D6 × C3 is the only nonabelian way to multiply. So it must be something else.

**Host:** It's the only way with the direct product. Last time we learned about the semidirect product.

**Friend:** Yeah. And we already saw an example in this video: D18 is C9 semidirect-times C2.

**Host:** But what does that mean?

**Friend:** Um — it means that C2 messes with C9, right?

**Host:** Yeah. C9 is the rotations. C2 is the flips. And the flips mess with the rotations — when rotation passes flip, it gets inverted.

**Friend:** Which means we can make nonabelian groups out of abelian groups.

**Host:** Exactly. And it also means that we have to be careful about the direction. C9 messed up by C2 could be different from C2 messed up by C9. We need to check both cases. So then we should also check C3² semidirect-times C2 and C2 semidirect-times C3², and then C6 semidirect-times C3, C3 semidirect-times C6, D6 semidirect-times C3, and C3 semidirect-times D6.

**Friend:** Wow, that's a lot.

**Host:** But wait — there's more. In this case, C2 messes with C9 by inverting: r goes to r inverse. Then with this product, C3 messes with D6: f could go to r f, or it could go to r² f. There are multiple options. For each semidirect product, we have to check all possible mess-aroundings — messing around… mess-aroundings.

**Friend:** Can you just say the real math term?

**Host:** Fine. Automorphisms.

**Friend:** Hm. That sounds like the term from last time — isomorphism.

**Host:** That's because they're closely related. To recap: what does it mean if two groups have an isomorphism?

**Friend:** It means they act the same.

**Host:** Yes. And we have some map that can move back and forth between them. An automorphism is an isomorphism from a group to itself — auto means self. So C9 has an automorphism by inverting the rotation. Both sides act the same.

**Friend:** Right — we're basically just switching from clockwise to counterclockwise.

**Host:** Exactly. And this automorphism can be used to make a semidirect product. It's okay if C2 messes with C9, because it will still act as C9. And that brings us to our first real-world application of the semidirect product.

**Friend:** Oh, cool.

**Host:** If you mess with someone, you must still let them act as themselves.

**Friend:** Sure, I guess. But that really has nothing to do with math.

**Host:** I know. That's why I said real world. Getting back to the abstract world: a semidirect product requires an automorphism. But not all of them work. C9 also has an automorphism that sends r to r², but it can't make an SDP.

**Friend:** Why not?

**Host:** Let's try. We'll say that f applies this automorphism. So when r passes f, it gets squared. Now, what happens when r passes ff?

**Friend:** After the first f it gets squared, and then the second f squares again. So we get r to the 4th.

**Host:** Yes, but now we have a problem. What does ff equal?

**Friend:** Oh — it's EINHEIT. The two sides are different.

**Host:** Yeah: f squares to EINHEIT. So then the f automorphism must square to the EINHEIT-omorphism, which doesn't do anything — it just maps r to itself. This fails with the square automorphism, since r ends up at r⁴. But what about the inverse automorphism?

**Friend:** r goes to r inverse, and that goes back to r. It's the EINHEIT-omorphism.

**Host:** Yes — that's why it works as an SDP.

## Chapter 5: Automorphisms form a group (8:37)

**Host:** So to find all the SDPs, we need to find all the automorphisms that square to the EINHEIT-omorphism. And that might sound like a difficult task, but we can use the magic of group theory: automorphisms form a group.

**Friend:** Wait, really?

**Host:** Yeah. Let's check the terms and conditions for being a group. First, we need an operation — a way to combine elements. And we can combine any two automorphisms: they go from a group to itself, so we can just fuse the middle g's. Like with C9 — what happens when we combine the square and inverse maps?

**Friend:** r goes to r², and then that goes to r to the −2.

**Host:** It's the squ-inverse map. Any two automorphisms combine in a similar way, so we do have an operation. The next condition is that we need a neutral element.

**Friend:** That's the EINHEIT-omorphism.

**Host:** Exactly. Easy peasy — nauseous beetle.

**Friend:** …Nauseous beetle.

**Host:** Lenin's queasy. Ugh. What's the next condition?

**Friend:** Inverses. Every automorphism needs an inverse — like the squ-inverse needs a squ-inverse inverse.

**Host:** Okay. They should combine to be neutral: r should end up back at r. We send r to r⁻², and then back to r. Yes — it's the backwards version. Any automorphism goes both ways, so we can just flip it. There are always inverses. And finally, we need associativity, which is boring, so we'll skip it. It's a group. Uh, wait — let's just say we covered it. What were we talking about before? The semidirect product, right? To find all the SDPs, we want to find all automorphisms that square to the EINHEIT-omorphism.

## Chapter 6: Hunting the new group (10:21)

**Host:** The automorphisms of C9 are the group C6 — a six-cycle, which we can see here. These automorphisms have order 6, so they don't square to EINHEIT. And these have order 3, so they don't either. It has to have order 2 — f is the inverse.

**Friend:** It can be the inverse — but it doesn't have to be.

**Host:** Oh? Could it also be the EINHEIT-omorphism?

**Friend:** Yes — the EINHEIT-omorphism does square to the EINHEIT-omorphism. The automorphism doesn't need to have order 2, as long as the order divides 2.

**Host:** That makes sense.

**Friend:** So, what group does the EINHEIT-omorphism make?

**Host:** Hm. f applies the neutral map. So when r passes f, it's still just r. They commute — it's just the direct product.

**Friend:** Exactly.

**Host:** So there are two possible SDPs.

**Friend:** Yes. But this one is abelian, and this is D18. We haven't found a nuke. Maybe we can find a nuke by flipping things around: C2 semidirect-times C9. What does this mean?

**Host:** Now C9 messes with C2. So r should apply an automorphism to f.

**Friend:** Exactly. But the automorphisms of C2 act like C1 — it's only the EINHEIT-omorphism.

**Host:** So then r must commute with f. We only have the direct product.

**Friend:** Yes. And there's nothing special about C9. If we take C2 semidirect-times any G, the elements of G must apply the EINHEIT-omorphism, and we have the direct product. So how could we apply this idea to the remaining cases? Hm — here there's a C2 on the left. That must be a direct product. So it's abelian.

**Host:** Yeah, that case is nupless. Where else can we apply this?

**Friend:** Nowhere, right? Nothing else has a C2 on the left.

**Host:** Not at first glance — but here we can split the C6 into C2 × C3. The right group will mess with them separately.

**Friend:** Okay, so the C2 will just be the direct product. We only have to check the C3.

**Host:** Yes. We'll say this one is generated by a, and this by b. So b should apply an automorphism of the left C3. And the automorphisms of C3 are the group C2: EINHEIT and inverse.

**Friend:** So b can only apply the EINHEIT-omorphism.

**Host:** Why?

**Friend:** The inverse has order 2, but b has order 3, and 2 doesn't divide 3 — so inverse-to-the-3 isn't the EINHEIT-omorphism.

**Host:** Nice. b must apply the EINHEIT-omorphism. Therefore we get the direct product. All the products are direct, so this group is—

**Friend:** —abelian.

**Host:** Yeah. Not a nuke. But we can use this splitting idea in other cases — here we can split the right side.

**Friend:** And we just showed that C3 semidirect-times C3 has to be direct.

**Host:** Exactly. We just need to check C2. And this case is interesting, since the automorphisms of C3 are C2.

**Friend:** So we can apply the inverse map. It's not direct. We might have a new group.

**Host:** We don't. Let's say that C3 is generated by r and C2 by f. So then f inverts r — it's the triangle group, D6.

**Friend:** Yeah — this is just D6 × C3, which we've already seen.

**Host:** But now we're ready for the nuke. We can split this D6 into C3 semidirect-times C2. C3 semidirect-times C3 must be direct. But what about C2? It could be the inverse.

**Friend:** Yes. And this is also the inverse — so they can combine. C2 applies the inverse map to C3 × C3. This is a noop.

## Chapter 7: The final group of order 18 (14:14)

**Computer:** Input generators.

**Host:** Oh. Um — for the first C3: A3 equals EINHEIT.

**Computer:** Did you intend "A3 equals blank"?

**Host:** Yes. And then B3 equals blank, and they commute. And then C2 equals blank, and C inverts A and B.

**Computer:** Preparing bar chart… Bar chart prepared.

**Friend:** Whoa. It's all orders 2 and 3.

**Host:** Yeah. We can think of this as the symmetries of two triangles, but they're messed with by the same C2 — so either both flip or neither flip. If they both flip, that has order 2. And if neither flip, that has order 3. And that's the final group of order 18. To summarize: each group is either a product of C3, C3, and C2 — or of C9 and C2.

**Friend:** They differ based on the type of product.

**Host:** Exactly.

**Friend:** What about the other SDPs?

**Host:** Oh, yeah. We didn't cover these two cases. We'll leave that as an exercise for the users.

**Friend:** The users?

**Host:** Uh, yeah — the users of the video.

## Chapter 8: The groups of order 20 (15:14)

**Host:** It's time to look at the groups of order 20. We already saw the abelian ones — what about nonabelian?

**Friend:** We have the basic ones: D20 and Q20. Then we can multiply smaller groups.

**Host:** Yes, but order 5 × 4 won't work, since those are all abelian.

**Friend:** We could do 10 × 2, using D10 × C2.

**Host:** Yes — though this is not a nuke. It's the same as—

**Friend:** D20?

**Host:** Yes. D20 is C10 semidirect-times C2. We can split the C10. But then notice that we have an SDP with C2 on the left, meaning—

**Friend:** —it has to be a direct product.

**Host:** Yeah. So we can remove that: C5 semidirect-times C2 is D10. So we end up with D10 × C2. Direct products don't give us a nuke.

**Friend:** Then we should check out the semidirect products.

**Host:** Yeah. Here are all of the cases. Where should we start?

**Friend:** Hm. These ones have C2 on the left, so they must be direct products.

**Host:** Yeah, they're nupless. And then these ones have C5 on the right, so the automorphism order divides 5 — it can be—

**Friend:** —1 or 5.

**Host:** But the automorphisms of C4 are the group C2, which doesn't have any elements of order 5.

**Friend:** So it has to be the EINHEIT-omorphism. It's a direct product.

**Host:** And the automorphisms of C2 squared are D6.

**Friend:** Also no order 5. So that's direct too.

**Host:** Yeah — these are both nupless. But then we have C5 semidirect-times C4. The automorphisms of C5 are the group C4: the EINHEIT-omorphism, the square, the inverse, and the squ-inverse.

**Friend:** So we can use the square automorphism, since it has order 4. Is this a noop? Let's see: A4 equals blank, B5 equals blank, BA equals—

**Host:** Oh, uh — it's squared. So AB = B²A.

**Computer:** Thank you. Preparing bar chart… Bar chart prepared.

**Host:** It is a noop. And it's only orders 2, 4, and 5. The semidirect products seem to concentrate elements into small orders.

**Friend:** Yeah, that's an interesting point. D20 and Q20 are also mostly small, but they have some order 10. And then the abelian groups are mostly large. And actually, these are all of the groups of order 20. Let me guess: you're going to leave those other cases as exercises for the users.

## Chapter 9: The groups of order 21 (17:55)

**Host:** It's time for order 21. We saw earlier that there is just one abelian group. What about nonabelian?

**Friend:** 21 is odd, so we don't have D21 or Q21. Maybe we can multiply smaller groups—

**Host:** —but that would have to be 3 × 7, and both are abelian.

**Friend:** So the product would be abelian.

**Host:** Yeah.

**Friend:** Okay. Maybe there's a semidirect product.

**Host:** There are two cases. As we've seen, the automorphisms of C3 are the group C2, which means—

**Friend:** —C7 must apply the neutral map. This is a direct product.

**Host:** Yeah. But in the other case, the automorphisms of C7 are the group C6, which we can see here.

**Friend:** The square map has order 3. So C3 can apply the square.

**Host:** Yes — this is a nuke, and it's the only nonabelian group. These are the only groups of order 21. And that wraps up this episode. Thanks to the recent supporters of the channel. You can learn further by exploring the Cayley diagrams and tables of these groups at the site linked below. We'll see you next time for the groups of order 24—

**Friend:** —and maybe 25?

**Host:** I'm not sure. I haven't planned the full scope of it yet. Like — well, we will get to 25, of course. I just mean that I'm not sure if it's going to happen in the next episode. Like, I— I don't know how long 24 is going to take.

---

## Cleanup notes

1. **Source & timestamps:** The auto-captions were retrieved directly from the video, and YouTube's rolling two-line caption format was deduplicated so that every caption line appears exactly once. Per-line timestamps were stripped; each chapter's approximate start time is kept in its heading. Chapter titles are inferred from the content — the video's official chapter list was not available.
2. **Speakers:** The **Host** and the **Friend**, plus the **Computer** — the group-explorer website (revealed at the end of Part 2) in robot voice, whose lines ("Please input generators", "Preparing bar chart") are kept. This episode hands the Friend long stretches of the math, continuing Part 2's role reversals; labels follow the caption speaker-change marks plus context, and some could be flipped.
3. **ASR fixes:** "aelion / ailion" → "abelian"; "a billion" → "abelian" (five places); "quatronians" → "quaternions"; "semiirect / semmit" → "semidirect"; "STPs" → "SDPs"; "Messing around. Messa ringowns." → kept as the stumble "mess-aroundings — messing around… mess-aroundings"; "The fomorphism" → "The automorphism"; "Einhe / Einheight / Einhyomorphism / inhomorphism" → "EINHEIT / EINHEIT-omorphism"; "Kaly diagrams" → "Cayley diagrams"; "gratitude" → "Thank you" (robot voice); "R 9= Ein" → "R9 = EINHEIT". The computer-input lines systematically lost their exponent digits; restored from the group definitions: "R r equals blank" → "R9 equals blank", "RR is blank" → "R3 is blank", "FF equals blank" → "F2 equals blank", "FR equals R R" → "FR = R8F", "FR equals RRF" → "FR = R2F", "A A is blank" → "A3 is blank", "Did you intend a A equals blank" → "Did you intend 'A3 equals blank'", "BB BB equals blank" → "B3 equals blank", "C equals blank" → "C2 equals blank", "A a A a equals blank" → "A4 equals blank", "BB B equals blank" → "B5 equals blank", "So A A B" → "AB = B²A".
4. **Math corrections:** (a) "Every finite group is the unique product of p p cycles" → "Every finite abelian group is the unique product of p p cycles" — the uniqueness half of the structure theorem (the "true funag") is about abelian groups; (b) "So inverse to the 3 is an Einhe" → "…isn't the EINHEIT-omorphism" — composing the inverse map three times gives the inverse map, not the identity, which is exactly why b cannot apply it; (c) the Host's opening "groups of order 18 through 21" is kept as spoken — it's the joke, and the Friend immediately points out the title says 17 through 23; (d) the garbled case list "C6 C3 C366 D6 C3 and C3 D6" is rendered as "C6 semidirect-times C3, C3 semidirect-times C6, D6 semidirect-times C3, and C3 semidirect-times D6".
5. **Running gags kept as heard:** "funag" and "the true funag" (the fundamental theorem of finite abelian groups; the "true" version adds uniqueness and prime powers); "p p cycles" (prime-power cycles — hence the Friend's "which means prime power"); "SDP" (semidirect product); "mess-aroundings" (his stand-in for "automorphisms"); "EINHEIT-omorphism" (the identity automorphism); "nuke" / "noop" (his slang for a genuinely new group, rendered as heard; "nupless" = yielding no new group); "Easy peasy — nauseous beetle. Lenin's queasy." — a rhyme riff the captions garble (presumably from the "easy peasy lemon squeezy" family), kept as heard; "exercise for the users" (the website's users, not the viewers).
6. **Notation:** products with ×; "C3 squared" written C3²; semidirect products written out in words ("C9 semidirect-times C2") as spoken; equations dictated to the computer kept in its input style (R9 = blank), with capitalized letters there and lowercase in prose.
