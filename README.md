LogicApp is built to process ADT HL7 message and generate JSON Output
assuming thet end users send only ADT A01 HL7 messages through Http post request
LogicApp is invoked to by receiving raw HL7 message as input, process it through DecodeHL7 action and generate ADT Body xml & Message Header xml messages
Compose action is used to prepare output JSON message as per end users requirement
Send the JSON Output as Http response

  
