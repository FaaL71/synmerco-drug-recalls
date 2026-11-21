# US drug recalls reported 1 August to 31 December 2026: class, cause and firm, three pulls

## Executive summary

Three timed pulls of the openFDA drug enforcement endpoint (search `report_date:[20260801 TO 20261231]`, limit 100, paged by skip 0/100/200/300) were made 19, 20 and 21 November 2026, each returning the same raw total of 302 recalls and an identical 302-row CSV (SHA-256 `f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c` for all three pulls), so the underlying data did not change at all between pulls: no recall was added, removed, or changed in status, classification or reason for recall. Of the 302 recalls in the last good pull (PULL 3), 263 are Class II, 19 are Class I, 18 are Class III and 2 are Not Yet Classified; the leading cause groups are other (114), manufacturing practice (71), sterility (58) and contamination (30), with potency (22) and labeling (7) behind; reports cluster in November (91), September (83), October (75) and August (53); 41 firms have two or more recalls, led by Victory Medical Center Pharmacy with 43, and all 302 recalls are still Ongoing. The 19 Class I recalls are dominated by particulate matter in injectable products, plus two sterile-compounding microbial contamination cases, one unapproved-drug case and one superpotent thyroid tablet case.

## Answers

1. Each pull's PROOF quotes the raw results total, and that pull's CSV holds one row per recall returned: PULL 1 raw total 302 with a 302-row CSV; PULL 2 raw total 302 with a 302-row CSV; PULL 3 raw total 302 with a 302-row CSV — see excerpt 1 (PULL 1 raw totals), excerpt 2 (PULL 2) and excerpt 3 (PULL 3) in PROOF, and the CSV SHA-256 `f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c` quoted in each PULL note.

2. The three CSV files are attached with exactly the listed columns: `drug-recalls-pull1.csv`, `drug-recalls-pull2.csv` and `drug-recalls-pull3.csv` all carry the header `recall_number,recalling_firm,state,classification,status,report_date,recall_initiation_date,cause group,reason_for_recall`, one row per recall returned, sorted by report_date then recall_number — see excerpt 4 (CSV headers) in PROOF.

3. The cause groups follow the stated rule, and the tables, repeat firms and Class I list agree with the CSV they use: cause groups were assigned in order — sterility (`steril`), manufacturing practice (`cgmp` or `good manufacturing`), contamination (`contaminat` or `impurit`), potency (`potency`, `subpotent` or `superpotent`), labeling (`label`), else other — as case-insensitive substrings of the full `reason_for_recall`; the classification table sums to 302 (263 + 19 + 18 + 2), the cause-group table sums to 302 (114 + 71 + 58 + 30 + 22 + 7), the month table sums to 302 (53 + 83 + 75 + 91), the 41 repeat firms and the 19 Class I recalls are counted directly from `drug-recalls-pull3.csv` — see excerpt 5 (Class I raw lines) in PROOF.

4. The PLATFORM RECORD shows a PULL 1: note and each later PULL note at least its wait after the one before, each with its CSV's row count and SHA-256; each good pull's source time is later than the previous good pull's; the change counts agree with the CSV files: PULL 1 note recorded 2026-11-19 00:01:51Z (302 rows, SHA-256 `f47a44d6…90c`); PULL 2 note recorded 2026-11-20 00:17:34Z, 24h 15m 43s after the PULL 1 note (302 rows, same SHA-256); PULL 3 note recorded 2026-11-21 00:46:48Z, 24h 29m 14s after the PULL 2 note (302 rows, same SHA-256); source times increase — Thu, 19 Nov 2026 00:01:25 GMT, then Fri, 20 Nov 2026 00:16:36 GMT, then Sat, 21 Nov 2026 00:46:24 GMT; both Changes sections report no change with row counts 302 and 302, matching the identical CSVs — see excerpt 6 (progress-note record) in PROOF.

## Raw totals per pull

| Pull | Raw total (meta.results.total) | CSV rows | CSV SHA-256 | Source time (first response Date header) |
|------|-------------------------------|----------|---------------------------------------------|------------------------------------------|
| PULL 1 | 302 | 302 | f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c | Thu, 19 Nov 2026 00:01:25 GMT |
| PULL 2 | 302 | 302 | f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c | Fri, 20 Nov 2026 00:16:36 GMT |
| PULL 3 | 302 | 302 | f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c | Sat, 21 Nov 2026 00:46:24 GMT |

## Recalls per classification (last good pull: PULL 3, 302 rows)

| Classification | Recalls |
|---------------|---------|
| Class I | 19 |
| Class II | 263 |
| Class III | 18 |
| Not Yet Classified | 2 |
| **Total** | **302** |

## Recalls per cause group (last good pull: PULL 3)

Cause group rule, in order, as case-insensitive substrings of the full `reason_for_recall`: sterility (`steril`), manufacturing practice (`cgmp` or `good manufacturing`), contamination (`contaminat` or `impurit`), potency (`potency`, `subpotent` or `superpotent`), labeling (`label`), else other.

| Cause group | Recalls |
|-------------|---------|
| other | 114 |
| manufacturing practice | 71 |
| sterility | 58 |
| contamination | 30 |
| potency | 22 |
| labeling | 7 |
| **Total** | **302** |

## Recalls per report_date month (last good pull: PULL 3)

| Month (report_date) | Recalls |
|---------------------|---------|
| 2026-08 | 53 |
| 2026-09 | 83 |
| 2026-10 | 75 |
| 2026-11 | 91 |
| **Total** | **302** |

## Firms with two or more recalls (last good pull: PULL 3)

