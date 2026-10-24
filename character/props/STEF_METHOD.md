# STEF finger tattoo method (binding)

Applies to every future image where the fingers of the right hand are visible.

## Why
AI image models do not render "STEF" correctly: wrong letter order, letters not rotated, doubled letters. So the letters are never left to the model.

## Workflow
1. Have the model remove the finger tattoos ("plain fingers").
2. Insert the real ink letters from `character/props/tattoo_STEF_reference.png` locally in Python.

## Placement rules
- Order: **S** little finger, **T** ring finger, **E** middle finger, **F** index finger.
- Rotate each letter along the axis of ITS own finger, top of the letter towards the knuckle.
- Centre each letter on the first finger segment, between the knuckle and the first joint crease (not on the knuckle).
- Size: about 55-60% of the finger width across.
- The letters follow the slanted knuckle line.

## Check
Rotate the hand so the fingers point down. STEF must then read exactly like the reference.

## Tip
Best results: have the user sketch the letter positions in red, then place the letters precisely on those marks.

## Approved example
`content/reels/001_studio/shot6_final_v7.png`
