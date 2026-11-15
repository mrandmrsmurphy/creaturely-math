# Group Theory Step-by-Step: 16 — Cleaned Transcript

*Video: "Group Theory Step-by-Step: 16" by TheGrayCuber (YouTube, Aug 17, 2025, ~18 min). Third in the series (after "1 - 7" and "8 - 15"; a fourth video, "17 - 23", exists): the semidirect product and all 14 groups of order 16. Two speakers: the **Host**, who explains, and his **Friend**, who asks questions and snarks. Speaker labels are inferred from context, as in Parts 1 and 2. Section headings are content-based; YouTube's auto-chapters are Abelian groups of order 16 (0:00), Visualizing abelian groups (4:35), Introduction to nonabelian (5:07), Checking group differences (6:16).*

---

## Intro: The abelian groups of order 16 (0:00)

**Host:** Welcome back to Group Theory: Step-by-Step! This episode is all about the groups of order 16. There are a bunch of them. And funnily enough, for order 16, the number of groups is 16—

**Friend:** No, it's 14.

**Host:** Okay. Well, let's start with the abelian groups, using the funto.

**Friend:** For anyone who hasn't seen the previous video — that's his nickname for the fundamental theorem of finite abelian groups.

**Host:** It tells us that every finite abelian group is made of cycles. So for order 16, we just find all the factorizations of 16 — each one defines a group. But then we have to check for duplicates by counting the orders of the elements. Sure. So let's do C16: for order 1, there is just one element — 0 — because it's neutral. EINHEIT. Then, how many elements have order 2?

**Friend:** Hm… just 8?

**Host:** Yep — 8 × 2 is neutral. How about order 4?

**Friend:** 4 and 12. Hey — it's always the numbers in the middle of the chunks.

**Host:** Yeah, great observation. So then these four have order 8, and all the rest have order 16.

**Friend:** Nice.

**Host:** We now have the counts for C16. And here are the counts for all the other groups. If any two groups have the same counts, they're the same group.

**Friend:** Wait, that's weird — none of them are the same.

**Host:** Why is that weird?

**Friend:** Well — there's a bunch. I thought there might be at least one pair.

**Host:** No — 16 is a p².

**Friend:** Excuse me?

**Host:** A prime power. The abelian groups are all different when the order is a prime power.

**Friend:** You've got to stop with the nicknames.

**Host:** In the last video, we saw the groups were all different for the prime-power orders 8 and 9. But 10 and 12 are not prime powers, so they had duplicates.

**Friend:** So — why are prime powers special?

## What "isomorphic" really means (1:47)

**Host:** Well, to answer that, let's take a closer look at the duplicates. What does it mean for groups to be isomorphic?

**Friend:** Uh — it means they act the same.

**Host:** Yeah. And the whole point of acting the same is that if we have a calculation in one group, we can solve it — or we can pass it to the other group, solve it there, and if we pass it back, the result is the same. So groups being isomorphic means there's a map between them. And it's conventional to name the map f.

**Friend:** That's not an f.

**Host:** I'm not conventional. The map should preserve calculations. So we could combine a and b, then map — or we could map separately, then combine. Both results will be equal.

**Friend:** And also the map must be one-to-one — a and b can't map to the same place, because then we couldn't map them back.

**Host:** Exactly — it's not clear which path to take. So having a map that's one-to-one and preserves calculations is the same as being isomorphic. In this case, we can map 1 to 1.1—

**Friend:** What?

**Host:** Sorry — I turned European for a sec: (1, 1). Then where does 2 map?

**Friend:** (2, 2)?

**Host:** Yeah, but the left group is a two-cycle — so that simplifies to (0, 2). Then 3 maps to (1, 3); 4 goes to (0, 4), and so on. The first coordinate is the value mod 2, and the second is the value mod 5. Calculations work the same in modular arithmetic, and the map is one-to-one. So it's an isomorphism. Yeah. And we used 2 and 5 in this example, but the map would work for any coprime numbers: if they have no common divisor, the cycles combine. But if there is a common divisor — like with 2 and 4 — then, Houston, we have an issue.

**Friend:** You mean a problem?

**Host:** Yeah, it is a problem. Where could we map 1?

**Friend:** Nowhere. It has order 8. But C2 × C4 doesn't have any elements of order 8.

