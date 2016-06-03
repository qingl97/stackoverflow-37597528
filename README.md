Demo repo for stackoverflow question 
http://stackoverflow.com/questions/37597528/execution-order-of-maven-profile-task-and-goal-differs-on-version-3-3-9-and-3-2

Run command ```mvn clean validate``` using maven verison :

 * 3.2.5

   ```
   [DEBUG]   (s) resources = [Resource {targetPath: null, filtering: false, FileSet {directory: C:\Users\liang\workspace\stackoverflow-37597528\src\main\resources, PatternSet [includes: {}, excludes: {}]}}]
   ```
   Then both common-resource and profile-resource is copied in that target.
 * 3.3.9
 
   ```
   [DEBUG]   (s) resources = [Resource {targetPath: null, filtering: true, FileSet {directory: src/main/resources, PatternSet [includes: {}, excludes: {conf/}]}}]
   ```
   Only common-resource is copied.
