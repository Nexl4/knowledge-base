
If you’ve ever seen the message _“Your local data is out of sync with the data on the Tuta servers. You will be logged out and your locally stored data will be cleared and re-downloaded as needed,”_ it can feel a bit alarming at first.

It usually shows up unexpectedly, sometimes after a short service interruption, sometimes after switching networks or devices. And yes, it can be frustrating.

But this behavior is not a bug. It’s a deliberate design decision.

## What actually happens

When this message appears, the system has detected a mismatch between:

- your **local data** (stored in your browser or app), and
- the **server data**

In systems like Tuta, which rely on end-to-end encryption, data consistency is critical. The client and the server must stay in sync.

If that consistency is broken, the safest option is:

1. Log you out
2. Clear the local state
3. Re-download the data from the server

## Why this happens

There are a few common reasons why this sync issue occurs:

- Temporary server interruptions
- Network instability
- Multiple devices
- Client updates

## Why logging out is actually a good thing

At first glance, being logged out feels like a disruption. But from a system design perspective, it’s the safer choice.

Here’s why:

- Data integrity comes first – The system avoids the risk of working with corrupted or partially synced data
- No silent failures – Instead of guessing what’s correct, the system forces a clean state
- Predictable recovery – Re-downloading ensures that everything is consistent again
- Security benefits – It reduces the risk of lingering sensitive data in a potentially unstable state

## What you should do when you see this

In most cases, **no action is required**.

You can simply:

- Log in again
- Let the app re-sync your data
- Continue using the service as usual

If the issue persists:

- Try restarting the app or browser
- Check your internet connection
- Try another device or browser

## When it’s not your fault

This error often appears during or after:

- short service interruptions
- backend maintenance or updates
- temporary sync issues affecting multiple users

In many cases, it’s not related to anything you did.

## A small but important UX trade-off

This design choice highlights a key principle in systems like Tuta:

> It’s better to interrupt the user than to risk data inconsistency.

From a user perspective, this means occasional interruptions.

From a system perspective, it ensures:

- strong data consistency
- reliable encryption integrity
- predictable recovery