**Host:** Exactly. If we map 1 to (a, b), then 4 goes to (4a, 4b), which reduces to (0, 0). But 0 also maps to (0, 0). This can't be a one-to-one map — so it's not an isomorphism. If cycles share a factor, they won't combine into one larger cycle. And 16 is a prime power, so all of its prime factors are the same — meaning that any two cycles will share factors. Nothing combines. So all the abelian groups are unique. Let's move on to the non-abelian groups.

## The abelian diagrams (4:35)

**Friend:** Wait — can we look at the diagrams for the abelian ones first?

**Host:** Oh, sure. So C16 is just a cycle. And then here's C8 × C2, which makes two connected 8-cycles. And then let's compare C4 × C4 with C4 × C2 squared.

**Friend:** They both have the yellow four-cycles, but they're connected differently.

**Host:** And finally, here's C2 tesseracted.

**Friend:** Now — can we do non-abelian?

**Host:** Yes, we can.

## The non-abelian groups (5:07)

**Host:** So, of course, we have D16, the symmetries of an octagon.

**Friend:** Oh, it's getting dangerous.

**Host:** Dangerous?

**Friend:** Yeah. Now, the stop sign can flip — people probably won't even see it.

**Host:** No, nobody's flipping stop signs. We also have Q16, the quaternion group. This one is fun: zeta to the 4th is −1. So, zeta is the square root of i. It's like a quadratic extension of the normal quaternions — it's a QQ.

**Friend:** Quadratic quaternions! …I can't think of any other groups, though.

**Host:** Well, what if we multiply smaller groups?

**Friend:** Oh, yeah. We could have an order 8 × an order 2, or an order 4 × an order 4.

**Host:** But all the groups of order 4 are abelian, so if we multiply, we'll get something abelian. So we just have this case: the only order-2 option is C2, so the order-8 group must be non-abelian — it's either D8 or Q8.

**Friend:** Nice. Two new groups! …But I'm not sure if these are all different.

**Host:** Oh, good point. We should check.

## Checking group differences (6:16)

**Host:** Let's look at the orders of the elements — and we'll use Q8 × C2 as an example.

**Friend:** This group is a little weird, since the first operation is multiplication, but the second is addition. It's… multiple addition?

**Host:** Yes. And because it's multiple addition, (1, 0) is neutral. These elements, where the second coordinate is 0, act just like Q8 — that 0 is irrelevant. So 1 has order 1, −1 has order 2, and everything else has order 4.

**Friend:** What about the other ones?

**Host:** Well, we need an even order to make the right side neutral. These are order 4 on the left, so they'll stay order 4. And −1 has order 2, so that also still works. 1 is the only one that changes — it now has order 2. So that's a total of: one with order 1, three with order 2, and 12 with order 4. Here are the totals for the other groups. Let's turn them into bar charts so it's easier to compare.

**Friend:** They're all different.

**Host:** Yeah. This also makes it clear that the quaternions are heavy on order 4, while the dihedral are more order 2. And we can get rid of the 1 bars, since they're redundant — every group has just a single EINHEIT.

**Friend:** Can we see the charts for the abelian groups?

**Host:** Yeah, here they are.

**Friend:** Whoa. What's up with C2 to the 4?

**Host:** Yeah — each coordinate is a two-cycle, so there can't be any elements with order more than 2. On the other end of the spectrum, C16 has an extra bar: it's the only group with an order-16 element, because if a group has an order-16 element, it's C16 itself. And these two have the same counts — but they can't be the same group, since one is abelian and the other is not.

**Friend:** They're kind of similar, though. On the left, we have two separate four-cycles. And on the right, i and j each make a four-cycle, but they overlap since they share a square.

**Host:** Hey, that rhymed.

**Friend:** Oh yeah — I'm a poet and I didn't even know that I was one of them.

**Host:** Well, you ruined it. Anyway — the cycles overlap, but there's an extra two-cycle that makes up for that.

## The semidirect product (8:30)

**Friend:** What about the other groups? You said there were 14, so we're still missing 5. What if we multiply smaller groups?

**Host:** We just did that.

**Friend:** What if we… semi-multiply?

**Host:** What does that mean?

**Friend:** Oh, sorry — lorry-multiply, for the overseas viewers.

**Host:** What does it mean, mathematically? The multiplication we've done so far is called the direct product. But there's another type called the semidirect product. It's a little more tricky, but a lot more useful. Let's use D16 as an example. We have: rotate-to-the-8 is neutral, flip squared is neutral, and rotate gets inverted when it swaps with flip. But what if it didn't get inverted?

