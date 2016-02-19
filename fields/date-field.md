# Date Field


## Available Filters

1. **is**
2. **contains**
3. **does not contain**
4. **later than**
5. **earlier than**
6. **equal to or later than**
7. **equal to or earlier than**
8. **between** *
9. **relative** *

<sup>
<strong>*</strong> Not displayed in the symphony admin area yet.
</sup>

## Date formats

- `y`
- `y-m`
- `y-m-d`
- `y-m-d H:i:s`


## Sample Data

1. `2011-05-10 2:00pm`
2. `2011-06-01 12:00am`
3. `2010-07-01 3:00pm`
4. `1960-10-10 2:00am`
5. `2012-03-04 7:30pm`


## Tests

###### Performed with Symphony CMS 2.6.5

| Nr. | Filter | Value | Expected Result | DF | PF |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1.1 | **is** | `2011` | **1**, **2** | :white_check_mark: | :white_check_mark: |
| 1.2 | **is** | `2010-05` | – | :white_check_mark: | :white_check_mark: |
| 1.3 | **is** | `2011-06-01` | **2** | :white_check_mark: | :white_check_mark: |
| 1.4 | **is** | `2011-06-10 2:00pm` | – | :white_check_mark: | :white_check_mark: |
| 1.5 | **is** | `1960-10-10 2:00am` | **4** | :white_check_mark: | :white_check_mark: |
| 2.1 | **contains** | `2011`  | **1**, **2** | :white_check_mark: | :white_check_mark: |
| 2.2 | **contains** | `10` | **1**, **3**, **4** | :white_check_mark: | :white_check_mark: |
| 3.1 | **does not contain** | `2011` | **3**, **4**, **5** | :white_check_mark: | :white_check_mark: |
| 3.2 | **does not contain** | `10` | **2**, **5** | :white_check_mark: | :white_check_mark: |
| 4.1 | **later than** | `2011` | **5** | :white_check_mark: | :white_check_mark: |
| 4.2 | **later than** | `2012` | – | :white_check_mark: | :white_check_mark: |
| 4.3 | **later than** | `1960` | **1**, **2**, **3**, **5** | :white_check_mark: | :white_check_mark: |
| 4.4 | **later than** | `2011-05` | **2**, **5** | :white_check_mark: | :white_check_mark: |
| 4.5 | **later than** | `2011-05-02` | **1**, **2**, **5** | :white_check_mark: | :white_check_mark: |
| 4.6 | **later than** | `2010-05-10 1:00pm` | **1**, **2**, **3**, **5** | :white_check_mark: | :white_check_mark: |
| 4.7 | **later than** | `2011-05-10 11:00am` | **1**, **2**, **5** | :white_check_mark: | :white_check_mark: |
| 4.8 | **later than** | `2011-05-10 2:00pm` |  **2**, **5** | :white_check_mark: | :white_check_mark: |
| 4.9 | **later than** | `2011-06-01 8:00pm` |  **5** | :white_check_mark: | :white_check_mark: |
| 5.1 | **earlier than** | `2011` | **3**, **4** | :white_check_mark: | :white_check_mark: |
| 5.2 | **earlier than** | `2012` | **1**, **2**, **3**, **4** | :white_check_mark: | :white_check_mark: |
| 5.3 | **earlier than** | `1960` | – | :white_check_mark: | :white_check_mark: |
| 5.4 | **earlier than** | `2011-05` | **3**, **4** | :white_check_mark: | :white_check_mark: |
| 5.5 | **earlier than** | `2011-05-02` | **3**, **4** | :white_check_mark: | :white_check_mark: |
| 5.6 | **earlier than** | `2011-07-01 11:00am` | **1**, **2**, **3**, **4** | :white_check_mark: | :white_check_mark: |
| 5.7 | **earlier than** | `2011-05-10 2:00pm` | **3**, **4** | :white_check_mark: | :white_check_mark: |
| 5.8 | **earlier than** | `2011-06-01 8:00pm` |  **1**, **2**, **3**, **4** | :white_check_mark: | :white_check_mark: |
| 6.1 | **equal to or later than** | `2011` | **1**, **2**, **5** | :white_check_mark: | :white_check_mark: |
| 6.2 | **equal to or later than** | `2012` | **5** | :white_check_mark: | :white_check_mark: |
| 6.3 | **equal to or later than** | `1960` | **1**, **2**, **3**, **4**, **5** | :white_check_mark: | :white_check_mark: |
| 6.4 | **equal to or later than** | `2011-05` | **1**, **2**, **5** | :white_check_mark: | :white_check_mark: |
| 6.5 | **equal to or later than** | `2011-05-02` | **1**, **2**, **5** | :white_check_mark: | :white_check_mark: |
| 6.6 | **equal to or later than** | `2010-05-10 1:00pm` | **1**, **2**, **3**, **5** | :white_check_mark: | :white_check_mark: |
| 6.7 | **equal to or later than** | `2011-05-10 11:00am` | **1**, **2**, **5** | :white_check_mark: | :white_check_mark: |
| 6.8 | **equal to or later than** | `2011-05-10 2:00pm` |  **1**, **2**, **5** | :white_check_mark: | :white_check_mark: |
| 6.9 | **equal to or later than** | `2011-06-01 8:00pm` |  **5** | :white_check_mark: | :white_check_mark: |
| 7.1 | **equal to or earlier than** | `2011` | **1**, **2**, **3**, **4** | :white_check_mark: | :white_check_mark: |
| 7.2 | **equal to or earlier than** | `2012` | **1**, **2**, **3**, **4**, **5** | :white_check_mark: | :white_check_mark: |
| 7.3 | **equal to or earlier than** | `1960` | **4** | :white_check_mark: | :white_check_mark: |
| 7.4 | **equal to or earlier than** | `2011-05` | **1**, **3**, **4** | :white_check_mark: | :white_check_mark: |
| 7.5 | **equal to or earlier than** | `2011-05-02` | **3**, **4** | :white_check_mark: | :white_check_mark: |
| 7.6 | **equal to or earlier than** | `2010-05-10 1:00pm` | **4** | :white_check_mark: | :white_check_mark: |
| 7.7 | **equal to or earlier than** | `2011-05-10 11:00am` | **3**, **4** | :white_check_mark: | :white_check_mark: |
| 7.8 | **equal to or earlier than** | `2011-05-10 2:00pm` |  **1**, **3**, **4** | :white_check_mark: | :white_check_mark: |
| 7.9 | **equal to or earlier than** | `2011-06-01 8:00pm` |  **1**, **2**, **3**, **4** | :white_check_mark: | :white_check_mark: |
| 8.1 | **between** | `2011 to 2012` | **1**, **2**, **5** | :white_check_mark: | :white_check_mark: |
| 8.2 | **between** | `2011-05 to 2012-05` | **1**, **2**, **5** | :white_check_mark: | :white_check_mark: |
| 8.3 | **between** | `2011-05-01 to 2011-06-10` | **1**, **2** | :white_check_mark: | :white_check_mark: |
| 8.4 | **between** | `2010-06-01 2:00pm to 2011-06-01 11:00pm` | **1**, **2**, **3** | :white_check_mark: | :white_check_mark: |
| 8.5 | **between** | `2010-05-01 11:00am to 2011` | **1**, **2**, **3** | :white_check_mark: | :white_check_mark: |
| 8.6 | **between** | `2010-05-01 11:00am to 2011-05` | **1**, **3** | :white_check_mark: | :white_check_mark: |
| 8.7 | **between** | `2010-06-01 12:00am to 2010-06-01 9:30pm` | – | :white_check_mark: | :white_check_mark: |

<sup>
<strong>DF</strong> = Datasource Filtering
<i>/</i>
<strong>PF</strong> = Publish Filtering
</sup>