| Recalling firm (exact string as returned) | Recalls |
|-------------------------------------------|---------|
| Victory Medical Center Pharmacy | 43 |
| Baxter Healthcare Corporation | 20 |
| ABC Compounding Co., Inc. | 19 |
| PRITAM INTERNATIONAL PRIVATE LIMITED | 17 |
| Carolina Infusion, LLC | 16 |
| American Regent, Inc. | 13 |
| ACCORD HEALTHCARE, INC. | 12 |
| Apollo Care, LLC | 11 |
| Sterling Pharmaceutical Services LLC | 9 |
| K.C. Pharmaceuticals, Inc. | 8 |
| Safecor Health, LLC | 7 |
| Fresenius Medical Care Renal Therapies Group, LLC | 5 |
| Shoolin Pharma Chem LLP | 5 |
| Allies Group Inc. | 4 |
| Ascend Laboratories, LLC | 4 |
| Hikma Pharmaceuticals USA INC. | 4 |
| SUN PHARMACEUTICAL INDUSTRIES INC | 4 |
| American Health Packaging | 3 |
| BioMed Laboratories, LLC. | 3 |
| Mylan Pharmaceuticals Inc | 3 |
| Par Health USA, LLC | 3 |
| Pfizer | 3 |
| Ajanta Pharma USA Inc | 2 |
| Apotex Corp. | 2 |
| Apothecary Pharma LLC | 2 |
| B BRAUN MEDICAL INC | 2 |
| Brandywine Pharmaceuticals, LLC | 2 |
| Eagle Pharma Outsourcing LLC | 2 |
| Fresenius Kabi USA, LLC | 2 |
| Glenmark Pharmaceuticals Inc., USA | 2 |
| Golden State Medical Supply Inc. | 2 |
| Houston Rx LLC | 2 |
| Insight Pharmaceuticals LLC, a Prestige Consumer Healthcare company | 2 |
| Lexia LLC | 2 |
| Meitheal Pharmaceuticals, Inc | 2 |
| Preferred Pharmaceuticals, Inc. | 2 |
| SV Labs Toronto Corporation | 2 |
| Shilpa Medicare Limited | 2 |
| Sunny Pharmtech Inc. | 2 |
| Teva Pharmaceuticals USA, Inc | 2 |
| Zydus Pharmaceuticals (USA) Inc | 2 |

## Class I recalls in full (last good pull: PULL 3, 19 recalls)

| Recall number | Recalling firm | State | Status | Report date | Initiation date | Cause group | Reason for recall (first 100 chars) |
|---------------|---------------|-------|--------|-------------|-----------------|-------------|---------------------------------------|
| D-0743-2026 | Sunny Pharmtech Inc. |  | Ongoing | 20260812 | 20260717 | other | Presence of Particulate Matter; identified as stainless steel |
| D-0744-2026 | Sunny Pharmtech Inc. |  | Ongoing | 20260812 | 20260717 | other | Presence of Particulate Matter; identified as stainless steel |
| D-0769-2026 | Buy-Herbal | NY | Ongoing | 20260819 | 20260321 | other | Marketed Without an Approved NDA/ANDA: Product contains undeclared drug ingredients dexamethasone an |
| D-0772-2026 | Victory Medical Center Pharmacy | TX | Ongoing | 20260819 | 20260701 | sterility | Microbial Contamination of Sterile Products - out of specifications results were obtained for bacter |
| D-0773-2026 | Liebel-Flarsheim Company LLC | NC | Ongoing | 20260819 | 20260731 | other | Presence of Particulate Matter: comprising polyethylene and other plastic materials, stainless steel |
| D-0787-2026 | Baxter Healthcare Corporation | IL | Ongoing | 20260819 | 20260724 | other | Presence of Particulate Matter |
| D-0788-2026 | Fresenius Kabi USA, LLC | IL | Ongoing | 20260826 | 20260804 | labeling | Labeling: Label Mixup: MicroVault labeled as Morphine 2 mg/1 mL, contains a Prefilled Syringe of Dil |
| D-0800-2026 | American Regent, Inc. | NY | Ongoing | 20260826 | 20260724 | contamination | Presence of Particulate Matter: Product contaminated with particulate matter identified as glass and |
| D-0827-2026 | Fresenius Kabi USA, LLC | IL | Ongoing | 20260902 | 20260810 | other | Presence of particulate matter:An internal investigation at the firm found the product to contain gl |
| D-0832-2026 | B BRAUN MEDICAL INC | PA | Ongoing | 20260902 | 20260812 | other | Presence of Particulate matter. |
| D-0849-2026 | Baxter Healthcare Corporation | IL | Ongoing | 20260909 | 20260817 | other | Presence of particulate matter: Particulates identified as fiberglass |
| D-0851-2026 | OPTIMAL BALANCE PHARMACY | TX | Ongoing | 20260909 | 20260805 | sterility | Microbial Contamination of Sterile Products - out of specifications results were obtained for bacter |
| D-0850-2026 | Baxter Healthcare Corporation | IL | Ongoing | 20260916 | 20260817 | other | Presence of Particulate Matter: particulate matter identified as stainless steel particles in the so |
| D-0865-2026 | American Regent, Inc. | NY | Ongoing | 20260916 | 20260811 | sterility | Presence of Particulate Matter and Lack of Assurance of Sterility. Particulate matter identified as  |
| D-0869-2026 | B BRAUN MEDICAL INC | PA | Ongoing | 20260916 | 20260819 | other | Presence of Particulate Matter: particulate matter identified as iron oxide, inorganic material, cel |
| D-0866-2026 | VITRUVIAS THERAPEUTICS INC | AL | Ongoing | 20260923 | 20260821 | potency | Superpotent Drug |
| D-0082-2027 | Par Health USA, LLC | MI | Ongoing | 20261028 | 20261013 | other | Particulate matter: particulate matter identified as cellulose, polystyrene, polyethylene teraphalat |
| D-0083-2027 | Par Health USA, LLC | MI | Ongoing | 20261028 | 20261013 | other | Particulate matter: particulate matter identified as cellulose, polystyrene, polyethylene teraphalat |
| D-0084-2027 | Greenwich Rx | TX | Ongoing | 20261028 | 20261001 | sterility | Microbial Contamination of Sterile Products |

## Changes — PULL 2 vs PULL 1

Matched by key `recall_number`; Changes columns: status, classification, reason_for_recall.

no change — PULL 1 rows 302, PULL 2 rows 302. New: 0. Gone: 0. Changed: 0. (302 = 302 + 0 − 0.) The two CSVs are byte-identical (SHA-256 `f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c` for both).

## Changes — PULL 3 vs PULL 2

Matched by key `recall_number`; Changes columns: status, classification, reason_for_recall.

