# Summary    
This workflow receives an HTTP POST request containing an HL7 message, then:  
  
- Decodes the HL7 payload  
- Checks the message type  
- Only allows ADT messages  
- Extracts key patient, visit, and message header details from the HL7 content  
- Returns the parsed data in a structured JSON response  
  
If the message type is not ADT, it returns a 400 error. If decoding or processing fails, it returns a 500 error.  
  
In short, its purpose is to validate and transform incoming HL7 ADT messages into a cleaner JSON format. 