**Friend:** Then they commute — this would be an abelian group.

**Host:** Which abelian group?

**Friend:** R makes an 8-cycle and F makes a 2-cycle — so C8 × C2?

**Host:** Exactly — it's the direct product. But D16 is the semidirect product: the two-cycle messes with the 8-cycle by inverting the rotation. They're not independent.

**Friend:** Are all of the D-groups semidirect products?

**Host:** Yeah: D2n is Cn semidirect-product C2. But in the 16 case, we should clarify by noting this with a −1, because the SDP is not unique.

**Friend:** SDP — oh, got it.

**Host:** This one sends r to the −1 power. But we could instead send it to the third power.

**Friend:** Would that be a different group?

**Host:** Let's count the orders of the elements. All the powers of r work as expected. How about rf? If we square it: then swapping takes r to the third power. So that's r⁴, and then flips cancel each other out. Then square again, and we get r to the 8, which is neutral — it has order 4. How about r² f? Swapping takes the square to the 6th, so that cancels with the r squared, and then the flips also cancel — it just has order 2. Yes — and the other elements with an odd power of r have order 4, and the even powers of r have order 2. So that totals to 5, 6, and 4. Here's the bar chart.

**Friend:** It's different. This is a new group!

**Host:** And we can get another new group by sending r to the fifth power. Here's that bar chart.

**Friend:** Interesting. What if we send r to r squared?

**Host:** Nope. Nope. Nope.

**Friend:** Is that not a new group?

**Host:** It's not a group at all!

**Friend:** Wait, why not?

**Host:** Let's try it out: r does not equal r to the 5th. But if we apply flip, then swapping doubles the powers and— oh, they end up being the same. Yeah — the f-swap is a map, and r and r to the 5th got mapped to the same element. It only works if flip is a one-to-one map, like going to the third power. But it's not just any one-to-one map.

**Friend:** Is it an isomorphism?

**Host:** Don't spoil it! Let's say f adds 1 to the power of r. This is one-to-one, but it doesn't work. Let's say we have f·r³: if we swap separately, then combine, we get r⁴ f. But if we combine, then swap, it's just r³ f.

**Friend:** Yeah — this is not a group?

**Host:** The flip changed the calculations. The flip map must be one-to-one AND preserve calculations.

**Friend:** So it's an isomorphism — like I said earlier!

**Host:** Yes, it must be an isomorphism. And C8 has four isomorphisms to itself: the inverse, the third power, the fifth power, and just neutral (r to r). So we have four different SDPs.

**Friend:** Wait — with the neutral one, doesn't that mean that r and f commute? That's just the direct product.

**Host:** Yeah — the DP is just a neutral SDP. And here are the diagrams for these groups. You can see the different ways that the two-cycle acts.

## C4 ⋊ C4 and a second test (12:45)

**Host:** So now let's use the SDP to find some other new groups.

**Friend:** What about C4 semidirect-product C4? How would this work?

**Host:** Hmm — maybe let's start by asking what is possible for the left group.

**Friend:** Well — of course, the neutral isomorphism. And we could also invert everything. I can't think of anything else.

**Host:** Good, because there is nothing else. Since everything is a multiple of a, we can explain the entire map by where a goes. If it goes to itself, that's neutral. If it goes to a cubed, that's inverse. But if it goes to a squared, then a cubed also goes to a squared — it's not one-to-one. And the same thing happens if we map to EINHEIT.

**Friend:** Yeah. So these are the only two isomorphisms. But if we use the neutral one, we just get the direct product — so let's use the inverse map.

**Host:** Great. We have a with order 4, and the second group has b with order 4. And when a swaps with b, it gets inverted. These equations describe the group.

**Friend:** Hey — it looks like the quaternions!

**Host:** It does — the quaternions have the same equations.

**Friend:** So is this a quaternion group?

**Host:** No — the quaternions have an extra equation: j² = i². They're both −1. On the left, this is not true. And so, in a sense, C4 ⋊ C4 is more concise than the quaternions — we need fewer equations.

**Friend:** The bottom equation replaces the second one?

**Host:** Oh yeah, it does. So in a sense, these groups are equally concise. And these definitions using equations are really useful, particularly with computers. It's what I do when writing code to make the diagrams and tables. For this group, we have three equations. So we tell the computer: replace any value on the left with the value on the right. Although, instead of "a to the 4," we use a blank — and the same with b. And then e is blank.

**Friend:** Blank?

