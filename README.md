# SOEN_6611
Software Measurement - SOEN 6611
Team K:
Heer Oza	,
Meet Maniar	,
Shriyans Athalye	

This project consist of measuring software quality attributes and relating them with metric.
The selected projects are
1) JFreeChart - https://github.com/jfree/jfreechart
2) Apache Commons io - https://github.com/apache/commons-io
3) Apache Commons codec - https://github.com/apache/commons-codec

These are open source maven projects easily downloadable from the provided link. For this project, 5 version of each mentioned in the above list were selected and data collected for same.Different metrics were distributed over different folders as per team members convenience.
Folder MI contains maintainability index of selected projects calculated using formula. The data also contains cyclomatic complexity as it was required for MI calculation
Folder Defect Density contains the defects measured from JIRA 
Screenshot of Mutation testing were calculated using tool for all the selected projects version
For code coverage in some of the projects, additional changes were necessary to generate coverage report
In version 1,2,3 of Commons_io and commons_codec additional dependencies in pom file needs to be added.
  <dependency>
        <groupId>org.openclover</groupId>
        <artifactId>clover-maven-plugin</artifactId>
        <version>4.3.1</version>
        <type>maven-plugin</type>
    </dependency>
After writing this, Intellij has to be restared and then run all test with coverage option needs to be selected
For calculating cyclomatic complexity, metricsreloaded plugin is used in Intellij. This can be done by selecting Help from main toolbar and then selecting first option FindAction.
Then Search bar would appear wherein Calculate metrics need to be typed and select from below options
For Complexity- Complexity metric needs to be selected.
Defect density from JIRA and GitHub Issue tracker.
JIRA link for Issues
Apache CommonsCodec - https://issues.apache.org/jira/projects/CODEC/issues/CODEC-134?filter=allopenissues
Apache CommonsIO - https://issues.apache.org/jira/projects/IO/issues/IO-552?filter=allopenissues
Under advanced filter, following query needs to be used to get bug report for above projects
project = CODEC AND issuetype = Bug AND resolution = Unresolved ORDER BY priority DESC, updated DESC (for CODEC)
project = IO AND issuetype = Bug AND resolution = Unresolved ORDER BY priority DESC, updated DESC( for IO)
For JFreechart, it is collected through GitHub Issue tab on home page of project done through calculating the count from the label reported as "Bug/Defects/Issue"

