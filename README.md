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
5) Define a parameter inside template file using <%= %> tag.<br/>
       Example:  \<Envelope\><br/>
                      \<body\><br/>
                       <input><%= input_field %></input><br/>
                      </body> <br/>
                 </Envelope><br/>
6) Create an instace of SOAPService into your working ruby file.<br/>
       Example: soap_client = SOAPService.new<br/>
7) Call execute method using web service name defined in service_config.yml file and parameters to be replaced from template xml file.<br/>
       Example: response = soap_client.execute('My_Soap_Service', {'input_field' => 'value'})<br/>