no change — PULL 2 rows 302, PULL 3 rows 302. New: 0. Gone: 0. Changed: 0. (302 = 302 + 0 − 0.) The two CSVs are byte-identical (SHA-256 `f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c` for both).

No pull failed: every request in all three pulls returned HTTP 200, so no "pull k failed" applies.

## PROOF

### PULL 1

- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=0 — Retrieved (UTC): 2026-11-19T00:01:22Z — HTTP status: 200
- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=100 — Retrieved (UTC): 2026-11-19T00:01:24Z — HTTP status: 200
- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=200 — Retrieved (UTC): 2026-11-19T00:01:25Z — HTTP status: 200
- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=300 — Retrieved (UTC): 2026-11-19T00:01:26Z — HTTP status: 200

Source time (first response Date header, copied exactly): `Thu, 19 Nov 2026 00:01:25 GMT`

Excerpt 1 — raw results total for PULL 1:

```
meta.results.total: 302
```

### PULL 2

- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=0 — Retrieved (UTC): 2026-11-20T00:16:34Z — HTTP status: 200
- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=100 — Retrieved (UTC): 2026-11-20T00:16:35Z — HTTP status: 200
- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=200 — Retrieved (UTC): 2026-11-20T00:16:36Z — HTTP status: 200
- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=300 — Retrieved (UTC): 2026-11-20T00:16:37Z — HTTP status: 200

Source time (first response Date header, copied exactly): `Fri, 20 Nov 2026 00:16:36 GMT`

Excerpt 2 — raw results total for PULL 2:

```
meta.results.total: 302
```

### PULL 3

- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=0 — Retrieved (UTC): 2026-11-21T00:46:20Z — HTTP status: 200
- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=100 — Retrieved (UTC): 2026-11-21T00:46:23Z — HTTP status: 200
- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=200 — Retrieved (UTC): 2026-11-21T00:46:25Z — HTTP status: 200
- Request: https://api.fda.gov/drug/enforcement.json?search=report_date%3A%5B20260801%20TO%2020261231%5D&limit=100&skip=300 — Retrieved (UTC): 2026-11-21T00:46:26Z — HTTP status: 200

Source time (first response Date header, copied exactly): `Sat, 21 Nov 2026 00:46:24 GMT`

Excerpt 3 — raw results total for PULL 3:

```
meta.results.total: 302
```

Excerpt 4 — CSV headers (all three CSVs carry exactly these columns, in this order):

```
recall_number,recalling_firm,state,classification,status,report_date,recall_initiation_date,cause group,reason_for_recall
```

Excerpt 5 — raw result lines of every Class I recall from the last good pull (PULL 3), one line per recall, copied exactly as returned:

