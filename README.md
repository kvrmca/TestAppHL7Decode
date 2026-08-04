# Summary    
This workflow receives an HTTP POST request containing an HL7 message, then:  
  
- Decodes the HL7 payload  
- Checks the message type  
- Only allows ADT messages  
- Extracts key patient, visit, and message header details from the HL7 content  
- Returns the parsed data in a structured JSON response  
  
If the message type is not ADT, it returns a 400 error. If decoding or processing fails, it returns a 500 error.  
  
In short, its purpose is to validate and transform incoming HL7 ADT messages into a cleaner JSON format. 

sample HL7 message

MSH|^~\&|EPIC|HOSPITAL|LAB|FACILITY|20260725120000||ADT^A01|MSG00001|P|2.51 <br>
PID|1||123456^^^MRN||DOE^JOHN||19800101|M|||123 MAIN ST||55512345673 <br>
PV1|1|I|ER||||12345^SMITH^ROBERT <br>
