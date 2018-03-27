# Ruby_Codes
Ruby codes for several good stuff<br/>
To use SOAPService class , follow the steps below<br/>
1) Copy SOAPService class file into a ruby file under working directory.<br/>
2) Include SOAPServcie class to your working ruby file.<br/>
3) Create service_config.yml file under working directory.<br/>
4) Define soap properties in service_config.yml file:<br/>
     a) Example 1, in case of no wsdl.<br/>
          My_Soap_Service: <br/>
             namespace: 'http://xyzSoapServiceNamespace' <br/>
             endpoint:   'soap_end_point'<br/>
             action:      'Soap action here'<br/>
             basic_auth:   ['usr', 'pass']<br/>
             template:  'location of request template relative to working directory'<br/>
     b) Example 1, in case of wsdl.   <br/>
          My_Soap_Service: <br/>
             namespace: 'http://xyz_WSD__LINK'<br/>
             template:  'location of request template relative to working directory'<br/>
