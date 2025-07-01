# Software Testing
- Mengecek apakah program ada eror sebelum dikirim ke user
- Bukan hanya eror kritikal, namun kualitas, performa, dan standar performa juga
- Agar efektif, harus strategis:
	- Review yang efektif
	- Mulai dari komponen yang kecil hingga ke seluruh sistem dan integrasi berbagai macam komponen tersebut
	- Biasanya dilakukan oleh grup eksternal jika projek besar
	- Debugging dan testing berbeda
- Developer akan melakukan testing agar produk bisa dirilis secepat mungkin / sebelum deadline. Independent tester akan melakukan testing agar produk kualitasnya sebaik mungkin.
## Verification & Validation
- Verifikasi: apakah produk sesuai standar?
- Validasi: apakah produk ini diinginkan user?

## Isu
- Harus ada "target"
- Target harus mengikuti kemauan user
- Software sebaiknya "mengetest" dirinya sendiri
- Selalu perbarui / adaptasi proses testing

## Integration Testing Strategies
- Top down
- Bottom up
- Sandwich

## Testing lainnya
- Regression, mengulang tes untuk memastikan perubahan tidak menyebabkan perubahan tidak terduga
- Smoke, komponen terbaru diintegrasikan ke build rilis kemudian build tersebut dites

## Object Oriented Testing
- Mirip software testing, namun metode dan objek diperhatikan
- Integration testing:
	- Thread-based, kelas diberikan input dan outputnya direview
	- use-based, beberapa kelas digunakan untuk suatu test-case
	- cluster, beberapa kelas digunakan untuk suatu fitur
- Metode:
	- Fault-based, mencari kemungkinan masalah, membuat testing untuk mengetes hipotesis tersebut
	- Class & Class Hierarchy, mengecek hierarki kelas / inheritance
	- Scenario-based, melihat aksi user dan membuat tes berdasarkan aksi user
- Metode OOT:
	- Random
	- Partition
	- Inter-Class
	- Behaviour Testing

## WebApp Testing
- Konten, fungsi, dan struktur webapp dites untuk menemukan eror
- Konten dites pada 2 level,
	- Semantic, validasi informasi, ke-konsisten-an
	- Synctactic, tata bahasa, typo, dll.
- Fungsi dites untuk kebenaran, ketidak stabilan, dan mengikuti standar
- Struktur dites untuk modularitas dan konten bisa disajikan dengan baik
- Usability dan Navigability dites untuk UX dan konten rusak (link rusak, dll)
- Performance, obvious
- Compatibility, obvious
- Interoperability, kemampuan Web app untuk berinteraksi dengan sistem lain
- Security, obvious
- Dites oleh grup end-user terpilih

## High Order Testing
- Validation, untuk requirements / kebutuhan
- System, untuk integrasi sistem
- A/B, melihat preferensi end-user
- Recovery, melihat recovery software jika ada eror
- Security, obvious
- Stress, obvious
- Performance, obvious

## Debugging
- Membenarkan masalah
- Melakukan regression testing
- Teknik
	- Brute force
	- Backtracking
	- Induction
	- Deduction

## Testability
- Operability
- Observability
- Controllability
- Decomposability
- Simplicity
- Stability
- Understandability

## White Box Testing
- Melihat keseluruhan dan setiap kemungkinan "logika" / path aplikasi
- Basis path testing, data flow testing, control structure testing, loop testing, 

## Black Box Testing
- Mengetes aplikasi tanpa mengetahui code spesifik
- equivalence partitioning, boundary values analysis, comparison testing, orthogonal array testing, model based testing

# Project Management
## 4P
- People, every human involved
- Product, the product to be built
- Process, the frameworks to get the job done
- Project, all the work

## Stakeholders
- Anyone who's involved in the project
- Senior managers, define issues
- Project / Technical Managers, plan, motivate, and organise practitioners
- Practitioners, people who actually works on the project
- Customers, specify the needs to be filled + other stakeholders who have an interest in the outcome
- End-users, users

## Software Teams
- When structuring the team, the difficulty, size, length, and how (quality, modularity, standard, etc.) the problem is built needs to be considered
- Avoid toxicity (frenzied work, frustration, low accountability, poor communication, low morale)

## AGILE Teams
- Trust needed
- "Mavericks" / Wild members excluded / coherence needed
- Skills must be distributed
- Team is self organising (Closed, Random, Open, and Syncronous paradigms combined)
## Organisational Paradigms
- Closed, traditional hierarcy
- Random, no hierarcy, depends on member's initiative
- Open, closed + random
- Synchronous, each member focuses on their own problem, little teamwork
### MOI Model
- Motivation
- Organization
- Ideas / Innovation

## Product Scope
- Must be understandable, unambiguous
- Problem decomposition; Once a scope is defined, what does the individual components do? What do they look like?
### Scope
- Context, how does the software fit into an existing system? What does it do?
- Information objectives, What are the inputs? What should the output be?
- Function & Performance, What does the software do? Any special requirements?

## Scheduling principles
- Compartmentalization, define tasks
- Interdependency, indicate tasks interrelationship
- effort validation, ensure resources are available
- defined responsibilities, people must be assigned
- defined outcomes, every task must have a goal
- defined milestones, a deadline or a review for quality

## Effort Allocation
- 40-50% front end; designing, review, modification, customer communication
- 15-20% coding
- 30-40% testing (unit, integration, black & white box, regression)

## Task sets
- Determine project type
- assess degree of rigor required
- identify adaptation criteria
	- select appropriate software engineering tasks 