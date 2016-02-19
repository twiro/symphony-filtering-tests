# Input Field


## Available Filters

1. **is**
2. **contains**
3. **does not contain**


## Sample Data

1. `Andorra`
2. `Bosnien & Herzegowina`
3. `Deutschland`
4. `Grönland`
5. `Großbritannien`
6. `Österreich`
7. `USA`


## Tests

###### Performed with Symphony CMS 2.6.5

| Nr. | Filter | Value | Expected Result | DF | PF |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1.1 | **is** | `Deutschland` | **3** | :white_check_mark: | :white_check_mark: |
| 1.2 | **is** | `Grönland` | **4** | :white_check_mark: | :white_check_mark: |
| 1.3 | **is** | `Bosnien & Herzegowina` | **2** | :white_check_mark: | :white_check_mark: |
| 1.4 | **is** | `Österreich, Großbritannien` | **5**, **6** | :white_check_mark: | :white_check_mark: / :x: * |
| 1.5 | **is** | `USA, Bosnien & Herzegowina` | **2**, **7** | :white_check_mark: | :x: |
| 2.1 | **contains** | `land`  | **3**, **4** | :white_check_mark: | :white_check_mark: |
| 2.2 | **contains** | `Gr` | **4**, **5** | :white_check_mark: | :white_check_mark: |
| 2.3 | **contains** | `s` | **2**, **3**, **6**, **7** | :x: | :x: |
| 2.4 | **contains** | `Ö` | **4**, **6** | :white_check_mark: | :white_check_mark: |
| 2.5 | **contains** | `ö` | **4**, **6** | :x: | :x: |
| 2.6 | **contains** | `&` | **2** | :white_check_mark: | :x: |
| 2.7 | **contains** | `en & Herz` | **2** | :white_check_mark: | :x: |
| 2.8 | **contains** | `^G` | **4**, **5** | :white_check_mark: | :white_check_mark: |
| 2.9 | **contains** | `a$` | **1**, **2**, **7** | :white_check_mark: | :white_check_mark: |
| 3.1 | **does not contain** | `land` | **1**, **2**, **5**, **6**, **7** | :white_check_mark: | :white_check_mark: |
| 3.2 | **does not contain** | `Gr` | **1**, **2**, **3**, **6**, **7** | :white_check_mark: | :white_check_mark: |
| 3.3 | **does not contain** | `s` | **1**, **4**, **5** | :white_check_mark: | :white_check_mark: |
| 3.4 | **does not contain** | `Ö` | **1**, **2**, **3**, **5**, **7** | :x: | :x: |
| 3.5 | **does not contain** | `ö` | **1**, **2**, **3**, **5**, **7** | :x: | :x: |
| 3.6 | **does not contain** | `&` | **1**, **3**, **4**, **5**, **6**, **7** | :x: | :x: |
| 3.7 | **does not contain** | `en & Herz` | **1**, **3**, **4**, **5**, **6**, **7** | :x: | :x: |
| 3.8 | **does not contain** | `^G` | **1**, **2**, **3**, **6**, **7** | :white_check_mark: | :white_check_mark: |
| 3.9 | **does not contain** | `a$` | **3**, **4**, **5**, **6** | :white_check_mark: | :white_check_mark: |

<sup>
<strong>*</strong> Works when using autocomplete suggestions <i>/</i> Doesn't work when typing manually.
</sup>

<sup>
<strong>DF</strong> = Datasource Filtering
<i>/</i>
<strong>PF</strong> = Publish Filtering
</sup>
