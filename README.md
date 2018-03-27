# Ruby_Codes
Ruby codes for several good stuff
To use SOAPService class , follow the steps below
1) Copy SOAPService class file into a ruby file under working directory.
2) Include SOAPServcie class to your working ruby file.
3) Create service_config.yml file under working directory.
4) Define soap properties in service_config.yml file:
     a) Example 1, in case of no wsdl.
          My_Soap_Service: 
             namespace: 'http://xyzSoapServiceNamespace' <br/>
             endpoint:   'soap_end_point'
             action:      'Soap action here'
             basic_auth:   ['usr', 'pass']
             template:  'location of request template relative to working directory'
     b) Example 1, in case of wsdl.   
          My_Soap_Service: 
             namespace: 'http://xyz_WSD__LINK'
             template:  'location of request template relative to working directory'
