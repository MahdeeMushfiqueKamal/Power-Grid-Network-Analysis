# Manual Data Cleaning

## Changes on Transmission_Lines.csv

- Deleted entry `222,Aminbazar 400/132kV transformer connecting 132kV line,132,1.0,Single,,,0.413`. Reason: Inconsistant formatting.
- Deleted entry `38,Madunaghat,Khulshi,132,13.0,Single,Grosbeak,636 MCM,13.0`. Reason: Duplicate entry.
- Deleted entry `15,Gopalganj,Aminbazar River Crossing,400,7.50,Double,Quad ACCC Finch,1113 MCM,15.00`. Reason: The data is already present in the `Gopalganj,Aminbazar(With River)` entry. Later replaced `Aminbazar(With River)` with `Aminbazar`.
- Deleted Entry `188,LILO of Khulshi - Halishahar,Rampur,132,2.775,Four,XLPE,800 sq.mm,5.55`. Reason: Same entry exists at 219.
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
- `Barapukuria at Bogura(West)` was replaced with `Barapukuria`.
- `Aminbazar at Keraniganj` was replaced with `Aminbazar`.
- `Old Airport (O/H)` and `Old Airport (U/G)` was replaced with `Old Airport`.
- `Khulna (S) at Jhenaidah` was replaced with `Jhenaidah` as the distance from `LILO of Bheramara` were only 1.97 KM.
- `Khulshi (Circuit-2)` was replaced with `Khulshi`.
- `Kaliakoir at Kodda PP` was replaced with `Kaliakoir`.
- `Meghnaghat at Shyampur` was replaced with `Meghnaghat`.

# Appendix

## Prompt for data cleaning:

```
I have extracted a list of substation names from a data source, but I'm seeing more entries than expected. This suggests that some station names may have been misspelled, causing duplicates or near-duplicates in the list.

Your task is to identify similar or potentially duplicate names in the list, so I can recheck and consolidate them as needed.

---

Substation Names:

{Substation_names}
```
