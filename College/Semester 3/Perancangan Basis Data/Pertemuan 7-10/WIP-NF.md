<!-- https://en.wikipedia.org/wiki/Database_normalization -->
# 1st Normal Form
1 row, 1 attribute value

Observe the following table:
![[Pasted image 20251007081839.png]]
This is **NOT** allowed, due to "address" serving multiple rows

![[Pasted image 20251007082149.png]]
	  
![[Pasted image 20251007082050.png]]
This is **NOT** allowed, due to items 1 and 4 having more than 1 attribute value

![[Pasted image 20251007082207.png]]
This is fine

Observe the following table:

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

# 2nd Normal Form
- Each 1NF is also a 2NF if it contains no partial dependencies.
	-   ![[Pasted image 20251104084746.png]]
	  The table is NOT 2NF. `kode_faktur` and `nama_barang` are both UIDs. Imagine if we need to change the name "Indomie Goreng" to "Alfamie Goreng"; we would need to change 2 entries (entry 1 and 5), which would be increasingly cumbersome the larger the table gets.
	  What we can do is split the table into 2. One to handle manufacturing da