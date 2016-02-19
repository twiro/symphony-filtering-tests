# Author Field


## Available Filters

1. **is**
2. **contains**
3. **does not contain**


## Sample Data

1. `Friedrich` `Schiller` / `friedrich.schiller`
2. `Johann Wolfgang` `von Goethe` / `Goethe`
3. `Heinrich` `Heine` / `heinrich.heine`
4. `Heinrich` `Böll` / `heinrich.boell`
5. `Eduard` `Mörike` / `eduard.moerike`

<sup>
<strong>Schema:</strong> First Name, Last Name / Username
</sup>


## Tests

###### Performed with Symphony CMS 2.6.5

| Nr. | Filter | Value | Expected Result | DF | PF |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1.1 | **is** | `Friedrich` | **-** | :white_check_mark: | :white_check_mark: |
| 1.2 | **is** | `Goethe` | **2** | :white_check_mark: | :white_check_mark: |
| 1.3 | **is** | `Heinrich Heine` | **3** | :white_check_mark: | :white_check_mark: |
| 1.4 | **is** | `eduard.moerike` | **5** | :white_check_mark: | :white_check_mark: |
| 1.5 | **is** | `Friedrich Schiller, Goethe` | **1**,  **2** | :white_check_mark: | :white_check_mark: |
| 1.6 | **is** | `1` | **1** | :white_check_mark: | :white_check_mark: |
| 2.1 | **contains** | `Heinrich`  | **3**, **4** | :white_check_mark: | :white_check_mark: |
| 2.2 | **contains** | `o` | **2**, **4**, **5** | :white_check_mark: | :white_check_mark: |
| 2.3 | **contains** | `ö` | **4**, **5** | :white_check_mark: | :white_check_mark: |
| 2.4 | **contains** | `2` | **2** | :white_check_mark: | :white_check_mark: |
| 3.1 | **does not contain** | `Heinrich`  | **1**, **2**, **5** | :x: | :x: |
| 3.2 | **does not contain** | `o` | **1**, **3** | :x: | :x: |
| 3.3 | **does not contain** | `ö` | **1**, **2**, **3** | :x: | :x: |
| 3.4 | **does not contain** | `2` | **1**, **3**, **4**, **5** | :x: | :x: |

<sup>
<strong>DF</strong> = Datasource Filtering
<i>/</i>
<strong>PF</strong> = Publish Filtering
</sup>

