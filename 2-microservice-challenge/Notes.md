# Data management and Communication Betwen Services is the Biggest Challenge in Microservices.
# One Micro Service Cannot Communicate with the Database of Another MicroService.

# We Need to Follow the Database Per Service Pattern 

# There are 2 Ways to Communicate between Microservices 
  *Sync -- Services Communicate with each other Using Direct Request. 
        ## Advantages
          1. Easy to Understand
          2. Some Services don't need DB, there Requests Can be  Fullfilled by Comminicating with other MS.

        ## Limitations
           1. Has Dependency Between Services 
           2. If Any Inter-Service Request Fails, the Overall Request Fails 
           3. Request is Slow
  
  *Async --  Services Communicate with each other Using Events.
    
    ## Async Communication Has a 2 Ways of MS Communication
       1. Which is Similar to Similar to Sync but Using Event BUS.

       2. Which Creates a DB of What is Required to Fullfill the Request for Particaular Feature MS with the Help of Event BUS i.e Whenever a Service Communicates to a DB it Also Emits Event Simutaneously to Event Bus Which Communicates to Other Services Which are Interested in that Event.
              ## Advantages 
                 1. There is No Dependency On Other Services.
                 2. Request is Very Fast.

             ## Limitations 
                1. Data Duplication, Extra DB Charge.
                2. Harder to Understand.