```
{"address_1": "Hsinchu Science Park","address_2": "No. 255 Longyuan 1st Rd.; Longtan Dist.","center_classification_date": "20260807","city": "Taoyuan City","classification": "Class I","code_info": "Lot # C23019V1, Exp 10/31/2026; C24015V1, Exp 4/30/2027","country": "Taiwan","distribution_pattern": "USA Nationwide","event_id": "99437","initial_firm_notification": "Letter","more_code_info": "","openfda": {},"postal_code": "N/A","product_description": "Cyclophosphamide for Injection, USP, 1 gram/vial, One Single-Dose Vial, Rx only, Manufactured for: Long Grove Pharmaceuticals, LLC, Rosemont, IL 60018.  Manufactured in Taiwan, NDC 81298-8112-1","product_quantity": "4,077 vials","product_type": "Drugs","reason_for_recall": "Presence of Particulate Matter; identified as stainless steel","recall_initiation_date": "20260717","recall_number": "D-0743-2026","recalling_firm": "Sunny Pharmtech Inc.","report_date": "20260812","state": "","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "Hsinchu Science Park","address_2": "No. 255 Longyuan 1st Rd.; Longtan Dist.","center_classification_date": "20260807","city": "Taoyuan City","classification": "Class I","code_info": "Lot # V24010V1, Exp 3/31/2027","country": "Taiwan","distribution_pattern": "USA Nationwide","event_id": "99437","initial_firm_notification": "Letter","more_code_info": "","openfda": {},"postal_code": "N/A","product_description": "Cyclophosphamide for Injection, USP, 2 gram/vial, One Single-Dose Vial, Rx only, Manufactured for: Long Grove Pharmaceuticals, LLC, Rosemont, IL 60018.  Manufactured in Taiwan, NDC 81298-8114-1","product_quantity": "1,464 vials","product_type": "Drugs","reason_for_recall": "Presence of Particulate Matter; identified as stainless steel","recall_initiation_date": "20260717","recall_number": "D-0744-2026","recalling_firm": "Sunny Pharmtech Inc.","report_date": "20260812","state": "","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "13661 41st Ave","address_2": "Box 239","center_classification_date": "20260817","city": "Flushing","classification": "Class I","code_info": "All lots within expiry.","country": "United States","distribution_pattern": "Product was sold to individual consumers via ebay third party seller.","event_id": "98650","initial_firm_notification": "E-Mail","more_code_info": "","openfda": {},"postal_code": "11355-2464","product_description": "Kian Pee Wan Capsules, 30-count bottles","product_quantity": "71 bottles","product_type": "Drugs","reason_for_recall": "Marketed Without an Approved NDA/ANDA: Product contains undeclared drug ingredients dexamethasone and cyproheptadine.","recall_initiation_date": "20260321","recall_number": "D-0769-2026","recalling_firm": "Buy-Herbal","report_date": "20260819","state": "NY","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "4303 Victory Dr","address_2": "","center_classification_date": "20260819","city": "Austin","classification": "Class I","code_info": "Lot # 1984345, 1980571, 1981940, Use Before Date: 08/27/2026.","country": "United States","distribution_pattern": "USA Nationwide","event_id": "99509","initial_firm_notification": "Telephone","more_code_info": "","openfda": {},"postal_code": "78704-7507","product_description": "Glutathione (MDV), 200 mg/mL, 30 mL vial, each mL contains Glutathione 200 mg, Ascorbic Acid 20 mg, Benzyl Alcohol 1.5%, Na Hydroxide (Ph Adjust) in sterile water for injection, VMC.","product_quantity": "91","product_type": "Drugs","reason_for_recall": "Microbial Contamination of Sterile Products - out of specifications results were obtained for bacterial endotoxin.","recall_initiation_date": "20260701","recall_number": "D-0772-2026","recalling_firm": "Victory Medical Center Pharmacy","report_date": "20260819","state": "TX","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "8800 Durant Rd","address_2": "","center_classification_date": "20260819","city": "Raleigh","classification": "Class I","code_info": "Lot # 25ZF3670, Exp Date: May 31, 2027.","country": "United States","distribution_pattern": "Distributed Nationwide in the US and Mexico.","event_id": "99510","initial_firm_notification": "E-Mail","more_code_info": "","openfda": {"application_number": ["NDA020923"],"brand_name": ["OPTIRAY"],"generic_name": ["IOVERSOL"],"is_original_packager": [true],"manufacturer_name": ["Liebel-Flarsheim Company LLC"],"nui": ["N0000180185","N0000010258"],"package_ndc": ["0019-1333-65","0019-1323-65","0019-1332-65"],"pharm_class_epc": ["Radiographic Contrast Agent [EPC]"],"pharm_class_moa": ["X-Ray Contrast Activity [MoA]"],"product_ndc": ["0019-1323","0019-1333","0019-1332"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["INTRA-ARTERIAL","INTRAVENOUS"],"spl_id": ["471b778f-d9cc-ff10-e063-6394a90a27c9"],"spl_set_id": ["cd718d1c-f813-4114-a50d-c744ff7eb1bf"],"substance_name": ["IOVERSOL"],"unii": ["N3RIB7X24K"],"upc": ["0300191332653","0300191323651","0300191333650"]},"postal_code": "27616-3104","product_description": "Optiray Imaging Bulk Package-350, Ioversol Injection 74%, 350 mg/mL Organically Bound Iodine, 500 mL Multiple-Dose Vial, Rx only, Sterile Solution, Manufactured by: Liebel-Flarsheim Company LLC, Raleigh, NC 27616, Made in USA, NDC 0019-1333-65.","product_quantity": "3,486 500mL-vials","product_type": "Drugs","reason_for_recall": "Presence of Particulate Matter: comprising polyethylene and other plastic materials, stainless steel and glass.","recall_initiation_date": "20260731","recall_number": "D-0773-2026","recalling_firm": "Liebel-Flarsheim Company LLC","report_date": "20260819","state": "NC","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "1 Baxter Pkwy","address_2": "","center_classification_date": "20260821","city": "Deerfield","classification": "Class I","code_info": "Lot # LD175708, Exp Date: 14-Feb-2027.","country": "United States","distribution_pattern": "US Nationwide.","event_id": "99463","initial_firm_notification": "Letter","more_code_info": "","openfda": {"application_number": ["NDA207131"],"brand_name": ["CEFAZOLIN"],"generic_name": ["CEFAZOLIN SODIUM"],"is_original_packager": [true],"manufacturer_name": ["Baxter Healthcare Corporation"],"package_ndc": ["0338-3508-41","0338-3503-41","0338-0096-06"],"product_ndc": ["0338-0096","0338-3508","0338-3503"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["INTRAVENOUS"],"rxcui": ["1665050","1665060","2630753"],"spl_id": ["092b9ea3-0c78-4236-80c9-ff97d09fa14e"],"spl_set_id": ["d91a8d13-99a0-4d87-88dc-71cbd37922b4"],"substance_name": ["CEFAZOLIN SODIUM"],"unii": ["P380M0454Z"]},"postal_code": "60015-4625","product_description": "Cefazolin in Dextrose, Injection, USP, 2g / 100mL (20mg / mL) Single-Dose Infusion Bag in 100mL GALAXY Plastic Container, Frozen Premix, Sterile, Rx only, Manufactured by Baxter Healthcare Corporation, Deerfield, IL 60015, USA, NDC 0338-3508-41.","product_quantity": "19,032 bags","product_type": "Drugs","reason_for_recall": "Presence of Particulate Matter","recall_initiation_date": "20260724","recall_number": "D-0787-2026","recalling_firm": "Baxter Healthcare Corporation","report_date": "20260819","state": "IL","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "3 Corporate Dr","address_2": "","center_classification_date": "20260824","city": "Lake Zurich","classification": "Class I","code_info": "Lot #: 6402820, Exp. Date 12/2028","country": "United States","distribution_pattern": "Nationwide within the USA.","event_id": "99533","initial_firm_notification": "Two or more of the following: Email, Fax, Letter, Press Release, Telephone, Visit","more_code_info": "","openfda": {"application_number": ["NDA204223"],"brand_name": ["MORPHINE SULFATE"],"generic_name": ["MORPHINE SULFATE"],"is_original_packager": [true],"manufacturer_name": ["Fresenius Kabi, USA LLC"],"package_ndc": ["76045-238-01","76045-238-10","76045-004-01","76045-004-11","76045-005-01","76045-005-11","76045-006-01","76045-006-11","76045-007-01","76045-007-11","76045-008-01","76045-008-11"],"product_ndc": ["76045-238","76045-004","76045-005","76045-006","76045-007","76045-008"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["INTRAMUSCULAR","INTRAVENOUS"],"rxcui": ["894912","894914","998212","998213","1442790","2752697"],"spl_id": ["e61f6eb4-cc71-47d3-b2f6-5e689c773779"],"spl_set_id": ["1f53de80-efc8-4930-b3e3-fba0d026af05"],"substance_name": ["MORPHINE SULFATE"],"unii": ["X3P646A2J0"]},"postal_code": "60047-8930","product_description": "Morphine Sulfate Injection, USP, 2 mg /mL, 1 mL single-dose Simplist prefilled syringes, For Intramuscular or Intravenous use, Rx only, Fresenius Kabi, Lake Zurich, IL. Unit of Use NDC Number 76045-004-01; Unit of Sale NDC Number 76045-004-11","product_quantity": "625500 syringes","product_type": "Drugs","reason_for_recall": "Labeling: Label Mixup: MicroVault labeled as Morphine 2 mg/1 mL, contains a Prefilled Syringe of Dilaudid 0.5 mg/0.5 mL.","recall_initiation_date": "20260804","recall_number": "D-0788-2026","recalling_firm": "Fresenius Kabi USA, LLC","report_date": "20260826","state": "IL","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "5 Ramsay Rd","address_2": "","center_classification_date": "20260826","city": "Shirley","classification": "Class I","code_info": "Lot #: 25202, Exp. Date: 11/30/2026.","country": "United States","distribution_pattern": "Nationwide within the U.S","event_id": "99503","initial_firm_notification": "Press Release","more_code_info": "","openfda": {"brand_name": ["PAPAVERINE HYDROCHLORIDE"],"generic_name": ["PAPAVERINE HYDROCHLORIDE"],"is_original_packager": [true],"manufacturer_name": ["American Regent, Inc."],"package_ndc": ["0517-4002-01","0517-4002-25"],"product_ndc": ["0517-4002"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["INTRAVENOUS"],"rxcui": ["1789947"],"spl_id": ["402161da-fe45-4b0f-a5ca-a230593cc434"],"spl_set_id": ["9e5e2ce4-7a57-4c61-a826-64c8d11d038e"],"substance_name": ["PAPAVERINE HYDROCHLORIDE"],"unii": ["23473EC6BQ"],"upc": ["0305174002257"]},"postal_code": "11967-4701","product_description": "Papaverine HCl Injection, USP, 60 mg/2 mL (30 mg/mL), packaged in a) 2mL Single-Dose Vial (NDC 0517-4002-01), and b) 25x2mL Single-Dose Vials (NDC 0517-4002-25), Rx Only, AMERICAN REGENT, INC., SHIRLEY, NY 11967.","product_quantity": "86,100 vials","product_type": "Drugs","reason_for_recall": "Presence of Particulate Matter: Product contaminated with particulate matter identified as glass and/or paraformaldehyde","recall_initiation_date": "20260724","recall_number": "D-0800-2026","recalling_firm": "American Regent, Inc.","report_date": "20260826","state": "NY","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "3 Corporate Dr","address_2": "N/A","center_classification_date": "20260901","city": "Lake Zurich","classification": "Class I","code_info": "Lot: 16UI07, Exp 08/31/2028","country": "United States","distribution_pattern": "Nationwide in the USA","event_id": "99603","initial_firm_notification": "Two or more of the following: Email, Fax, Letter, Press Release, Telephone, Visit","openfda": {"application_number": ["BLA761275"],"brand_name": ["TYENNE"],"generic_name": ["TOCILIZUMAB-AAZG"],"is_original_packager": [true],"manufacturer_name": ["Fresenius Kabi USA, LLC"],"nui": ["N0000190478","N0000190480"],"package_ndc": ["65219-590-04","65219-592-10","65219-594-20"],"pharm_class_epc": ["Interleukin-6 Receptor Antagonist [EPC]"],"pharm_class_moa": ["Interleukin 6 Receptor Antagonists [MoA]"],"product_ndc": ["65219-590","65219-592","65219-594"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["INTRAVENOUS"],"rxcui": ["2679431","2679438","2679440","2679441","2679442","2679443"],"spl_id": ["363d125e-6d69-4bb2-ae09-5eeb5d9edbae"],"spl_set_id": ["e400bbe6-43c5-4de6-82b9-cb44ce3cd906"],"substance_name": ["TOCILIZUMAB"],"unii": ["I031V2H011"]},"postal_code": "60047-8930","product_description": "Tyenne (tocilizumab-aazg) Injection, 400 mg/20 mL (20 mg/mL), 20 mL vial, Rx Only, Manufactured  by Fresenius Kabi USA, LLC,  Lake Zurich, Illinois, 60047, NDC 65219-594-20.","product_quantity": "4,643 20mL-vials","product_type": "Drugs","reason_for_recall": "Presence of particulate matter:An internal investigation at the firm found the product to contain glass particles.","recall_initiation_date": "20260810","recall_number": "D-0827-2026","recalling_firm": "Fresenius Kabi USA, LLC","report_date": "20260902","state": "IL","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "861 Marcon Blvd","address_2": "N/A","center_classification_date": "20260903","city": "Allentown","classification": "Class I","code_info": "Lot#: J4H077, Exp 30NOV2026.","country": "United States","distribution_pattern": "U.S. Nationwide","event_id": "99633","initial_firm_notification": "Letter","openfda": {"application_number": ["NDA019632"],"brand_name": ["LACTATED RINGERS"],"generic_name": ["SODIUM CHLORIDE, SODIUM LACTATE, POTASSIUM CHLORIDE, AND CALCIUM CHLORIDE"],"is_original_packager": [true],"manufacturer_name": ["B. Braun Medical Inc."],"package_ndc": ["0264-7750-00","0264-7750-10","0264-7750-20"],"product_ndc": ["0264-7750"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["INTRAVENOUS"],"rxcui": ["847630"],"spl_id": ["13f7b9a6-d2da-49fe-b7c2-11a4953b2aed"],"spl_set_id": ["d3d29c8f-c326-4097-814a-7f4e08c67068"],"substance_name": ["SODIUM CHLORIDE","SODIUM LACTATE","POTASSIUM CHLORIDE","CALCIUM CHLORIDE"],"unii": ["451W47IQ8X","TU7HW0W0QT","660YQ98I10","M4I0D6VV5M"]},"postal_code": "18109-9577","product_description": "Lactated Ringer's Injection USP, 1000 mL EXCEL container, Rx only, L7500, B. Braun Medical, Inc., Bethlehem, PA 18018-3524 USA, NDC 0264-7750-00","product_quantity": "23,688 bags","product_type": "Drugs","reason_for_recall": "Presence of Particulate matter.","recall_initiation_date": "20260812","recall_number": "D-0832-2026","recalling_firm": "B BRAUN MEDICAL INC","report_date": "20260902","state": "PA","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "1 Baxter Pkwy","address_2": "N/A","center_classification_date": "20260915","city": "Deerfield","classification": "Class I","code_info": "Lot: Y495523, Y495523A, Exp 31-Oct-2027","country": "United States","distribution_pattern": "Natonwide in the USA","event_id": "99678","initial_firm_notification": "Letter","more_code_info": "","openfda": {"application_number": ["NDA018016"],"brand_name": ["SODIUM CHLORIDE"],"generic_name": ["SODIUM CHLORIDE"],"is_original_packager": [true],"manufacturer_name": ["Baxter Healthcare Corporation"],"package_ndc": ["0338-0049-01","0338-0049-02","0338-0049-03","0338-0049-04","0338-0049-10","0338-0049-41","0338-0049-11","0338-0049-31","0338-0049-48","0338-0049-18","0338-0049-38","0338-0043-03","0338-0043-04"],"product_ndc": ["0338-0043","0338-0049"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["INTRAVENOUS"],"rxcui": ["1807551","1807552","1807627","1807630","1807631","1807632","1807633","1807634","1807639"],"spl_id": ["b2052b49-cb90-45d6-b538-f3274f5b46de"],"spl_set_id": ["f55bd888-5e01-474d-871b-24654c070178"],"substance_name": ["SODIUM CHLORIDE"],"unii": ["451W47IQ8X"]},"postal_code": "60015-4625","product_description": "0.9% Sodium Chloride Injection USP 500 mL, VIAFLEX Plastic Containers, with 24 units per case. Baxter Healthcare Corporation, Deerfield, IL, 60015, USA, Made in USA, NDC 0338-0049-03","product_quantity": "145,464 500mL bags","product_type": "Drugs","reason_for_recall": "Presence of particulate matter: Particulates identified as fiberglass","recall_initiation_date": "20260817","recall_number": "D-0849-2026","recalling_firm": "Baxter Healthcare Corporation","report_date": "20260909","state": "IL","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "2204 Cypress Creek Pkwy","address_2": "N/A","center_classification_date": "20260916","city": "Houston","classification": "Class I","code_info": "Lot#: LG342009076, Beyond Use Date: 10/4/26","country": "United States","distribution_pattern": "USA Nationwide.","event_id": "99662","initial_firm_notification": "E-Mail","more_code_info": "","openfda": {},"postal_code": "77090-3113","product_description": "Glutathione 200 mg/mL, 30 mL sterile multidose vial, Each vial contains: Glutathione, Ascorbic Acid, Benzyl Alcohol & sterile water for injection, For IM or IV Injection Use Only, RX only,  Optimal Balance Pharmacy, 2204 Cypress Creek Pkwy Suite F, Houston, TX 77090","product_quantity": "53 vials","product_type": "Drugs","reason_for_recall": "Microbial Contamination of Sterile Products - out of specifications results were obtained for bacterial endotoxin.","recall_initiation_date": "20260805","recall_number": "D-0851-2026","recalling_firm": "OPTIMAL BALANCE PHARMACY","report_date": "20260909","state": "TX","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "1 Baxter Pkwy","address_2": "","center_classification_date": "20260915","city": "Deerfield","classification": "Class I","code_info": "Lot #: Y495066, Exp. Date July 31, 2027","country": "United States","distribution_pattern": "U.S. Nationwide.","event_id": "99679","initial_firm_notification": "Letter","more_code_info": "","openfda": {},"postal_code": "60015-4625","product_description": "Dextrose Injection, USP, 70 %, 2000 mL bags, Rx Only, Baxter Healthcare Corporation Deerfield, IL, 60016, Made in USA, NDC 00338-0719-06","product_quantity": "606 bags","product_type": "Drugs","reason_for_recall": "Presence of Particulate Matter: particulate matter identified as stainless steel particles in the solution.","recall_initiation_date": "20260817","recall_number": "D-0850-2026","recalling_firm": "Baxter Healthcare Corporation","report_date": "20260916","state": "IL","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "5 Ramsay Rd","address_2": "","center_classification_date": "20260922","city": "Shirley","classification": "Class I","code_info": "Lots: 25128L1C0, Exp. August 31, 2026; 25280L1C0, Exp. October 31, 2026; 26108L1C0, Exp. July 31, 2027","country": "United States","distribution_pattern": "Nationwide within the U.S.A","event_id": "99670","initial_firm_notification": "Letter","more_code_info": "","openfda": {"application_number": ["ANDA217192"],"brand_name": ["EPINEPHRINE"],"generic_name": ["EPINEPHRINE"],"is_original_packager": [true],"manufacturer_name": ["American Regent, Inc."],"nui": ["N0000000209","N0000000245","N0000175552","N0000175555","N0000175570","M0003647"],"package_ndc": ["0517-3030-01"],"pharm_class_cs": ["Catecholamines [CS]"],"pharm_class_epc": ["alpha-Adrenergic Agonist [EPC]","beta-Adrenergic Agonist [EPC]","Catecholamine [EPC]"],"pharm_class_moa": ["Adrenergic alpha-Agonists [MoA]","Adrenergic beta-Agonists [MoA]"],"product_ndc": ["0517-3030"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["INTRAMUSCULAR","INTRAVENOUS","SUBCUTANEOUS"],"rxcui": ["310132"],"spl_id": ["495f1aad-cf64-41ab-9f9e-59f6ebeb44aa"],"spl_set_id": ["61cacda5-64ee-45ca-b94c-e8640c43e581"],"substance_name": ["EPINEPHRINE"],"unii": ["YKH834O4BH"]},"postal_code": "11967-4701","product_description": "Epinephrine Injection, USP, 30 mg/30 mL (1mg/mL), 30 mL-Multiple-Dose Vial, Rx Only, For Intravenous Infusion, intramuscular and Subcutaneous Use, AMERICAN REGENT INC., SHIRLEY, NY 11967. NDC 0517-3030-01","product_quantity": "31,935 30mL-vials","product_type": "Drugs","reason_for_recall": "Presence of Particulate Matter and Lack of Assurance of Sterility. Particulate matter identified as nylon, cellulosic, acrylic, polyethylene and glass and broken and leaking vials.","recall_initiation_date": "20260811","recall_number": "D-0865-2026","recalling_firm": "American Regent, Inc.","report_date": "20260916","state": "NY","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "861 Marcon Blvd","address_2": "","center_classification_date": "20260922","city": "Allentown","classification": "Class I","code_info": "Lot #: J6B435, J6B444, J6B457, Exp Date: 30APR2027.","country": "United States","distribution_pattern": "Nationwide within the United States","event_id": "99703","initial_firm_notification": "Letter","more_code_info": "","openfda": {"application_number": ["NDA017464"],"brand_name": ["SODIUM CHLORIDE"],"generic_name": ["SODIUM CHLORIDE"],"is_original_packager": [true],"manufacturer_name": ["B. Braun Medical Inc."],"package_ndc": ["0264-1800-36","0264-1800-31","0264-1800-32"],"product_ndc": ["0264-1800"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["INTRAVENOUS"],"rxcui": ["1807630","1807631","1807632"],"spl_id": ["7d4ee37f-5016-422c-9f66-e675ae22c46a"],"spl_set_id": ["cc14fafd-3dcd-4fc8-bdbd-6f355c375768"],"substance_name": ["SODIUM CHLORIDE"],"unii": ["451W47IQ8X"]},"postal_code": "18109-9577","product_description": "0.9% Sodium Chloride Injection, USP, 100 mL Partial Fill in 150 mL PAB Container, Sterile, Rx only, B. Braun Medical Inc., Bethlehem, PA 18018 USA, NDC 0264-1800-32.","product_quantity": "201,472 total container","product_type": "Drugs","reason_for_recall": "Presence of Particulate Matter: particulate matter identified as iron oxide, inorganic material, cellulose cotton fiber or polystyrene","recall_initiation_date": "20260819","recall_number": "D-0869-2026","recalling_firm": "B BRAUN MEDICAL INC","report_date": "20260916","state": "PA","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "778 N Dean Rd Ste 600","address_2": "N/A","center_classification_date": "20260922","city": "Auburn","classification": "Class I","code_info": "Lot # 504950, Exp Date: 09/30/2026.","country": "United States","distribution_pattern": "US Nationwide.","event_id": "99709","initial_firm_notification": "Letter","more_code_info": "","openfda": {"brand_name": ["THYROID"],"generic_name": ["THYROID"],"is_original_packager": [true],"manufacturer_name": ["Vitruvias Therapeutics"],"package_ndc": ["69680-165-00","69680-166-00","69680-167-00","69680-168-00","69680-169-00"],"product_ndc": ["69680-165","69680-166","69680-167","69680-168","69680-169"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["ORAL"],"rxcui": ["208545","313387","313391","313393","314267"],"spl_id": ["0a6961da-1a42-4233-b6be-7e2d3a930353"],"spl_set_id": ["b1085f7c-70b3-4850-89c0-5d2b3c6c46cf"],"substance_name": ["THYROID"],"unii": ["6RV024OAUQ"]},"postal_code": "36830-4318","product_description": "Thyroid Tablets, USP, 1/2 Grain (30 mg), Each tablet contains: levothyroxine (T4) 19 mcg, liothyronine (T3) 4.5 mcg, 100 Tablets, Rx only, Distributed by: Vitruvias Therapeutics, Auburn, AL 36830, Product of USA, NDC 69680-166-00.","product_quantity": "1955 bottles","product_type": "Drugs","reason_for_recall": "Superpotent Drug","recall_initiation_date": "20260821","recall_number": "D-0866-2026","recalling_firm": "VITRUVIAS THERAPEUTICS INC","report_date": "20260923","state": "AL","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "870 Parkdale Rd","address_2": "","center_classification_date": "20261026","city": "Rochester","classification": "Class I","code_info": "Lot #: 83449, Exp Date: 10/2026; 82682, Exp Date: 11/2026; 86714, 87302, 87560, Exp Date: 02/2027; 87753, 88401, Exp Date: 03/2027; 88614, 88836, Exp Date: 04/2027; 90220, Exp Date: 05/2027; 91216, 91219, Exp Date: 06/2027; 92004, 92006, Exp Date: 07/2027; 92009, 92596, 92782, 93107, 93329, Exp Date: 08/2027; 93890, Exp Date: 09/2027.","country": "United States","distribution_pattern": "Nationwide within the United States","event_id": "100072","initial_firm_notification": "Press Release","more_code_info": "","openfda": {"application_number": ["ANDA091665"],"brand_name": ["ARGATROBAN"],"generic_name": ["ARGATROBAN"],"is_original_packager": [true],"manufacturer_name": ["Par Health USA, LLC"],"nui": ["N0000175980","N0000175518","N0000009963"],"package_ndc": ["42023-182-01"],"pharm_class_epc": ["Anti-coagulant [EPC]","Direct Thrombin Inhibitor [EPC]"],"pharm_class_moa": ["Thrombin Inhibitors [MoA]"],"product_ndc": ["42023-182"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["INTRAVENOUS"],"rxcui": ["308351"],"spl_id": ["05c8d32d-744b-4758-a94e-d912f410bbf7"],"spl_set_id": ["d4e5238f-2378-424e-bda2-f1a2cf874041"],"substance_name": ["ARGATROBAN"],"unii": ["IY90U61Z3S"]},"postal_code": "48307-1740","product_description": "Argatroban Injection, USP, 250 mg/2.5mL (100 mg/mL), 2.5 mL x 1 Single Dose Vial, Rx only, Manufactured for: Endo USA, Malvern,PA 19355/Argatroban Injection, 250 mg/2.5mL (100 mg/mL), 2.5 mL x 1 Single Dose Vial, Rx only,  Distributed by: Par Pharmaceutical, Chestnut Ridge, NY 10977, NDC 42023-182-01.","product_quantity": "18,991 vials","product_type": "Drugs","reason_for_recall": "Particulate matter: particulate matter identified as cellulose, polystyrene, polyethylene teraphalate, stainless steel, or stopper material in the product solution.","recall_initiation_date": "20261013","recall_number": "D-0082-2027","recalling_firm": "Par Health USA, LLC","report_date": "20261028","state": "MI","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "870 Parkdale Rd","address_2": "","center_classification_date": "20261026","city": "Rochester","classification": "Class I","code_info": "Lot #: 84193, Exp Date: 10/2026; 92880, Exp Date: 08/2027.","country": "United States","distribution_pattern": "Nationwide within the United States","event_id": "100072","initial_firm_notification": "Press Release","more_code_info": "","openfda": {"application_number": ["ANDA091665"],"brand_name": ["ARGATROBAN"],"generic_name": ["ARGATROBAN"],"is_original_packager": [true],"manufacturer_name": ["Par Health USA, LLC"],"nui": ["N0000175980","N0000175518","N0000009963"],"package_ndc": ["42023-182-89"],"pharm_class_epc": ["Anti-coagulant [EPC]","Direct Thrombin Inhibitor [EPC]"],"pharm_class_moa": ["Thrombin Inhibitors [MoA]"],"product_ndc": ["42023-182"],"product_type": ["HUMAN PRESCRIPTION DRUG"],"route": ["INTRAVENOUS"],"rxcui": ["308351"],"spl_id": ["493ddc78-4566-486f-8cdd-7d6868ddf153"],"spl_set_id": ["1a67a87d-59cb-414c-a11e-ab8f0a9bb778"],"substance_name": ["ARGATROBAN"],"unii": ["IY90U61Z3S"]},"postal_code": "48307-1740","product_description": "Argatroban Injection, USP, 250 mg/2.5mL (100 mg/mL), 2.5 mL x 1 Single Dose Vial, Rx only, Manufactured for: Endo USA, Malvern,PA 19355/ Argatroban Injection, 250 mg/2.5mL (100 mg/mL), 2.5 mL x 1 Single Dose Vial, Rx only, Distributed by: Par Pharmaceutical, Cranbury, NJ 08512, NDC 42023-182-89.","product_quantity": "1944 vials","product_type": "Drugs","reason_for_recall": "Particulate matter: particulate matter identified as cellulose, polystyrene, polyethylene teraphalate, stainless steel, or stopper material in the product solution.","recall_initiation_date": "20261013","recall_number": "D-0083-2027","recalling_firm": "Par Health USA, LLC","report_date": "20261028","state": "MI","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
{"address_1": "9733 Fm 2902 Rd. Suite 100","address_2": "","center_classification_date": "20261027","city": "Tomball","classification": "Class I","code_info": "Lot # 0060-062426-1, BUD: 10/02/2026; Lot # 0060-062726-1, BUD: 10/05/2026; Lot # 0060-070926-1, BUD: 10/17/2026; Lot # 0060-071426-1, BUD: 10/22/2026; Lot #0060-071426-2, BUD: 10/22/2026; Lot # 0060-072026-1, BUD: 10/28/2026; Lot # 0060-072726-1, BUD: 11/04/2026; Lot #0060-072926-1, BUD: 11/06/2026; Lot # 0060-073126-1; BUD: 11/08/2026; Lot # 0060-080426-1, BUD: 11/12/2026; Lot #: 0060-080526-1, BUD: 11/13/2026; Lot # 0060-081826-1, BUD: 11/26/2026.","country": "United States","distribution_pattern": "US Nationwide in th USA","event_id": "100004","initial_firm_notification": "Press Release","more_code_info": "","openfda": {},"postal_code": "77375","product_description": "Glutathione Injection (Glutathione-L, Ascorbic Acid, Sodium Hydroxide, Bacteriostatic Water), 200 mg/mL, 10 mL multi-dose vial, Rx only, Subcutaneous Only, Greenwich Rx.","product_quantity": "4,319 vials","product_type": "Drugs","reason_for_recall": "Microbial Contamination of Sterile Products","recall_initiation_date": "20261001","recall_number": "D-0084-2027","recalling_firm": "Greenwich Rx","report_date": "20261028","state": "TX","status": "Ongoing","voluntary_mandated": "Voluntary: Firm initiated"}
```

