# 2026 Conference Stripe Integrations

## Status

Stripe setup is substantially complete. The immediate work is checkout testing, conference-page completion, and registration email launch.

## Objective

Provide WASSP's 2026 conference registrants with clear card and check payment paths while ensuring WASSP receives its intended registration revenue, captures the information needed to run the event, and deposits Stripe proceeds into the conference bank account.

## Source

- Notion meeting: [WASSP Stripe SOW — July 12, 2026](https://app.notion.com/p/39b2b47bfc6980ddb6b5d9918f0b9b78)
- Meeting note and transcript captured below on July 12, 2026.

## Scope of work

### 1. Stripe payout configuration

- Use the linked conference bank account ending in **1912** as the payout destination.
- Retain the general account ending in **4428** as the other linked WASSP account.
- Run automatic payouts weekly on Mondays.
- Use standard settlement; do not pay for instant payout.
- Stripe processing fees are deducted from each payment before payout. There is no additional standard bank-transfer fee.

### 2. Registration products and pricing

| Registration type | Card price | Expected net after 2.9% + $0.30 |
| --- | ---: | ---: |
| WASSP member | $259 | $251.19 |
| Non-member | $465 | $451.22 |
| Aspiring/associate leader | $155 | $150.20 |

- Keep the older $250 and $257 member prices archived.
- Check payments may use the base registration amount without the card-processing cushion.
- Maintain separate Stripe payment links for each audience rather than asking Stripe to determine membership eligibility.

### 3. Checkout information

Each Stripe checkout must collect:

- Name
- Email
- Phone
- School
- School position
- Shirt size

Stripe should automatically send the payer a receipt/invoice.

### 4. Checkout testing

- Enable promotion-code entry on the relevant payment link if required.
- Use the **Jeff Internal Testing** 100%-off code to complete a checkout without charging a real card.
- Confirm all registration fields appear in Stripe and can be retrieved for reporting.
- Confirm the successful-payment experience and automatic receipt.
- Confirm the correct product, price, and conference payout route.

### 5. Conference registration email

Prepare the member launch email with:

- A short conference introduction
- A clearly labeled $259 member-registration link
- A link to the 2026 conference webpage
- A printable check-payment form
- A specific subject line aimed at WASSP members

Send a separate campaign to non-member principals using the $465 link. The meeting placed this outreach in August. Handle aspiring/associate leaders as a separate audience when needed.

### 6. Check-payment path

Provide a one-page, printer-friendly form that collects:

- Registrant name
- Position
- School
- Email
- Shirt size
- Conference name and dates

Include instructions to make the check payable to WASSP and mail the form with the check to the approved address. Keep the document simple because check payments are expected to be a minority of registrations.

## Deliverables

- Three working Stripe payment links
- Confirmed weekly payout configuration to the conference account
- Successful zero-dollar end-to-end test
- Updated 2026 conference webpage
- Member registration email
- Separate non-member registration email
- Printable check-payment form
- A repeatable registration export/reconciliation process

## Owners and dependencies

| Owner | Responsibility | Status |
| --- | --- | --- |
| Jeff | Collect Reggie Miller's remaining bio and send all speaker materials to Jacob | Pending |
| Jacob | Update the 2026 conference webpage with current headshots, bios, schedule, location, and dates | Pending; blocks email |
| Jacob | Crop the WASSP logo to remove excess white space | Pending |
| Jeff | Send the member registration email after the webpage is ready | Blocked |
| Jeff | Send separate non-member outreach in August | Planned |
| Aaron / Jeff | Test the Stripe checkout and verify collected data | Pending |
| Aaron | Help finalize the email subject line and formatting | Pending |

## Acceptance criteria

The Stripe work is ready when:

- All three payment links show the correct price and collect the required fields.
- A 100%-discount test completes successfully without a card charge.
- The test registration can be found with every required field.
- Automatic customer confirmation is received.
- Weekly Monday payouts point to the conference account ending in 1912.
- The member email contains the correct payment link, conference-page link, and check form.
- Older pricing cannot be accidentally selected.
- Jeff can retrieve registration information without rebuilding the setup.

## Out of scope for this phase

- Meal RSVPs; collect these closer to the conference.
- Automated reconciliation of Stripe registrations and photographed paper forms into Google Sheets. This is a future improvement.
- TeacherCon presentation development.
- A broader website redesign.

## Open questions

- What mailing address should appear on the check-payment form?
- Are refunds and cancellations allowed, and who approves them?
- Who has final approval authority for the checkout experience and registration email?
- What is the exact member-email launch date?
- When should the aspiring/associate leader link be promoted?
- What export or Google Sheet will serve as the registration roster?
- Is sales-tax treatment already confirmed for these conference registrations?

## Decisions

- Card prices are $259, $465, and $155.
- Conference proceeds settle to the conference bank account ending in 1912.
- Payouts run weekly on Mondays.
- Member and non-member audiences receive separate links and email campaigns.
- Meal information is not collected in Stripe.
- Check payers use a separate printable form.
- The conference webpage must be ready before the member email is sent.

## Next actions

1. Jeff gets the final speaker bio to Jacob.
2. Jacob completes the conference webpage and logo crop.
3. Aaron and Jeff run the zero-dollar Stripe test.
4. Confirm the check-payment mailing address.
5. Finalize the member email subject line and copy.
6. Send the member registration email after the webpage passes review.
7. Schedule the separate non-member campaign for August.

---

## Notion meeting note and transcript

The following is the complete source meeting note pulled from Notion. It is retained as the factual record behind the scope above.

<meeting-notes>
	**WASP 2026 Conference Stripe Setup & Email Campaign Planning** **<mention-date start="2026-07-12"/>**
	<summary>
		### Action Items
		- [ ] Jeff to collect remaining speaker bio from Reggie Miller (Riverton) and send all bios to Jacob [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981b58f68d6528407a9f2] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69816e84fcdc663c5c08bb]
		- [ ] Jacob to update the 2026 conference webpage with new speaker headshots and bios [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981719f94f6919c2e38d6] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981cd9b16cd474f6a1568]
		- [ ] Jacob to crop WASP logo to remove excess white space [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981c8b98cd21f421cdd4f]
		- [ ] Jeff to send conference registration email to members once the website page is ready [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69818ea9c4df56166deef4] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69816e84fcdc663c5c08bb]
		- [ ] Jeff to target non-member principals with separate registration email in August [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69811f8f8fce5c79ec8732]
		- [ ] Check with Aaron on a catchy email subject line (avoid generic "Educational Leadership Conference 2026") [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981478d53c9db7d212004] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69813ab252ed7b5c346ff1]
		- [ ] Test the Stripe checkout using the 100% off coupon code ("Jeff Internal Testing") to verify data collection [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981ae8302dd048a46642c] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981439898cbd365a8c34a]
		---
		### Stripe Bank Account & Payout Setup
		- Two bank accounts confirmed linked at First State Bank of Wyoming [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69816a9ea3ec3f9725c21f]
			- General account ending in **4428**
			- Conference account ending in **1912** (primary for conference payments)
		- Payout schedule set to **weekly on Mondays**, settling to the 1912 conference account [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69817d8b61f225c7332c0b] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc698113b042cdda2b621267]
		- Stripe fees are deducted at time of payment, not at settlement — no extra fee to transfer to the bank [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc698149a51fe669710b9be1]
		---
		### Pricing (with Stripe Fee Factored In)
		- **Member:** \$259 → nets \~\$250 [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69814a8db8c21d171f4231] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981c28d54e1635d4abf29]
		- **Non-Member:** \$465 → nets \~\$450 [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69819fa2e4c90e6272b5c6] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981dabaebc5416d6f7978]
		- **Aspiring/Associate Leader:** \$155 → nets \~\$150.20 [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981c28d54e1635d4abf29] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981b68e70f2c80a56d20b]
		- Previous archived prices (\$250, \$257) archived to prevent confusion [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981f08439ed8f8996828e] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981b79229c153752ae491]
		---
		### Three Stripe Checkout Pages Created
		- **Member (\$259)**, **Non-Member (\$465)**, and **Aspiring Leader (\$155)** payment links created and saved in the shared Google Doc [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69811b8623f348b217fa0d] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69812fa96cd96c7adccfe2] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69819d8b7ae51426bca85d]
		- All checkout pages collect: **name, email, phone, school, school position** (pre-filled "Principal"), and **shirt size** (pre-filled "Men's XL") [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69812d92e5d3d3e1d459a3] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981ba9b68e21dca6a30f0]
		- Registrants receive an automatic Stripe invoice — no need to issue manually [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981ab9336fe206b152b8a]
		- Strategy: send members the \$259 link; separately target non-members with \$465 link; no need to verify membership status in Stripe [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981679271c163c38dfdaa] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69810fb43bfa3ccdc3896a]
		- Meal RSVPs will be collected separately closer to the event (not on Stripe form) [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981be9d12cce7e514782a]
		---
		### Email Campaign Plan
		- Email targets: WASP members initially; non-member principals separately in August [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69811f8f8fce5c79ec8732] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69819eba7de62c796c3627]
		- Email will include three components [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc698187b18ef055fa937c18]:
			1. **Stripe checkout link** (member \$259) — displayed with clean anchor text like "WASP Registration Link," not the raw Stripe URL [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981989f05c7533d63d328] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981d283dddd9e42cb9c20]
			2. **Conference info webpage link** (speakers, keynotes, schedule, location — Ramcota, Nov 1–3) [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981acaf2cf4660100f5fd] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69818c909af55c0f5413fe]
			3. **Attachment** for those paying by check (see below) [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981faa744ca62a65a42e2]
		- Email is **blocked on the conference webpage** being ready (Jacob's task) [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69818ea9c4df56166deef4]
		- Subject line guidance: avoid generic names; use something specific to WASP members, e.g., *"Reserve your spot at WASP's Leadership Conference"* [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69813ab252ed7b5c346ff1] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69816f849be8a83607b880]
		---
		### Check Payment Form (Google Doc Attachment)
		- Duplicated from existing registration form and simplified for check payers [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc698178b688e24d3d8f66ba]
		- Collects: conference name/date, registrant name, position, school, email, shirt size [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981a38838dd47b9a1110c]
		- Instructions added: *"Make payable to WASP. Mail this form \[with check\] to \[address\]"* [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981509bf3c17092d34b08]
		- Intended as a printable email attachment for the small number of check payers [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981a98674d863e3cf8b8e]
		---
		### Other Topics
		- **Stripe coupon code** created ("Jeff Internal Testing," 100% off) for testing the checkout flow without real payment [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981439898cbd365a8c34a]; may require enabling coupon use on the product page [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981b28744facc127da232]
		- **TeacherCon presentation** briefly discussed — Jeff plans to use Google Slides as simple talking-point discussion guides for a small-group leadership session [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981dead0be4fbb57ee288] [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc6981a3941fd33e1482f052]
		- Long-term: system to reconcile Stripe and paper check data into a Google Sheet via photo capture was mentioned as a future improvement [^https://app.notion.com/p/39b2b47bfc69800b8d70d67ab85a6072#39c2b47bfc69818885a8dcc0650726be]
	</summary>
	<notes>
		<empty-block/>
	</notes>
	<transcript>
		<empty-block/>
		So what are you trying to connect to? The bank that it's going to get deposited in?
		Yeah, I want to see if I set it up. I'm pretty sure I would have. Set it up to a WASP bank account at the state bank. How do I find it out?
		And you didn't have any financial connections?
		The left?
		I don't know. That's theirs. Let me click around and then I'll see. Okay, go ahead. Superstar of one man. Have you taken in any payments? No. So you've never got one?
		No, I sent you a test in one time way back in November. And you said it looked like it was going to be good. I created some invoices.
		Yeah.
		So if you've never done it. But I think when I set it up, I had this, I had this set up with a,
		- Can you?
		Yeah, that one. Right. What's this, though?
		- Here we go.
		First State Bank of Wyoming. Do those look right? - Yeah, so does that mean, so those are two different accounts. So... - This is specifically for conference payments, the 1912? - Yeah, that's what we wanna do.
		Okay, well they're linked. But how do you select one when you go to do like a link, make a link?
		It doesn't matter until you want to rectify, like cash out all your payments. Stripe holds your money. It doesn't go into your accounts right away. And then you can say like every month deposit it. That's actually the last thing.
		It doesn't automatically go in there.
		No. That's how they make money is then they'll say if you want it immediately you pay a higher fee and then you can have it settled automatically.
		Well how often do they, do you have to request for it to be transferred in?
		You can set an automation like every first of the month or every Monday do a transfer and then it's like three to five days until it settles.
		So just to avoid, I want to avoid a higher fee, so how, the quickest possible.
		And that's at the end, we'll worry about that, because until you have the checkout pages.
		Okay, so I did set that up. So First State Bank of Wyoming is connected. Let me double check to make sure those last four digits are just correct.
		General account ends in 4428. Conference account ends in 1912.
		Conference account 1912. Yeah.
		And the other one was 4428 general account. Yeah. So where did you go to do that again? Under business settings? So let me go all the way back. In the top left, you click your Wyoming username. In the top left, go to Settings, Business, and then Linked External Accounts. Let's just double check this. What's that? So this is the bank that it settles to. It's in U.S. dollars. It's a free settlement fee, which is what you want.
		What is that?
		Basically, you're not paying money to settle from Stripe to you. Now, this is the payout schedule. So you could do something like... If it doesn't cost. It doesn't. You could just say every Monday, settle. Whatever's in my Stripe account goes to my Glacier Bank, whatever this is.
		No, is that 1812? We have to select. That's what I'm saying. Do we need to select? Because I want to select the conference account.
		Are you gonna want anything to go to a different account ever from Stripe or do you know?
		I don't really know but for now conference is the main thing. That's the 1912 account. Yeah. So we're right.
		Can you guys turn that down please Matt or Miles whoever has it.
		So it's set up with the right cam.
		Yeah 1912.
		How come it's showing that one not the other one? Isn't that the one you want? We just made a default time.
		Yeah. That's when we want. This was all set. I didn't change it. All I'm going to do is say weekly on Monday. I didn't know that was possible. Yep. So you never have to worry about it. Okay. And then... You aren't paying anything yourself with stripe as a payee, correct? You're only collecting money. So there's no reason to keep a minimum account because some people like keep 500 just like a savings.
		You don't have to do that. And you don't need a descriptor. So now on Mondays, every dollar you have in your stripe account will get settled to your conference account.
		- Did they take out the three point whatever percent then?
		- When it hits Stripe, not when you transfer. So if I pay \$100 on your invoice, Stripe is gonna give you like 96 or whatever the balance is. If that 96 is in your Stripe account on a Monday, it settles it. There's no extra fee to put it in your bank.
		Can we do a test one?
		You have to pay a stripe fee on it, so no, I wouldn't. This is the fancy stuff that matters that you, oh, you already set this up? Yeah, back in November. Is that? I don't know if it's right, but I just. I mean, it's good enough. I'm impressed. Because you want your invoices to have your logo on the colors. It makes people feel good because they're about to pull out a credit card. Yeah, it looks good.
		Okay, I mean, it's good enough to work, so we don't need to worry about it. Okay. Okay. I think we're ready to create a link. So you already have these set up. We're in your product catalog.
		Yeah, and so I adjusted some of these to...
		Non-members 450...
		Where's the conference fee? Right here. There's that non-member... Where's the member... New membership rate? No, that's for... That's for a lawyer.
		Here's the... Two prices, yeah. So... 257 and 250?
		Yeah, so... I want to get 250, supposed to be 250, but I'm thinking in the Stripe account that's 3% basically.
		So I'm kind of hearing out, put it 259. Why? Because one, you want to end up with 250, you're not going to get 250. It's going to be 240 something. And two, just pricing psychology, everyone who pays 257 would also pay 259.
		So by check it's going to be \$250 and by credit card it's going to be on my flyer. That's what I have, \$259.
		That's fine. And people understand \$9 for a credit card fee is fine because you're paying for convenience.
		Okay, so then we need to change that.
		So I'm just going to... It should show you how... So it's a one-time flat rate...
		I had a hard time adjusting the price on this and so basically I couldn't have you create a new one?
		You shouldn't have to. We should delete that one if we could. I wonder if we just go into this. Price was used in a transaction. Yeah, we have to make a new price. But can we just delete the old ones? Yeah, let's just archive it so it doesn't no one's gonna be able to access it, but it's still viewable.
		Let's go back.
		- Maybe I create a new-- - New price. One time. Flat rate. Type in your 259. Do you want to say conference? And then here's what I would do. This is to make your stuff searchable. Is do something like conference member 2026. And I like to put conference. I'll show you how I do this. It's called the kebab case. It's fine. So I'd go conference dash member. and it's 2026 conference, right? Yeah. It's just to make things searchable and the naming so it's organized.
		Okay, that's the only one people should be able to see because these are both archived.
		Do you have to hit default on that so it selects that? Well, there's only one. Oh, because the shows are archived.
		We can, but it won't matter.
		Now, my question is, we probably won't have many of the others, but we could. So...
		As in a non-member 2026 conference?
		A non-member, an associate member. So can I go into my Google Drive?
		So hold on before we do this. How are you going to disseminate the sign-up? You're going to email all your members and say, hey, the conference is coming up. Here's a link to get registered.
		I also want to send it out to... I'll do that for sure because I have a membership list. So I'll send it out to my membership list.
		Via email.
		Via email. Okay. I also want to send it to principals who are not members. I've got to do some digging. Targeted email.
		Okay. So you're not going to put in an email, if you're a member, click here. If you're not a member, click here. Those will be separate messages.
		I don't know. I showed, let's just kind of pull up my Google Drive.
		We'll keep that there, but just pull up my Google Drive. Yeah, sure. Get to the registration thing.
		And I was just going off of this is what he used, a hard copy that he just sent to people, you know, in an email. Then we'd fill it out and manually send it in or whatever. And they would mail it to you with a check? Or scan it, send it in to him. That's what he used last year.
		He was in charge of it. Do you know how many non-members you got? Not very many.
		One thing I was going to ask is like, just on this thing here, I don't want to make it too small, but there's so much space in here. Is there a way we can... Yeah. I mean, I tried to shrink it, this and that, but...
		What you need to do is, it's called cropping it. So cut out the white space, and then you can make it, the logo's bigger without taking up more room. But we can't do that in Google, so that's another problem for another day.
		So you can't do that on this farm? No. Because I barely got everything on this form on one page. I don't want two pages.
		So you're going to send this in an email.
		Yeah. So we're going to go 159. Is that what? No, wait. Wasp member 259.
		Oh, yeah.
		So I got to adjust all these then. So this was for It was \$4.50, so I want to get \$4.50. I put \$4.63. Just keep it or what? That's \$13. I mean, we're probably not going to get any of those. I don't know if we did last year or not. So you did \$4.63. Yeah, I did. That's 3%. A little under 3%. It's 50 cents less than 3%.
		Let me look. What? I mean...
		Because if we keep it...
		You're going to get \$4.4927 because it's a 2.9% plus \$0.30.
		Out of \$4.63?
		So you're going to be \$0.70, \$0.73. Keep it there then. But I'm just telling you, you might as well do \$4.65. Okay. No one is not going to do it. And we probably don't even get them anyway.
		Yeah. Okay. Um... What do you want to get? \$155,000. I want to get \$150,000. And we're...
		You will get \$149.23 on that.
		So \$155.
		Yeah. Yes. Okay, so that's good. you will net 150 and 20 cents if you charge 155.
		So, okay. So anyway, that's that. We can put this over here. Back to this. So my question is, with the link that we put on that form, do we have to put three different links on? Like if you're a member, it's 259. If you're an associate, it's this. How do we do that?
		Here's the problem. Your member list is a Google Doc or a Google spreadsheet. It's an Excel. Well, it's an Excel. In your Google Drive or in your Microsoft? Where's your master list? If someone says I'm a member and you have to reference yes or no, are they a good... It's not an Excel spreadsheet. So here's the hard thing. If you send a checkout page that says member or non-member these different prices, to get Stripe to enforce the fact that they're actually a member, you have to have...
		A list of people. Oh, that's a pain. Yeah. So what I would tell you, let's do the simplest thing. Just do that. Target people. So if you're going to go look up principal non-members and dig for their contact info at the state or something. Send them a different link. Have just this payment. It's only the 469 or whatever we said. And it only links to that in that email. Because where else is a non-member going to find it unless they text you or somebody knows one?
		website so that your members get one link to one checkout page for 255 and make those separate products so you don't have to try to check do they have an account are they in good standing because maybe they remember two years ago but not this year you can do that but it's not worth the headache
		Especially the first time you get a nice very few people that are going to fit into those categories So don't build an elaborate thing to make sure three people pay the higher fee because so what you're saying is just create a link for the 259 for all the members which is going to be 98% of all the people attending us and then when I go to target I want to send a different registration link to the non members and
		Yes.
		Then make that. So then do I have to make a link?
		We'll copy. I'll link that. But wait. Make this with t-shirt size, name, email, images, like whatever it's going to look like besides the price. Then you can just duplicate it and all you have to do is change the member to non-member and the price.
		The link.
		It's going to be a checkout page that the link takes them to on your stripe. And it's like, pull out your credit card, John Smith, school, district, t-shirt, check here to say I'm a member. Okay, so we have to do that basically like an invoice thing for each one. But do one, make it look nice, make it work, and then you duplicate it and make a non-member one. We have one. Do you have all the info you're collecting in the checkout page?
		Like the name, the school? I don't have that. I don't have that. See, that's what I was wondering is like... So you don't need that Google Doc, Jeff, with all this stuff. Well, how do I... Stripe can collect all that on the same page they pay you. And you'll get t-shirt size, name, school. Are you going to come to the Monday fun thing? Because the problem with the Google Doc, what do you want them to do?
		Copy it and share it? It's a pain in the ass. And then you have a Google Doc record and a Stripe record for payment. You don't want two different systems.
		So I just want, on the Google, I just want notification that we're having this conference. Here's the dates. I don't know what else we want to put on there that we don't want to collect in. You know what I mean?
		Really, instead of a Google Doc, you just need an email. You shared this with me, right? Yeah. I'm sure it should be the updated one.
		Well, what I want to do too is I built a quick, I want to do a preview of the speakers, the presenters. I have a little bio for everybody. I'm waiting on one person.
		And where do you want them? Put those on the form so they see who's speaking.
		I want to send that with, I was going to send that with this.
		So Stripe is the place to put that because you want them to click through and see big name, keynote speaker, local person they know, whoever. That's called a checkout page. So it's a website that's also going to take their payment, their info, put it all in one place. Trust me, because you're giving people three jobs. Okay. They're gonna be like where is that someone won't give you Google Docs someone will get frustrated not register and
		I haven't put that together yet, but I mean, it's in Google. I have them separate like Google, you know, page for each of the presenters.
		And you already have those confirmed?
		Minus one. Yeah, I got them all. They're all confirmed, the presenters.
		You just don't have the one's bio or something?
		I'm missing one bio. Reggie Miller from Riverton.
		Can you steal their picture from their school website or their LinkedIn and say, hey, I got to get this going, get it to me Monday, or I'll steal your...
		If you just show me how to do it, I could probably finish it up. But it's like I got... Got a headshot, and then I got what they sent me. I just put in what they sent me.
		So your Stripe page, you don't want all that, but you can do picture, name, school district, and do a little preview across the top of your big name speakers.
		Okay, well this stuff I'm going to have on the, I make it for my website, so I can have it on the website in more detail.
		Yeah, and you could do something like, After they register, what you should do is the Stripe invoice comes to their email like, "Thank you for paying. We're excited." You can point them towards something like your website page for the conference and say, "If you want to read more about the speakers and the scheduling, click here." Okay.
		So what do you think the next step should be?
		So this is a product.
		That you're gonna sell now we need a checkout page to house this product Checkout page which I thought we had that's under billing Isn't it just invoices?
		Invoices is how you just send someone, hey, you owe me money.
		I can't remember what I put. We saw it, what I had.
		I mean, you have a product now with a price.
		Yeah, but that thing we saw, remember you said, oh.
		That's just the default branding, like your logo and color you're talking.
		Well, we had a deal. Yeah, it was...
		So let me see your mouse here. So let's say we want to do this membership 259. It's previewing the page when they click that link. What do they see? Is there anyone who's going to do more than one like a principal books? Yeah, they could do multiple ones. What's the max realistically? Somebody's like 10. Yeah, never that high, but okay. Here's where it gets fun. You want their name? You don't want business, we want school, but we can do some custom stuff, I think.
		You want their address? Yeah. Do you need a phone number? Yeah, we should. And then down here, we want custom fields. So let's actually tick off business, it'll confuse them.
		Okay.
		I want school and district. So you want district first, I assume?
		School.
		I think school first. Okay, we can...
		I don't even know why I need district. District helps you with the mailing. If I need to send them a follow-up, I know what district they're in.
		So we want school, and they have to answer it, right? Okay. You need a t-shirt size? Let's do district next. School district.
		Or just district.
		Pull up your Google Doc and see. Position. We're already going to get their email, so we don't need to worry about that. Do I need to know if they're a member? This is only to members. Because if you say non-member, no one's going to pay that. You have no way to enforce that they're actually a member. Let's put school position.
		School in front of that. I think it's more descriptive. Sure. And they have to answer that? Yes. System principle or whatever. And now we want t-shirt size, shirt size, whatever. I think I'm running out of...
		Let me put...
		We can get rid of... We can get rid of phone number if you want.
		Well, I think district is probably... If we have the school on their position, I thought you could... I've never tried to put more than three, so... Okay. You definitely need t-shirt, right? Yeah. Let's just change this. We can rearrange. Is it t-shirt, jacket? No, shirt size.
		Men's? Yeah, men's versus women's. Do you order? Yes. Difference. Is there a way we can... Well, I just know that by their name. But some women like men's sizes too.
		Specify men's or women's. and you can do a default so you could do something like this men's xl like if they don't hit anything they'll see this as an option so they can say wl so they put in the sizes they have to unless you do a drop down with all of them it's a pain in the ass i'll show you
		I just want to know that if they do a large, I know it's a women's large or a men's large.
		You can only do eight options, so you're going to... Okay. Because you can't get like triple XL and quad XL and women's.
		Okay, so what I'm saying is I'm fine with them putting in their size, but I will know they have to write in men's or women's.
		And they'll see... That's men's XL. It's a default value. It's already in the box. So then they're going to erase that and go... It's just given them... It's called helper text. Like in school position, you could say assistant principal. Okay. In fact, maybe we should do that. What? What's the default school position? Principal. Principal. One, it saves them time because most people go, oh yeah, that's what I am.
		I don't have to type it.
		They're going to know that they can change it?
		Yes. Because look, there's a box. This is the preview. School position is pre-filled principal. Pre-filled men's Excel. Yes.
		Yes.
		And you don't have to mess with tax, right? No.
		But let's go to, can we go to our, make sure we got everything, name, position, school, we don't need district. Do we have email?
		It's already collecting that as a default. I'm just going to mark. You can delete that row if you want. Well, I don't want to delete, I want to strike through. Just so you know. Yeah. Oh, you need that?
		So we've had in the past. It helps us because a lot of people like, oh, I'm not going to the wards. And so we end up paying a bunch more for that.
		Did people give you accurate answers or would it be best to look at historical head count?
		I could send another RSVP thing separately, I guess. We only have so many. I can send a separate thing out as we get closer too. Let's just read it.
		Yeah, I'd make that only people who registered get a quick thing. Hey, when it's like however far out you need to do your catering order, only send it to people who registered and do like a quick Google for us. RSVP for meals. Yeah. I'll do the same thing on here so you know that these are not on the strike page, but the shirt is. Because you probably need more heads up on the shirt.
		Yes, I need that right away. I'll end up guessing because people won't register until the day before.
		Yeah. Okay, so this is what it looks like. Email name phone number school shirt size with an example school position with an example How are you gonna pay?
		Can they really do those other payments like yes Amazon pay and Apple pay if they're doing it personally, but I doubt their school They're the most from we're gonna do a credit card doesn't matter which one they pick though. We get the money. Yeah, okay now What about an invoice there? What are they going to use for an invoice then to show their school or turn their office?
		They'll get an automatic one from stripe That's part of what you pay the fee is they don't have to bug you telling it's worth it So look we can edit this later, but let's just make it so you can see how this is different and
		Did I put the date on there? 2026 or anything? Maybe.
		You can take this link and put it on your website, send an email, text people. Where's that link going to be? It lives in Stripe because now we made a checkout page. So here's how this is different than a product. That's the product they get. Right. And we set the price. The checkout page, this, I'll show you, will load on your phone. It'll load on their browser.
		So we haven't done a checkout page yet?
		This is the preview of the one we just made.
		Oh, where did you go to do that?
		Well, it's just... I'm trying to keep track of... Now there's a payment link that takes them to this. So your web guide can put it on your website. It's active. This is what it's collecting.
		And that's my sample over there that we have.
		And then every time somebody looks at it or pays, you get...
		event like you can see people are on it people open it now where do I go maybe jump on ahead where do I go to see that completed forms like who has paid and of course their t-shirt their shirt size so I can
		How do I keep up on your payment links? This is the member conference 259. It's going to have everybody in this list. Just list it?
		Yes.
		So you click on it? So now I'll tell you, this is the way you test it. You make 100% off coupon for yourself and you send it to somebody and say, test it. Try this. Like I'll do it on my email so you know you're not logged in. And it'll do 100% off. But then you can see name, school, shirt size, when they paid. Whatever the price they paid, even though they're all going to pay full price. So then what you can do, let's go back to your payment links.
		You can take this one, you can duplicate it, and all we need to change for your non-member is the product that has the higher price. Everything else, the form, the name, the links are all set.
		And then we label it so we know what's what.
		Yeah.
		Let's go ahead and create. Let's duplicate it. Over here.
		Okay, but do you have that product? We already made that product for the non-member 460 whatever. I don't know. Let's just go back. Probably not. No, because we changed it. So this is your product catalog. This was November 2025. That's archived because it's just 250. Well, it's set as active, so let's archive it. So here's how I would do this. Let's go back to your catalog.
		You can't delete them, huh?
		Well, you don't want to delete them because you never know when you want to reference them. So this is what you have. Right. It's correct.
		So we want to duplicate. We need to do another product first, you said.
		Oh, that is our product catalog. Sure. We should be able to duplicate it here. I don't know why we can't just copy this one. See if I can make one.
		So that's going to be a non-member. Just you can go non-member. Did we need anything in the description? I was wondering about that conference feed for...
		It was 469. Oh, yeah. I wrote it down when I did the math. Give me a sec. 465. Because you will not...
		I just don't want to go backwards. Yeah. Have to upload an image or anything or is that already on there? I don't know. It's getting used by it a lot. Well, you can have an image on it. That's weird.
		I don't know why I can just duplicate it. Go to Send Logos.
		You can go to Wasp. Click on Wasp and go to Logos. And it's going to be that one, I think. That's what we did. The rest of them don't fit on there. Yeah. They all have weird aspect ratios. I want to get that boot change on that, too. But it's another time, I guess. I'll have Jacob work on that.
		Okay, now we have a product. We can go back and take... This is your checkout link to get the member one. I'm going to duplicate that, but we're going to rename it instead of copy. We're going to change this to non-member. There's your logo. We're going to do \$465, remember. Actually, I wonder if we change the product or we change...
		That says pricing \$259.
		I think we just want to do a different one. Knowing that it sets it that way. So then we're going to go. Like the naming we did on the other one.
		I got to put in all those things. Oh no, it doesn't copy that.
		So look, it already has. Yep. Principal, shirt size. The difference is the price. Oh, I know why. You do the product here. Let me just show you. That's what, I knew there was an easier way. Update product. I know, I'm just gonna get rid of this one. And now we don't have to redo the form, it'll collect all the same stuff, but charge them this. This will just have a different link now. To check it, here's the other checkout page, right?
		The only thing that should be different on this link that you're going to maybe email some guys that aren't members, all the same info, but they paid \$465. Instead of trying to say who's a member and who's not, it's just not worth it.
		What I thought I'd do is send them two links. Here's a link to join. And how much you'll save.
		For \$410. How much you'll save. For \$410 to get memberships. Okay, can I tell you that Stripe is built for this? It's called a cross-sell. Buy a membership from this email, immediately gives them the membership price for the conference on the next screen.
		Yeah, except that payment will come to me, which I guess would be okay.
		Can you take payments for the membership dues?
		I can't.
		I don't want to, but I can. The other thing you can do is you can make a coupon code. For the very few that I may get. You could give somebody something like... Well... Let's just get it working first. Then we can polish it later.
		I don't even know how many people we're going to do. Yeah. Because I want to send this out to my people soon. But not to the non-target. I'm going to target the others in August. Like week one. Did we update our prices on that too? Yeah.
		And I know this is messing up your formatting, but we don't care about that now. I'm just going to give you where these links live.
		Did you update on there?
		Yes. 259 and 465.
		Okay, and now we need to do another one for, let me get that down for the associate and aspiring. For 155? Yeah, we may actually get a couple of those. Okay, so... The most efficient way. Did we go 155? Yeah. And keep that way and just say, yeah, okay.
		Because 155, you'll break even plus 20 cents. Let's go back and make sure we have two. Good. Non-member, member. Now let's duplicate. Let's just give them, we don't even need a different product. That was dumb of me to do. Let's duplicate. Okay. And rename. What's the short name instead of non-member? Is like aspiring school leader or like?
		- I don't even know what the difference between an associate and aspiring is.
		- And then the other question is, do you have a list of those people? How are you gonna send that link? Members get one, you headhunt some non-members, How do you find these people?
		Well, like the people that are doing the, number one, there's five people that I would send them to that are getting our, they're in our grant program where we're paying for their tuition.
		So just call them aspiring leaders. Yeah, aspiring.
		Can we just go, I don't even know what the definition of associate is because I think they have it at the NASSP level. Can I check one thing?
		Yeah, let me just name this. One off, 155, we're naming it. And then we're gonna make this the default price. Good. A new checkout link for them and everything looks the same except the price is \$1.55. Nope. Exchange didn't save. I have that set to default. What the hell?
		You archived this one. Did you want to archive it? I wanted that one. This is inspiring.
		Non-members, we only want to have the \$465. Aspiring leaders, we only want to have \$155. So it's default. I don't know why that didn't show. So let's go back to our payment links.
		There.
		- Down there too.
		- Price is on there. - It was 465. We don't want that. - Right. - We want 155. - And then you're allowing them to-- - That's their own currency. It's like non-US dollars.
		And they can do more than one here too? Same thing?
		Yes, up to 20 I think. Now why is this, let's say 465? Because we copied the other one. Okay.
		Oh, it still says 465. Get active. No, that's the one I already did.
		Let's go back to your catalog. This is why it's being pain in the ass. Aspiring leader, 155. We got to do it within this. Let's delete the wrong price. - So we go to payment links. - Create payment link. - Let's duplicate one so we don't have to start over.
		Copy.
		I don't care why that's doing that.
		One off flat rate 155 Hmm, it's just that stupid name. I thought I already did one with an S. There it is. 155, school, shirt. That's all good. link Test the link.
		There's no way I could have done this on my own. Well, this is like the simple part of Stripe.
		I know it sounds dumb, but I'm telling you, when you connect it to your AI tool and just say what you want, it can do all this for you, name all the things. We'll get to that level, but I know you're the kind of guy that wants to see how it works.
		Yeah, because I want to be able to do this myself. I don't have to bug you every time I want to do one.
		So I'm going to put that link here. So all three links are here. They're all confirmed working. That was the hard part. Now.
		We have three different links. Yes. We have member, non-member, aspiring.
		Yes. I can't delete this one, so I just renamed it deprecated, like out of order, so it doesn't confuse you. These are your three. So we got three that are active. They're all working.
		Okay. So. Let's say I'm ready to send an email to all my non-members, which is going to be soon. All my members. It's going to be soon about the conference. I want to send them this Stripe link so they have an invoice and see what it costs and see what their choice is. Now, here's a question. If they're going to send me a check, I don't even put that on Stripe. I have to put that in an email.
		If you prefer to pay, here's how you mail me. And my address.
		They're going to need this. Like a form? Well, they're going to need... What do they need to tell you? They're going to need this right here. Hit pay by check or PO. Make payable to WASP and send to. Yeah. And then I want to have a... I'm supposed to get a link from... The REM code, I would think just go to and make the reservation or not to make a phone call because it's such a pain in the ass to make a phone call to the REM code and nobody picks it up.
		But I'll get that. Here's what we'll have to do. Let's make a good looking little thing they can print out because you're going to also need their t-shirt size and their school. So if they're going to do a check, how are you going to collect that data that the strike form is getting from credit card payees? See what I'm saying? So say I'm a Cheyenne Central assistant principal and I want to pay by check.
		How do you know my t-shirt size? If I mail you a check, you're going to have to give them a little thing to print out. Well, that's what this thing is. We'll make a really streamlined version for just the checks. Like circle t-shirt, you know.
		Check off this stuff. So we don't really need this at all. We'll adjust it to just pay for check people.
		Which will be a small group, so don't spend a lot of time on something that 10 people are going to use.
		We'll just use the same thing and just modify it.
		And we'll make it black and white so it's easy to print out.
		But, so with the email, what I want to send to my members is... I want to send them... The bios of the speakers so they can preview. I'm going to have it on my website. So conference 2026. It has the keynote, two different keynotes.
		And just to clarify, you don't have it yet on your website? No. Okay. But you have all the info except for the speaker? Gogan's going to put it on waiting for one more guy. Okay. Do you want that to be the follow-up when they pay on Stripe? They're going to get a screen that says, Success! Payment Collected. You can put stuff in that success page.
		No, I want that link to take him to the payment page is going to be one thing in an email. Yes. The other thing in the email is going to be the conference kind of schedule.
		Check it out.
		Yeah, yeah. Here, look at who our keynoters are, our presenters, our YML leaders.
		So you're not going to be able to send that email until he has that page down. Right. Because people are going to want to look before they pay. Yeah, I'm creating that though.
		No, no, no.
		Make it the same page that has your speakers. Just put the little thing, put the headliners at the top, and then do your schedule, your date, location, whatever. Make it one page that has all your conference. You mean this thing? Is that what you're talking about? No. So in your email, there's a checkout on Stripe if you're a member. And there's a learn more about the conference link. Correct? You're saying like, here's the...
		Headliners.
		Can I put all that in there that I want and learn more? Yeah. Okay. Yeah, link to the pictures, the bios of the speakers is what I want.
		Because they're going to look at that to say, is it worth \$250? Yeah, that's what I'm trying to do. It's like, here's who we have. So have Grogan make that webpage. Put that as your link you're talking and just tell them, I want my headliners. Here's your info. I got them on these Google Docs from these guys. Yeah. Put a little thing across the top. It's called above the fold, like the first screen they see.
		And then below, you can tell them what you want. Location, Ramcota, date, November 1st through 3rd, contact info, Jeff McKelkey.
		Well, I'm kind of confused on where I'm sending them then.
		So you're sending an email. There's a click here to go to Stripe and pay the \$2.65. Yeah. You want to also tease what's at the conference? Make that your web page that just has all your conference info. Is there anything on your website about 2026 conference?
		I can get him to do that first. So then the link would take him straight to the web page?
		And you go, here to pay, here to read more about the conference. Those are the only two links in the email. So I do a little introduction and then two links. We're excited. The conference is ready. Here's where you can read more.
		And I should put a blurb in there too. If you're not going to pay with a credit card, here's my address.
		We're going to attach a thing that can print out to the email. Like a Google Doc can say, if you want to Pay by check to save the 15 bucks or whatever, or your school doesn't have a credit card. Print this out, instructions are on it. Kind of like when you do a return label. Print it and it has instructions, address, everything. And I can give your web guide.
		So what I need on the email is... One is an introduction about the conference. Yeah. Excited about blah, blah, blah.
		That's called the copy, like the writing. You're going to need it. The most important thing is the subject line. That's what gets people to open it. Which you don't have to do these.
		It's just going to be Educational Leadership Conference 2026.
		No one's opening that shit, Jeff. I'm a marketer. Let me help you. They don't know what that is until they open it.
		Okay, what's the second thing?
		You have link, intro, that's called the copy. Now you need links. Let's make a list. Links for? Now the first thing, Stripe checkout for members. So for example, that would be, if I get this email from you, we're going to make it pretty, but it's the same link underneath. I'm Bob and I'm a member and I'm ready to pay I click it.
		Oh Look strike page 259 pull out my credit card and then we're gonna do it for non-members No, cuz you're not emailing us to non-members. Oh, let's use them and we're not the Elon to aspiring leaders We'll do a separate thing.
		Okay, but you want to read more about the conference?
		Okay. So the second link is gonna be website link and
		conference info bios well that sure whatever you want you can prioritize whatever you want yeah okay third thing is attachment attachment print this to pay by check and it'll have info for their shirt their school all the info you need and then the address to send because we're not even going into straight yeah because you got to reconcile their data
		So it's going to include their shirt size, their name, their school, everything that we have on Stripe. Name, school, and shirt size. Email. Okay. Is that it? Intro. Two different links. One to Stripe. One to the website. An attachment for those people paying by check.
		Yep.
		Is that it?
		So the bottleneck right now, like what you're waiting on is the web link because you can't send this.
		Yeah, I need a piece of information and then I'm sending it to Jacob saying, Jacob, OK. And so we'll just take a quick look because this conference 2026 is still up there. So here's conferences. So the link, we can get a link right to this.
		And you can say use this.
		Okay, redo this, Jacob. And here, I'm going to send him the new bios. Yeah. He's only got two on there, or three.
		From last year. Yeah, from last year. Interesting little animation on there.
		Okay. So. Is that it then, an email? Yep. Check with Aaron about a catchy...
		Subject line is what you should put most of your brain power into because no one reads the rest if they don't open it.
		What else you can say besides educational leadership conference is what it is. It's what it is. What else do you want to call it? I mean, he called it rendezvous, something like that.
		I don't care what you call the conference. The subject line doesn't have to be just the name of the conference. You can say, I'm just going to throw out examples. Leadership. Something about leadership. Calling all school leaders. Telephone emoji. You can put some little, I don't know how to do. This is, it gets me every time. Anything that has this gets people to open it. It's just, I know it's cheesy, but it's like a psychology trick.
		They don't think it's like an infected email?
		No, I'll show you. So here's how you do the test. This is what people can read. That's called the subject line. So like the New York Times spends a lot of time and money figuring out how to get you to open this because they lead with Lindsey Graham's likely cause of death revealed. Oh shit, I got to read more. Now, embedded image, headline, this is the copy. Well, if they just said Lindsey Graham dead,
		That's a different open rate. In other words, fewer people would probably grab it. I want to know his cause of death. They put that in the subject line. They hooked me to open it. Opening it is called a click-through rate. It's like what percent of people that got the email actually click on it. And then a percent of those actually pay. So the top, the bigger chunk you get, 5% of them are going to pay.
		Okay, we want to capture everybody to open because every 20 people that open, one's going to pay. Like this is, you can tell this is a dipshit who doesn't know what they're doing. WDE media release. WDE, okay. They could have just said WDE seeks public comment on this because they repeated WDE twice, but they're a government agency and don't know this stuff. The other thing is, don't you want people to know that WASP is hosting or...
		Because they're WASP members. That's why they're getting this email, right? Don't more of them know what WASP is than Educational Leadership Conference 2026? Anybody could have a conference called that. So something like...
		But I got to be careful because there's four groups that put it on. It's not just WASP. It's the Elementary Association, It's to spend people.
		Change the subject line for each group to be specific. Calling all elementary.
		Well, that's what they do. I don't, I'm not.
		You don't email them?
		I don't, no. They're doing their own thing. I just target my people.
		So they all know what WASP is if they're getting this email from you.
		Yeah.
		So I put WASP in the subject line. Like WASP's 2026 School Leadership Conference. Now, open it. Talk about the official name, but this just sounds generic, and they don't know it's you, your organization, you're a member. Another one is something like save your spot. Now, I don't know if this is true, but is there a cap on how many registrations you could possibly take? Never reached it. Well, welcome to marketing.
		You can say there isn't. Say something like save your spot or... Register now or reserve. Even though, I mean, they're kind of reserved. In the strategic line, you mean? Yeah. Reserve your spot at WASP's leadership conference. Yeah, sure. Something like that. You can...
		So my plan of attack now, thank you for doing that. I couldn't have done that on strike. There's no way. Yeah. My plan of attack or to do is one, I need to finish the bio once I get the last bio. Send it to Jacob. All the ones I've collected Send all to Jacob and have him redo the webpage. Redo conference. and then once that's done, once I have that, I just copy that link, I open up that web page link, copy that link, and click it.
		Now, how do I go to, show me how I go to Stripe and copy...
		What do you want to copy? These checkout page links?
		But only one, I only need one because I'm just targeting...
		Go back to your doc, just to make your life easy... I put them in your Docs Scroll-Up. Oh. They're all right under the one you said.
		So I just got to activate them.
		Yeah. And in your email, hide the link. Don't say buy.stripe.com. The text that shows is something like membership reservation form or pay here, and it opens to that link. I can help you with the formatting. Exactly.
		Okay, so now what you're saying is the link in the email won't show this. Yeah. How do I do that?
		I'll show you. Okay. So say I'm going to email you that link. I'm just going to find some link on here. See how this is a big, long, ugly link in my email? If I highlight it, hit the link button down here. Yeah. and hit change. The first line is Jeff will click this, but it still goes to that link. Right, that's just the text. So now, I don't know why that's black. They only see that in the email, but watch when I click.
		It still goes out to the URL I gave them. That's just a little trick because people are like, what the hell is buy.stripe.com? It should be Wasp.
		Let me see if I can do that right. Just do it once and remember I can do it.
		Yeah, but don't do it here. You can copy, but keep the full URL here. And take that, hit Control-C and go to your email. Yeah, I know. Copy.
		Yeah. And I'm going to go to my email. Yeah. email it to me. And then I want to highlight it and then I'm going to go to the link and it's going to go change and I'm going to say whatever I want. I would say something like Wasp registration link or something. Perfect.
		Okay So what am I forgetting? You need the web page that's your bottleneck and you need a simple printout that you can attach for the few people paying by check.
		Oh Yeah We got to create that And oh yeah, cuz that's gonna be an attachment So I got create the attachment Let's do that right now really quick. Can we do that real quick?
		Can I show you how I would do it? Yeah. You know how this form already has everything we need, but we don't want to mess with it? Yeah. Let's duplicate it and call it check stub. So we don't mess with the other one, but we're not starting blank. And that's a Google Doc. Yeah, so let's just make this really simple. You still can have them do that if you want. That's confusing.
		Oh, yeah.
		That's a different form. I think we should take it off the paste of the Czech people's too. Yeah. Keep it the same.
		That would be confusing.
		Just hit delete? No, we captured their shirt on the other ones.
		Oh, that's right.
		I'm just, I'm condensing it.
		You're going to get rid of district, right? I sure can. Just give me your row. There you go. Position, scroll, email, that's it. We didn't do phone number.
		Okay, now they're not going to need anything but the check. Yes. need any of this because they're not getting this if they're a non-member. And then we're going to say-- If paying by check. Yeah.
		Wham. Because this, the stripe doesn't have that either, does it? We can put that on there.
		What, the lodging? The lodging thing. You can have a follow-up thing that goes to everybody who paid. So you can always get, hey, quick Google form for your meal reservations. Hey, reminding you to book your rooms because you already got your conference. Okay, conference, registration, date, Ramcoda, name, position, school, email. Do you want their cell phone on this? Because you got it on the Stripe thing.
		Do we have a phone number?
		This is for people.
		I know. Do we have a phone number on the Stripe checkup?
		It's a default field you wanted to keep.
		I've got their phone numbers, basically. I guess. Yeah. Okay, you don't have to. Let's do above that, add one row above. I can switch it. That's fine.
		that because they're not printing something out to pay with the link. Do I want to Put a link on this form to the website. It's in the email. No one's going to print this out and need a link. Oh, yeah, yeah, yeah. Plus it's not ready.
		This is the attachment, yeah.
		This is done.
		Do we want to keep this on the bottom? Probably, no? I think it doesn't hurt. Okay. Do we want conference pricing? Does that look stupid or is that okay? No. Okay.
		Would you change anything else about this farm? No. I wouldn't waste time because only a handful of people are going to use it.
		I'd be surprised. So, so far, I mean, through last year, nobody used Stripe for this.
		But you didn't fucking know how to do it.
		Well, I wasn't setting it up. He didn't. He had Stripe set up. Did he send it? But he didn't want to keep losing money, so he... Look at all those checks. I don't want to mess with that. He lost his time. Yeah. I know. I don't want to mess with that. Imagine doing 300 of these by paper. No. Is there going to be enough? Because I'm still going to have to go by hand and check everything. Shirt sizes, meals.
		But I'll show you a system to rectify all the striped ones and all the paper ones into a Google Sheet just by taking a picture. You don't even have to enter it yourself. Okay, so they're going to send me this with the check.
		And that's only people printing this out from your email? Yeah, do I need to put something in here about send? Like, just for... Yes, they know they got to send us with the check right now. I would know that as one paying by check make it payable to wasp mail here Mail this form Maybe should say that mail this form. Yeah, I think So just put yeah right there This form to Okay. So where, this is different than my other thing, so, but you opened it up in the conference, where is this?
		Exactly where the other one was.
		It is, I don't have to move it. And it's shared with the same people. And I'm the creator? Yeah. Okay. Anyone at the link? Yep. Okay. All right. I'm good. What was the other thing? We can talk about the other thing later. I'm trying to think what the other thing was. Oh, what do you recommend? I got to put together, I haven't even started yet, but I got to put together a presentation that I'm giving at TeacherCon on the topic for principals.
		This is just for principals. For leadership teams. What I just been using Google slides. Is that okay? Do you recommend anything else?
		Here's what you know. I don't even know Google slides very good. You don't have a paid Canva, do you?
		No. I did a Gemini thing. I think I did a Gemini. Gemini works with slides. Fine. Just do slides.
		Unless you want to wow them with technology.
		No, I don't want to do that. I really want more discussion anyway. Not a sit and get thing, like look at the slide, look at the slide. It's just talking points to keep us, to lead the discussion. It's probably going to be a small group, right? A small group. How many went, didn't you do a thing at TeacherCon last year? Yeah, after the last three years. Not at TeacherCon, it was separate. Oh yeah, it's like the sister thing.
		Okay, do I need to check out of this or anything then? It's all saved in your doc.
		Okay, and it's all set up. Yeah, later we'll talk about how to go in there and see, get the report after people start paying. So can I show you how I would do that so you don't waste any money?
		These guys need to eat. They're hungry. Let's make a coupon. So you don't have to waste your money. Oh, this is a test run? Stripe test run. 100. 100% off, because it's 100% off.
		Okay, we're done, dear.
		Make a promo code. Let's call it Jeff Internal Testing. Now, anybody who had that code would be able to check out for 100% off. Now, I wonder if we have to tell your product page to let them use a code.
		Why are we doing this just as a test page?
		Because you want to see where the data goes. That's what you said. You want to, like, where's their shirt size and all that.
		Yeah, like, I can just do mine.
		Yeah, but you don't want to pay \$250.
		No, no. I mean, we could just fill it out like it's actual.
		I just want to see...
		Oh, we're not. We're done. Oh, okay.
		Yeah. You might have to go to your product catalog and say that people can use... Fun. It's a non-member. It's not a member.
		Jelly's over here, Macy. I'm going to put it-- you're doing it.
		Oh, it's down here, I think.
		There we go, \$2.58.
		I wonder if there's something we have to say to enable a coupon.
		You can get your jelly's on.
		I thought it just applied to anything, but I don't see a spot on this page to enter.
		Oh, on the checkout? You have to go to the checkout maybe?
		Oh, I'm on the checkout and I don't see anything. We can mess with it later. But there's a way to use that. You don't even have to put in a credit card because it collects zero dollars.
		Okay. I'm going to sign out.
	</transcript>
</meeting-notes>

