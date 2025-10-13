# 1 NF
- 1 row, 1 attribute value
	- ![[Pasted image 20251007081839.png]]
	  This is **NOT** allowed, due to "address" serving multiple rows
	  
	  ![[Pasted image 20251007082149.png]]
	  This is fine
	  
	- ![[Pasted image 20251007082050.png]]
	  This is **NOT** allowed, due to items 1 and 4 having more than 1 attribute value
	  
	  ![[Pasted image 20251007082207.png]]
	  This is fine
- Observe the following table:

| id  | name            | address       | store_name | store_floor |
| --- | --------------- | ------------- | ---------- | ----------- |
| 1   | Central Park    | Tanjung Duren | CGV        | 4           |
|     |                 |               | KKV        | GF          |
| 2   | Lippo Puri Mall | Puri Indah    | KKV        | 3           |
|     |                 |               | AZKO       | 2           |
| 3   | Neo Soho        | Tanjung Duren | Mixue      | 2           
	It is unnormal. The normalised table would be:

| id  | name            | address       | store_name | store_floor |
| --- | --------------- | ------------- | ---------- | ----------- |
| 1   | Central Park    | Tanjung Duren | CGV        | 4           |
| 1   | Central Park    | Tanjung Duren | KKV        | GF          |
| 2   | Lippo Puri Mall | Puri Indah    | KKV        | 3           |
| 2   | Lippo Puri Mall | Puri Indah    | AZKO       | 2           |
| 3   | Neo Soho        | Tanjung Duren | Mixue      | 2           |