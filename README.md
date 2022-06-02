# This project aims to automate some of the boring stuff in hospital medicine

files:
1. PMH LU file
2. Med LU file
3. Med indications file
4. med class file



Med->indication file:
For each medicine, its indication is listed

Med-> class file
For each medicine, the class it is derived from is indicated.


june 1st 2022: four new files added
Each of these files have 2 rows. These will be used to make dictionaries. The keys will be from the first row, the values from the second row
1. med_cls.csv = this maps each med to its class
2. med_indic.csv = this maps meds to indication. Each med-indication pair is a row. As each med will map to multiple indications, I will have to groupby the first column and list the second column to create a df which can then be used to make a one to many look up dictionary
3. med_map.csv = this maps generic and trade names to generic names. This dict is used to map the same drug with different trade names to the same medication entity.
4. clinical_entities_map.csv = This dataframe maps many to one. It compresseses variations in naming such as HFpEF and CHF into the same clinical entity. Essentially clinical entities which have different names, but are otherwise essentially the same, should map to a single entitiy. This way one can limit the number of entities one has to deal with, and thus one is able to write down functions and rules when said entity is encountered.
