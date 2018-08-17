# app image
FROM orb1t/meissa-base

ENV MEISSA_TEST_SERVER_URL "http://localhost:5000"

ENV MEISSA_TEST_SERVER_ADDR "localhost"
ENV MEISSA_TEST_SERVER_PORT="5000"

ENV MEISSA_TEST_AGENT_TAG "Agent1"
ENV MEISSA_TEST_AGENT_RUN_TIMEOUT "30"


RUN mkdir "c:\Resources"
RUN mkdir "C:\Users\ContainerAdministrator\AppData\Resources"

# RUN mkdir C:\_GHPReporter_SpecFlow_Report
# RUN mkdir C:\_GHPReporter_NUnit_Report
# RUN mkdir C:\_GHPReporter_Core_Report


ADD "Resources/" "/Resources"
ADD "Resources/" "C:\Users\ContainerAdministrator\AppData\Resources"
ADD "environments.xml" "/environments.xml"
ADD "environments.xml" "C:\Users\ContainerAdministrator\AppData\environments.xml"

WORKDIR "/apps/meissa"

CMD meissa.exe testAgent --testServerUrl="http://"%MEISSA_TEST_SERVER_ADDR%:%MEISSA_TEST_SERVER_PORT% --testAgentTag=%MEISSA_TEST_AGENT_TAG% --testAgentRunTimeout=%MEISSA_TEST_AGENT_RUN_TIMEOUT% --testTechnology="NUnit"