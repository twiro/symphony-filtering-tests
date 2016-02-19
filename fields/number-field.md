# Number Field

- [Github Repo](https://github.com/symphonycms/numberfield)
- [Symphony Extensions](http://symphonyextensions.com/extensions/numberfield)


## Available Filters

1. **is**
2. **less than**
3. **equal to or less than**
4. **greater than**
5. **equal to or greater than**
6. **between**


## Sample Data

1. `-99.99`
2. `0`
3. `0.00001`
4. `0.99`
5. `99`
6. `827372.79`


## Tests

###### Performed with Symphony CMS 2.6.5 and Number Field 1.7.1

| Nr. | Filter | Value | Expected Result | DF | PF |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1.1 | **is** | `-99.99` | **1** | :white_check_mark: | :white_check_mark: |
| 1.2 | **is** | `0` | **2** | :white_check_mark: | :white_check_mark: |
| 1.3 | **is** | `0.99` | **4** | :white_check_mark: | :white_check_mark: |
| 1.4 | **is** | `0, 99` | **2**, **5** | :white_check_mark: | :white_check_mark: |
| 1.5 | **is** | `827372.79` | **6** | :white_check_mark: | :white_check_mark: |
| 2.1 | **less than** | `-100`  | – | :white_check_mark: | :white_check_mark: |
| 2.2 | **less than** | `0`  | **1** | :white_check_mark: | :white_check_mark: |
| 2.3 | **less than** | `1` | **1**, **2**, **3**, **4** | :white_check_mark: | :white_check_mark: |
| 2.3 | **less than** | `1000000` | **1**, **2**, **3**, **4**, **5**, **6** | :white_check_mark: | :white_check_mark: |
| 3.1 | **equal to or less than** | `-99`  | **1** | :white_check_mark: | :white_check_mark: |
| 3.2 | **equal to or less than** | `0`  | **1**, **2** | :white_check_mark: | :white_check_mark: |
| 3.3 | **equal to or less than** | `0.99` | **1**, **2**, **3**, **4** | :white_check_mark: | :white_check_mark: |
| 3.3 | **equal to or less than** | `827372.79` | **1**, **2**, **3**, **4**, **5**, **6** | :white_check_mark: | :white_check_mark: |
| 4.1 | **greater than** | `-99`  | **2**, **3**, **4**, **5**, **6** | :white_check_mark: | :white_check_mark: |
| 4.2 | **greater than** | `0`  | **3**, **4**, **5**, **6** | :white_check_mark: | :white_check_mark: |
| 4.3 | **greater than** | `.99` | **5**, **6** | :white_check_mark: | :white_check_mark: |
| 4.3 | **greater than** | `1000000` | – | :white_check_mark: | :white_check_mark: |
| 5.1 | **equal to or greater than** | `-99`  | **2**, **3**, **4**, **5**, **6** | :white_check_mark: | :white_check_mark: |
| 5.2 | **equal to or greater than** | `0`  | **2**, **3**, **4**, **5**, **6** | :white_check_mark: | :white_check_mark: |
| 5.3 | **equal to or greater than** | `.99` | **4**, **5**, **6** | :white_check_mark: | :white_check_mark: |
| 5.3 | **equal to or greater than** | `827372.79` | **6** | :white_check_mark: | :white_check_mark: |
| 6.1 | **between** | `-100 to 0`  | **1**, **2** | :white_check_mark: | :x: |
| 6.2 | **between** | `-99.99 to .99`  | **1**, **2**, **3**, **4** | :white_check_mark: | :x: |
| 6.3 | **between** | `0 to 1`  | **2**, **3**, **4** | :white_check_mark: | :x: |
| 6.3 | **between** | `1 to 1000000`  | **5**, **6** | :white_check_mark: | :x: |






<sup>
<strong>DF</strong> = Datasource Filtering
<i>/</i>
<strong>PF</strong> = Publish Filtering
</sup>