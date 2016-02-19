# Tag List Field


## Available Filters

1. **is**
2. **contains**
3. **does not contain**


## Sample Data

1. `Andorra`, `Europa`
2. `Bosnien & Herzegowina`, `Europa`
3. `Deutschland`, `Europa`
4. `Grönland`, `Europa`, `Insel`
5. `Großbritannien`, `Europa`, `Insel`
6. `Österreich`, `Europa`
7. `USA`, `Amerika`


## Tests

###### Performed with Symphony CMS 2.6.5

| Nr. | Filter | Value | Expected Result | DF | PF |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1.1 | **is** | `Deutschland` | **3** | :white_check_mark: | :white_check_mark: |
| 1.2 | **is** | `Österreich` | **6** | :white_check_mark: | :white_check_mark: |
| 1.3 | **is** | `Bosnien & Herzegowina` | **2** | :white_check_mark: | :white_check_mark: / :x: * |
| 1.4 | **is** | `Insel, Deutschland` | **3**, **4**, **5** | :white_check_mark: | :white_check_mark: |
| 1.5 | **is** | `Österreich, Großbritannien` | **5**, **6** | :white_check_mark: | :white_check_mark: |
| 1.5 | **is** | `USA+Amerika` | **7** | :x: | :x: |
| 2.1 | **contains** | `land`  | **3**, **4** | :white_check_mark: | :white_check_mark: |
| 2.2 | **contains** | `Gr` | **4**, **5** | :white_check_mark: | :white_check_mark: |
| 2.3 | **contains** | `Ö` | **4**, **6** | :white_check_mark: | :white_check_mark: |
| 2.4 | **contains** | `ö` | **4**, **6** | :x: | :x: |
| 2.5 | **contains** | `&` | **2** | :white_check_mark: | :x: |
| 2.6 | **contains** | `en & Herz` | **2** | :white_check_mark: | :x: |
| 2.7 | **contains** | `^G` | **4**, **5** | :white_check_mark: | :white_check_mark: |
| 2.8 | **contains** | `l$` | **4**, **5** | :white_check_mark: | :white_check_mark: |
| 3.1 | **does not contain** | `land` | **1**, **2**, **4**, **6**, **7** | :x: | :x: |
| 3.2 | **does not contain** | `Gr` | **1**, **2**, **3**, **6**, **7** | :x: | :x: |
| 3.3 | **does not contain** | `Ö` | **1**, **2**, **3**, **5**, **7** | :x: | :x: |
| 3.4 | **does not contain** | `ö` | **1**, **2**, **3**, **5**, **7** | :x: | :x: |
| 3.5 | **does not contain** | `&` | **1**, **3**, **4**, **5**, **6**, **7** | :x: | :x: |
| 3.6 | **does not contain** | `en & Herz` | **1**, **3**, **4**, **5**, **6**, **7** | :x: | :x: |
| 3.7 | **does not contain** | `^G` | **1**, **2**, **3**, **6**, **7** | :x: | :x: |
| 3.8 | **does not contain** | `l$` | **1**, **2**, **3**, **6**, **7** |:x: | :x: |


<sup>
<strong>*</strong> Works when using autocomplete suggestions <i>/</i> Doesn't work when typing manually.
<br/><br/>
<strong>DF</strong> = Datasource Filtering
<i>/</i>
<strong>PF</strong> = Publish Filtering
</sup>