Excerpt 6 — platform record of the three PULL notes (progress-note responses, recordedAt is Synmerco server time):

```
PULL 1 note recordedAt: 2026-11-19 00:01:51Z — "PULL 1: 302 rows, CSV SHA-256 f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c, raw total 302, source time Thu, 19 Nov 2026 00:01:25 GMT."
PULL 2 note recordedAt: 2026-11-20 00:17:34.151018+00 — "PULL 2: 302 rows, CSV SHA-256 f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c, raw total 302, source time Fri, 20 Nov 2026 00:16:36 GMT. CSV identical to PULL 1 (no changes)."
PULL 3 note recordedAt: 2026-11-21 00:46:48.217771+00 — "PULL 3: 302 rows, CSV SHA-256 f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c, raw total 302, source time Sat, 21 Nov 2026 00:46:24 GMT. CSV identical to PULL 2 (no changes)."
```

Excerpt 7 — computed counts verified directly against drug-recalls-pull3.csv (302-row CSV; paging skip 0, 100, 200, 300):

```
csv: 302-row CSV; paging skip 0, 100, 200, 300
classification: Class II 263, Class I 19, Class III 18, Not Yet Classified 2 — total 302
cause group: other 114, manufacturing practice 71, sterility 58, contamination 30, potency 22, labeling 7 — total 302
month: 2026-08 53, 2026-09 83, 2026-10 75, 2026-11 91 — total 302
repeat firms: 41 firms with 2 or more recalls; most recalls by one firm: Victory Medical Center Pharmacy 43
status: Ongoing 302
```

## Data files

- D2 `drug-recalls-pull1.csv` — 302 rows, SHA-256 `f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c`
- D3 `drug-recalls-pull2.csv` — 302 rows, SHA-256 `f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c`
- D4 `drug-recalls-pull3.csv` — 302 rows, SHA-256 `f47a44d69db198f4d979766806d03c9974d1761f149a314a05fd559b0334d90c`

Columns, in order: `recall_number,recalling_firm,state,classification,status,report_date,recall_initiation_date,cause group,reason_for_recall`. Sorted by report_date then recall_number. One row per recall returned, never split; values as returned, reason cut to 100 characters. Key column: recall_number.

Source: openFDA drug enforcement, host api.fda.gov, endpoint /drug/enforcement.json. Only the sources listed in the job.