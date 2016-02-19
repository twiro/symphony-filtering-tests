# Checkbox Field


## Available Filters

1. **is**


## Sample Data

1. `Yes`
2. `No`
3. `Yes`


## Tests

###### Performed with Symphony CMS 2.6.5

| Nr. | Filter | Value | Expected Result | DF | PF |
| :--- | :--- | :--- | --- | --- | --- |
| 1.1 | **is** | `Yes` | **1**, **3** | :white_check_mark: | :white_check_mark: |
| 1.1 | **is** | `yes` | **1**, **3** | :white_check_mark: | :white_check_mark: |
| 1.2 | **is** | `No` | **2** | :white_check_mark: | :white_check_mark: |
| 1.3 | **is** | `Yes, no` | **1**, **2**, **3** | :white_check_mark: | :white_check_mark: |


<sup>
<strong>DF</strong> = Datasource Filtering
<i>/</i>
<strong>PF</strong> = Publish Filtering
</sup>
