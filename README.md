# aadhaar-in-context
Exploring Aadhaar enrolment and update data with a focus on patterns, change, and context.
Day-1 (14/1/25)
UIDAI Datasets analysis

Background Analysis:
UIDAI is the Unique Identification Authority of India. They issue aadhar which has an unique identification number.
-Issuing of the first UID was on September 2010. 

Aadhaar Number generation:
-Aadhaar is a random number that never starts with a 0 or 1
-Aadhar UID is Unique Identification Number xxxx-xxxx-xxxx
-Aadhaar first 11 numbers are random but the last number is generated using Verhoeff 
 Algorithm for typing mistakes and fake numbers.
-Aadhaar data is kept in about 7,000 servers in Bengaluru and Manesar.
-The major advantage is that all this can be taken care of by simply producing a citizen   
  identity card as proof of individual identity.
-In 2020, UIDAI introduced a new physical Aadhaar card made of PVC with additional 
 security features such as holograms, micro text, ghost images, guilloché Patterns, 
 invisible logos etc.
-Not limited to citizens - any resident of India (≥182 days in past 12 months) can get it

Criticism:
1. Privacy & Data Protection- Aadhaar stores sensitive data; India had no strong privacy law for years.
2. Security breaches & data leaks: Repeated leaks from government/agency portals
3. Mandatory use vs Supreme Court limits
4 . Exclusion from Welfare due to Authentication Failures- Fingerprints fail, Network outages block food rations & NREGA wages
5. Linking with Other Databases: Data leakages

Population of India
	Current population is 1.47 billion by 2050 it is expected to be 1.67 billion
Given datasets are:	
  -Enrolment Data
  -Demographic Update Data
  -Biometric Update Data

1. Enrolment dataset details
Starts on 2-03-2025 till 31-12-2025
Contains 3 csv files named api_data_aadhar_enrolment_0_500000.csv, api_data_aadhar_enrolment_500000_1000000.csv, api_data_aadhar_enrolment_1000000_1006029.csv
Rows: Number of rows mentioned in the title
Columns(7): date (date of enrollment), state, district, pincode, age_0_5, age_5_18, age_18_greater
Understanding: 
India uses a 6-digit PIN (Postal Index Number) system to identify postal regions and post offices.
The first digit indicates the postal zone.
1–8 → Civilian geographical zones of India
9 → Army Postal Service (APS)
Army PIN codes always start with 9 and are assigned to military units, not geographic locations.
The first 2 digits represent the postal circle / sub-region.
The first 3 digits identify the sorting district.
The last 3 digits specify the individual post office.
India currently has ~19,000 active PIN codes, while the system allows up to 1,000,000 possible combinations, so it is highly scalable


2. Demographic Update Data dataset
Contains 5 csv files named api_data_aadhar_demographic_0_500000.csv, api_data_aadhar_demographic_500000_1000000.csv, api_data_aadhar_demographic_1000000_1500000.csv, api_data_aadhar_demographic_1500000_2000000.csv, api_data_aadhar_demographic_2000000_2071700.csv
Rows: Number of rows mentioned in the title
Columns(6): date (date of enrollment), state, district, pincode, demo_age_5_17 (Age of people who updated), demo_age_17_
Starts on 1-03-2025 till 29-12-2025

3. Biometric Update Data
Contains 3 csv files named api_data_aadhar_biometric_0_500000.csv, api_data_aadhar_biometric_500000_1000000.csv, api_data_aadhar_biometric_1000000_1500000.csv, api_data_aadhar_biometric_1500000_1861108.csv
Starts on 1-03-2025 till 29-12-2025
Rows: Number of rows mentioned in the title
Columns(6): date (date of enrollment), state, district, pincode, bio_age_5_17 (Age of people who gave biometrics), bio_age_17_


