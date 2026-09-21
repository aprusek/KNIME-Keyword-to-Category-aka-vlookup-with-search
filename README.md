# KNIME-Keyword-to-Category-aka-vlookup-with-search

How to scan a field for a keyword and lable the record with a Category from a Lookup file

<img width="6504" height="2456" alt="image" src="https://github.com/user-attachments/assets/e61dd7d7-3efe-4eb5-b056-7c793cfe5a87" />

1 - Node used to restart all subsequent nodes

2 - CSV reader of Input File

3 - Add original ROWID to data, used to join the Category later

4 - Remove columns not needed for matching stream

5 - Set columns used for matching to UPPERCASE

6 - CSV reader for Keyword/Category mapping file, one line per Key, multiple keys can be mapped to one category

7 - Remove un-used columns

8 - Set columns used for matching to UPPERCASE

9 - Cross Join original Description + ROWID to KEY + CATEGORY

10 - Count occurances of the KEY in the DESCRIPTION column
<img width="1732" height="1242" alt="image" src="https://github.com/user-attachments/assets/523a7d6f-f503-464a-96ec-a8620d713bc3" />

11 - Filter rows with zero KEY values found
<img width="1014" height="1210" alt="image" src="https://github.com/user-attachments/assets/9243821a-dadd-4a91-9f6f-d0346d677b20" />

12 - Remove Duplicate Rows (reqturn first KEY match only
<img width="1010" height="1494" alt="image" src="https://github.com/user-attachments/assets/a08b0679-3362-4510-b35d-fc74248fe192" />

13 - Join Inmput data with CATEGORIES
<img width="1006" height="1394" alt="image" src="https://github.com/user-attachments/assets/4336acb1-ad65-48ad-b661-906a919f71b6" />

14 - Remove un-used columns

15 - Output Data
