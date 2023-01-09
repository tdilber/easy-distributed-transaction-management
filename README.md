# Easy Distributed Transaction Management
DTM using with gRPC. 

Distributed Management Problems: 



My Model: 

- Check Preiodicly

- Delete Topics Periodicly

delete after sure all previous transactions completed  
for specific name CHECKING_NAME

1. delete first type:EQUAL:HEAD, sequence:LESS_OR_EQUAL:maxCheckingId, name:EQUAL:CHECKING_NAME  (make sure to deleting maybe u should implement transactional response) 
2. send delete transaction other 

BaseTransactionEntity:
- id
- name 
- sequence
- type (HEAD, MID, TAIL)
- nextTopics (json or json array maybe) 
(optionals)
- currentSequence
- sequenceLenght

contraints 
unique [or identity] (id)
unique (name, sequance)


Distributed Management Solution Reaction: 