**Host:** Yeah. The elements are words, and the operation is to smush them together. So a blank is neutral. We can smush any two words, and the equations will simplify into 0 to 3 a's followed by 0 to 3 b's.

**Friend:** That's 16 options.

**Host:** Yes — every element has a unique representative word. So now we can make the computer count the orders of the elements. Here are the results.

**Friend:** Cool. Wait a sec — it's the same as Q8 × C2!

**Host:** They do have the same counts. But they're not the same—

**Friend:** —right? Since they're not abelian: same counts might not mean same group.

**Host:** So we need a second test. Let's count the squares. Here are the groups' tables — the squares are the entries on the backslash. C4 ⋊ C4 has three different squares, but Q8 × C2 only has two.

**Friend:** Yeah. So they must be different groups.

**Host:** If they were isomorphic, the map would connect squares — but that map can't be one-to-one. Let's put three squares here and two squares here to remember why they're different.

**Friend:** Nice. I like it.

## The final two groups (16:06)

**Host:** We have a similar situation with the final two groups. First, there's C2 squared ⋊ C4, where a and b generate the two-cycles, c generates the four-cycle, and the c-map swaps a with b. And second, we have Q8 ⋊ C2: of course there's i and j, then a makes the two-cycle, and the a-map inverts i, but it doesn't change j.

**Friend:** These groups have the same counts, but they're not isomorphic — different counts of squares.

**Host:** Exactly. Here are the tables. It's three squares versus two squares, just like before. So — here are all of the groups of order 16. Of course, there are a bunch of other SDPs we could try out, like this one — but they'll always be isomorphic to one of the 14. And actually, this example has four different possibilities, depending on which isomorphism of C4 × C2 we use. And that wraps up this episode. Thanks to Balik and Garbage Boftutor for supporting the channel.

## Outro (17:17)

**Friend:** I'm tired of making videos.

**Host:** Yeah, I get it. I'm tired of only doing group theory. So let's put a pause on this series. But don't worry — I've got a bunch of other cool videos planned. And in the meantime, you can learn more with my interactive group visualizer, linked in the description.

**Friend:** It's really cool!

**Host:** I've added all of the groups of order 16. And I've also added a setting to see the generators — how the computer stores elements when we define using equations. So check it out, and we'll see you in the next episode.

*[Post-outro beat: "A… a-b… ab."]*

---

## Cleanup notes

1. **Source:** Auto-generated captions, pulled from the video's transcript panel (164 caption segments). Duplicated timestamp markers stripped; section start times kept in the headings.
2. **Speakers:** Split into **Host** and **Friend** as before; attribution of the shortest interjections is inferred from context.
3. **Garbled words fixed:** "a billion" → abelian (throughout); "quatian(s)" → quaternions; "isomeorphic" → isomorphic; "semiirect" → semidirect; "nonabilian" → non-abelian; "height" → EINHEIT; "more order too" → order 2; "particularly ly" → particularly.
4. **Jokes kept/decoded:** "16 is a p²" (captions' "pee pee" — hence "Excuse me?"); "peeps"/"pee orders" = prime powers; "1.1" read as "one and a tenth," then "I turned European for a sec: (1, 1)"; "lorry-multiply" — the Friend's pun on "semi" (semi-truck = lorry, for the overseas viewers); "Houston, we have an issue" → "You mean a problem?"; the mangled idiom "I'm a poet and I didn't even know that I was one of them"; DP/SDP abbreviations; "C2 tesseracted."
5. **Math reconstructions:** "map one to one and a 10th" → map 1 to 1.1/(1, 1) in the C10 ≅ C2 × C5 example; "4 A, 4 B" → (4a, 4b); the order counts for C8 ⋊ C2 (5, 6, 4 for orders 2, 4, 8) verified; C16 is the only order-16 group with an element of order 16 (such an element generates the whole group); element-pair shorthand and "(1, 1) → (0, 2)" simplification reconstructed.
6. **Uncertain renderings (as heard):** the Ko-fi supporter names "Balik and Garbage Boftutor"; "instead of a to the 4, we use a blank" (captions: "we use ah"); the closing post-outro caption "A a b ab" (the word-smushing gag — attribution unclear); the "three squares vs two squares" counting for C4 ⋊ C4 vs Q8 × C2 is as spoken.
7. **Presentation equations:** j² = i² for the quaternions; the group word notation ("elements are words, the operation is to smush them together") kept in the Host's own phrasing.
