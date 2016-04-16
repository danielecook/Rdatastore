[![Build Status](https://travis-ci.org/danielecook/rdatastore.svg?branch=master)](https://travis-ci.org/danielecook/rdatastore)

# rdatastore
R package for accessing google datastore


### To Do

* [x] Add tests for autoallocation of ids when committing.
* [x] Add tests for __keep_existing__ T/F.
* [x] Add test for datetime consistancy.
* [x] When committing, return data and transaction id.
* [ ] Blob support.
* [ ] Check for character vectors/lists, etc.

### Functions

* [x] `lookup` - Lookup single entities. Returns a data frame.
* [x] `commit` - Update a single entity.
* [ ] `commit_df` - Save a dataframe to the google datastore with update/upsert/insert/delete (consistant data).
* [ ] `commit_list` - Save a list (heterogeneous data).
* [ ] `runQuery` - Function for querying. Possibly using dplyr style.
* [ ] `datasets` - A centralized function for tracking/accessing datasets. Read only store.

### Features

* [x] __keep_existing__ When updating - keep existing values, add new ones, and overwrite where specified.
* [ ] Figure out how to store blobs or at the very least offer way to serialize data (_e.g._ lists, df, and other types of objects).

#### `commit_df()`

User specifies a key (unique value) for a given dataframe  

#### `datasets()`

The aim of the datasets function is to centralize storage of datasets and make them easily searchable. 
