# appconfig_notes

What isAppConfig 
    Quickly deploy application configurations
    Influence the behavior of your application
    
 Support Applications hosted 
     EC2
     Lambda
     Containers
     Mobile applications
     IoT devices
  
 Helps simplify 
    Configure
    Validate
    Deploy and Monitor
    
 Use Cases 
    Application tuning
    Feature toggle
    Allow list
    Operational issues
    
 Benefits 
   Reduce errors in configuration changes
       reduce downtime through code validation
             syntactic validation : JSON schema
             semantic validation  : call on lambda function to run configuration before you deploy
   Deploy changes across a set of targets quickly
       supports configuration stored in Systems Manager Parameter Store , SSM documents and S3
       targets dont need to be confiured with SSM agent or Instance Profile (can work with unmanaged instances)
   Update appliation without interruptions
       deploy comfiguration changes at runtime
       uses deployment strategies
       

HOW IT WORKS 
  Application  : Own application 
  Environment  : Dev or Prod
  Configuration profile :   access data in its stored location
          configuration data in YAML , JSON or other format stored in hosted configuration store
          configuration data stored as objects in S3 bucket
          Pipeline stored in AWS CodePipeline
          Secret stored in AWS secret manager
          security string in parameter store
          configuration data in SSM document stored in SSM document store

