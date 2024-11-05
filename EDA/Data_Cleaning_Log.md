# Manual Data Cleaning

## Changes on Transmission_Lines.csv

- Deleted entry `222,Aminbazar 400/132kV transformer connecting 132kV line,132,1.0,Single,,,0.413`. Reason: Inconsistant formatting.
- `SS` after the node name was removed. For example `Daudkandi ss` was replaced with `Daudkandi`
- The name `Barisal` was replaced with `Barishal`.
- The name `Bogra` was replaced with `Bogura`. `Bogura 230kV` was replaced with `Bogura`.
- `Bheramara` was misspelled as `Bheramana`. `Bheramara 230` (SN 32) was replaced with `Bheramara`.
- `Comilla(N)` and `Comilla North` was replaced with `Comilla (N)`. `Comilla(S)` was replaced with `Comilla (S)`.
- `Khula` was replaced with `Khulna`.
- `Shiddhirganj` was replaced with `Siddhirganj`.
- `Basundhara` was replaced with `Bashundhara`.
- `Ishwardi` was replaced with `Ishurdi`.
- `Jessore` was replaced with `Jashore`.

## Prompt for data cleaning:

```
I have extracted a list of substation names from a data source, but I'm seeing more entries than expected. This suggests that some station names may have been misspelled, causing duplicates or near-duplicates in the list.

Your task is to identify similar or potentially duplicate names in the list, so I can recheck and consolidate them as needed.

---

Substation Names:

{Substation_names}
```

## LLM Response:

1. Aminbazar variations:

   - Aminbazar
   - Aminbazar River Crossing
   - Aminbazar at Keraniganj
   - Aminbazar(With River)

2. Barishal/Barisal variations:

   - Barishal
   - Barishal (N)
   - Barishal(N)

3. Bheramara variations:

   - Bheramana
   - Bheramara
   - Bheramara 230

4. Bogra/Bogura variations:

   - Bogra
   - BograNew
   - BograOld
   - Bogura 230kV
   - Bogura(West)

5. Comilla variations:

   - Comilla (N)
   - Comilla (S)
   - Comilla North
   - Comilla(N)
   - Comilla(S)

6. Confidence Power Plant:

   - Confedence PP
   - Confidence PP

7. Daudkandi variations:

   - Daudkandi
   - Daudkandi PP
   - Daudkandi ss

8. Gopalganj variations:

   - Gopalganj
   - Gopalganj PP
   - Gopalganj ss
   - Gopalganj(N)

9. Khulna variations:

   - Khula 330MW
   - Khula(S)
   - Khulna
   - Khulna (C)
   - Khulna (S)
   - Khulna(S)

10. Madunaghat variations:

    - Madunaghat
    - Madunaghat 400kV
    - Madunaght(O)

11. Siddhirganj/Shiddhirganj variations:

    - Shiddhirganj
    - Siddhirganj
    - Siddhirganj 210 MW P/S
    - Siddhirganj Dutch Bangla PP
    - Siddhirganj ss

12. Basundhara/Bashundhara:

    - Bashundhara
    - Basundhara

13. Ishurdi/Ishwardi:

    - Ishurdi
    - Ishwardi

14. Jessore/Jashore:

    - Jashore
    - Jessore

15. Noapara variations:
    - Noapara
    - Noapara PP
    - Noapara Ss

# Similar Names That May Need Verification

1. DU / Dhaka University

2. Maniknagar / Manaknagar

3. Meghnaghat variations:

   - Meghnaghat
   - Meghnaghat at Shyampur
   - Megnaghat Rental PP

4. Old Airport entries:

   - Old Airport
   - Old Airport (O/H)
   - Old Airport (U/G)

5. Sirajganj variations:
   - Sirajganj
   - Sirajganj at Sreepur
   - Sirangj 68MW Solar

# Special Cases to Check

1. Multiple LILO entries that may refer to the same location but with different connection points

2. Entries with location indicators that might be the same substation:

   - Bangladesh Border
   - Bangladesh Border (Baharampur)
   - Bangladesh Border (Baharampur) 2nd

3. Entries with different formatting conventions:
   - Some use parentheses: (N), (S)
   - Some use spaces and parentheses: (N)
   - Some use no spaces: (N)
