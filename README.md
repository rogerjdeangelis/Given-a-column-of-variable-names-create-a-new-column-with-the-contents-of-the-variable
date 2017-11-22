# Given-a-column-of-variable-names-create-a-new-column-with-the-contents-of-the-variable
Assign value using variable containing names of variables (vvaluex). Given a column of variable names create a new column with the contents of the variable.

    ```  Given a column of variable names create a new column with the contents of the variable.                                                                      ```
    ```  Assign value using variable containing names of variables (vvaluex).                                                                                         ```
    ```                                                                                                                                                               ```
    ```  see                                                                                                                                                          ```
    ```  https://goo.gl/6SNnTJ                                                                                                                                        ```
    ```  https://communities.sas.com/t5/Base-SAS-Programming/Assign-value-using-variable-containing-names-of-variables/m-p/415510                                     ```
    ```                                                                                                                                                               ```
    ```                                                                                                                                                               ```
    ```  INPUT                                                                                                                                                        ```
    ```  =====                                                                                                                                                        ```
    ```                                                                                                                                                               ```
    ```    WORK.HAVE total obs=4       |    RULES (want additional variable VAR                                                                                       ```
    ```                                |                                                                                                                              ```
    ```     Obs    A    B    C    V    |   VAR                                                                                                                        ```
    ```                                |                                                                                                                              ```
    ```      1     1    2    3    A    |    1      contents of A                                                                                                      ```
    ```      2     1    2    3    B    |    2      contents of B                                                                                                      ```
    ```      3     4    5    6    A    |    4      contents of A                                                                                                      ```
    ```      4     4    5    6    C    |    6      contents of A                                                                                                      ```
    ```                                |                                                                                                                              ```
    ```                                                                                                                                                               ```
    ```  PROCESS                                                                                                                                                      ```
    ```  =======                                                                                                                                                      ```
    ```     data want;                                                                                                                                                ```
    ```       set have;                                                                                                                                               ```
    ```       var=vvaluex(v);                                                                                                                                         ```
    ```     run;quit;                                                                                                                                                 ```
    ```                                                                                                                                                               ```
    ```  OUTPUT                                                                                                                                                       ```
    ```  ======                                                                                                                                                       ```
    ```                                                                                                                                                               ```
    ```     WORK.WANT total obs=4                                                                                                                                     ```
    ```                                                                                                                                                               ```
    ```      A    B    C    V   VAR                                                                                                                                   ```
    ```                                                                                                                                                               ```
    ```      1    2    3    A    1                                                                                                                                    ```
    ```      1    2    3    B    2                                                                                                                                    ```
    ```      4    5    6    A    4                                                                                                                                    ```
    ```      4    5    6    C    6                                                                                                                                    ```
    ```                                                                                                                                                               ```
    ```  *                _               _       _                                                                                                                   ```
    ```   _ __ ___   __ _| | _____     __| | __ _| |_ __ _                                                                                                            ```
    ```  | '_ ` _ \ / _` | |/ / _ \   / _` |/ _` | __/ _` |                                                                                                           ```
    ```  | | | | | | (_| |   <  __/  | (_| | (_| | || (_| |                                                                                                           ```
    ```  |_| |_| |_|\__,_|_|\_\___|   \__,_|\__,_|\__\__,_|                                                                                                           ```
    ```                                                                                                                                                               ```
    ```  ;                                                                                                                                                            ```
    ```                                                                                                                                                               ```
    ```  data have;                                                                                                                                                   ```
    ```  input a b c v$ r;                                                                                                                                            ```
    ```  cards4;                                                                                                                                                      ```
    ```  1 2 3 A 1                                                                                                                                                    ```
    ```  1 2 3 B 2                                                                                                                                                    ```
    ```  4 5 6 A 4                                                                                                                                                    ```
    ```  4 5 6 C 6                                                                                                                                                    ```
    ```  ;;;;                                                                                                                                                         ```
    ```  run;quit;                                                                                                                                                    ```
    ```                                                                                                                                                               ```
    ```  *          _       _   _                                                                                                                                     ```
    ```   ___  ___ | |_   _| |_(_) ___  _ __                                                                                                                          ```
    ```  / __|/ _ \| | | | | __| |/ _ \| '_ \                                                                                                                         ```
    ```  \__ \ (_) | | |_| | |_| | (_) | | | |                                                                                                                        ```
    ```  |___/\___/|_|\__,_|\__|_|\___/|_| |_|                                                                                                                        ```
    ```                                                                                                                                                               ```
    ```  ;                                                                                                                                                            ```
    ```                                                                                                                                                               ```
    ```  data want;                                                                                                                                                   ```
    ```    set have;                                                                                                                                                  ```
    ```    var=vvaluex(v);                                                                                                                                            ```
    ```  run;quit;                                                                                                                                                    ```
    ```                                                                                                                                                               ```

