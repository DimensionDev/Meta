# Article 2: UX Prototype Artboard Naming Convention

Key | Value
--- | ---
Type | Convention
Date | 2019-11-11
Status | Ratified
Authors | Neruthes
Amendments | N/A

# Abstract

We need a consistent storyboard coding guide to make storyboards readable again.

# Basic Structure

## Starting Point

Every storyboard with `Starting Point` property shall be coded `S`.

## Fork

For example, if `S` has 2 options which will lead to 2 different paths, the two succeeding storyboards shall be coded `S.a1` and `S.b1`, respectively.

We use lowercase letters to represent forking to different paths.

## Continuation

For example, if `S.a1` has 2 more steps to give forking options again, the three succeeding story boards shall be coded `S.a2` and `S.a3`, respectably.

We use decimal integers to represent steps.

## Error Handling

For example, if `S.a1` has 2 error cases, they shall be coded `S.a1.Ea1` and `S.a1.Eb1` respectively.

## Combining Them

For example, `S.b1.a3.Ea3.b1` means:

- Select the 2nd option on Starting Point.
- Select the 1st option.
- Move 2 more steps forward.
- Fall into the 1st error.
- Move 2 more steps forward.
- Select the 2nd option.

We join the array with `.`.

# Simplification

## Omitting Step Indicator

For example, if `S.a1` immediately gives 2 options, the two succeeding storyboards shall be coded `S.a1.a1` and `S.a1.b1`, respectively. In this case, since no storyboard will be coded `S.a2`, we may write `S.a1` as `S.a` to simplify the code.
