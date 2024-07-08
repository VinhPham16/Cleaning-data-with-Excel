
-	Split data:
Field “PropertyAddress” has the value with format “address, city” and field “OwnerAddress” has the value with format “address, city, state” so the purpose is split address and city into two separated columns so it will be helpful for later with statistic or visualize.
In Excel, I use Text to columns to solve this: 
o	Choose Delimited ->  Delimiters by Comma -> Data format: Text
“PropertyAddress” field was splited into 2 seperated fields name “PropertyAddressSplitAddress” and “PropertyAddressSplitCity”
As the same method we did with “PropertyAddress field”, “OwnerAddress” was splited into 3 fields name “OwnerAddressSplitAddress”, “OwnerAddressSplitCity”, “OwnerAddressSplitState”.
	
-	Convert data type
Field “SaleDate”’s original format is in various of date format so we need to format into one only shared format. In this case, I want this field to be reformatted as “YYYY-MM-DD” to import into SQL.

-	Replace data value
“SoldAsVacant” is standed for answer with two answers Yes and No but values in this field is “Yes” “Y” “No” “N” so all values need to be unified as 1 value for each answer. I will transfer “No” into “N” and “Yes” into “Y”

-	Checking for duplicate
Checking for duplicate with Function: “Duplitcate Values” in Excel then base on ParcelID, SaleDate and LegalReference to delete value that duplicated 
-	Finally, I delete fields that I don’t need or I already create another field that similar to.
