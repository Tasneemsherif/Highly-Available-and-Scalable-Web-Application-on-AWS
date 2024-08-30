# Highly Available and Scalable Web Application on AWS

## Problem Definition
The admissions department at University has been experiencing significant issues with their student records web application during peak admissions periods. The application becomes slow or unavailable due to the high number of concurrent users, resulting in a poor user experience. The existing on-premise infrastructure lacks the necessary scalability, high availability, and load balancing capabilities to handle the increased load, leading to potential data loss, reduced accessibility, and user dissatisfaction.

## Solution
To address these challenges, a proof of concept (POC) was developed to host the student records web application on AWS Cloud, leveraging its robust services to enhance performance, scalability, and availability. The solution involves the following key components:

1. **Architecture Design:** A scalable and secure architecture was designed using AWS services, including EC2 for compute resources, RDS for managed relational databases, and VPC for networking.

2. **Load Balancing and Auto Scaling:** An Application Load Balancer (ALB) was implemented to distribute traffic across multiple web servers, ensuring no single server is overloaded. Additionally, EC2 Auto Scaling was configured to automatically adjust the number of instances based on traffic demands, maintaining optimal performance during peak periods.

3. **High Availability:** The application was deployed across multiple Availability Zones to ensure high availability. In case of an instance failure, traffic is automatically rerouted to healthy instances, minimizing downtime.

4. **Security:** The application was secured using AWS best practices, including restricting database access to the web servers, securing web server access, and using AWS Secrets Manager to manage database credentials securely.

5. **Cost Optimization:** The architecture was designed with cost-efficiency in mind, using the AWS Pricing Calculator to estimate and minimize costs while ensuring all performance and security requirements were met.


## Project Phases
The project is divided into four key phases:

### Phase 1: Planning the Design and Cost Estimation
- **Architectural Diagram**:
 ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/Diagram.png)
- **Cost Estimation**:
  [attached pdf]([./filename.pdf](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/My%20Estimate%20-%20AWS%20Pricing%20Calculator.pdf))


### Phase 2: Creating a Basic Functional Web Application
- **Virtual Network Creation**: Set up a Virtual Private Cloud (VPC) with the necessary subnets and security groups.
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/VPC.png)
- **Virtual Machine Deployment**: Deploy an EC2 instance running Ubuntu to host the web application.
  ![Alt text](https://github.com/user-attachments/assets/8ec9cb4d-c0fb-41df-9dc9-e2e53d0190a7)
- **Testing Deployment**: Ensure the web application is accessible and functional.
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/EC2-test.png)

### Phase 3: Decoupling the Application Components
- **EC2 Configuration**: Update the network to support a separate database layer.
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/EC2-RDS.png)
- **Amazon RDS Setup**: Create and configure a MySQL database using Amazon RDS.
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/RDS.png)
- **Secrets Management**: Use AWS Secrets Manager to store and retrieve database credentials securely.
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/ASM.png)
- **Web Server Configuration**: Deploy the web application on a new EC2 instance, connecting it to the RDS database.
- **Database Migration**: Migrate data from the original database to the new RDS instance.
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/DB-migration-1.png)
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/DB-migration-2.png)
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/DB-migration-3.png)
- **Application Testing**: Perform functionality tests to ensure the application works with the new database setup.
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/RDS-modification.png)
  

### Phase 4: Implementing High Availability and Scalability
- **Application Load Balancer**: Deploy an Application Load Balancer to distribute traffic across multiple instances.
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/ALB-1.png)
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/ALB-2.png)

- **Auto Scaling**: Configure an Auto Scaling group to ensure the application can scale based on demand.
![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/ASG-1.png)

- **Accessing the Application**: Test the application through the load balancer’s endpoint.
- **Load Testing**: Perform load testing to monitor the application’s scaling capabilities.
  
  ![Alt text](https://github.com/Tasneemsherif/Highly-Available-and-Scalable-Web-Application-on-AWS/blob/main/final-test.png)


## AWS Services Used
- **Amazon EC2**: Virtual machine hosting.
- **Amazon RDS**: Managed relational database service.
- **Amazon VPC**: Network isolation.
- **AWS Secrets Manager**: Secure storage of credentials.
- **AWS Cloud9**: Integrated development environment for running CLI commands.
- **Application Load Balancer (ALB)**: Distributes incoming application traffic.
- **Auto Scaling**: Automatically adjusts the number of EC2 instances based on demand.

## Security Considerations
- **Network Security**: Configured security groups to restrict access to necessary ports.
- **Database Security**: RDS instances are hosted in private subnets, inaccessible from the internet.
- **Secrets Management**: Database credentials are securely stored and retrieved using AWS Secrets Manager.

## Cost Optimization
- **Cost Estimation**: Utilized the AWS Pricing Calculator to estimate the cost of the solution.
- **Auto Scaling**: Configured to scale instances dynamically to balance cost and performance.

## Conclusion
This project demonstrates the deployment of a highly available, scalable, and secure web application on AWS. The phased approach ensures that the architecture is robust, cost-effective, and meets the requirements of a real-world application scenario.

## Author
[Tasneem Sherif Ahmed](mailto:tasneemsherif45@gmail.com)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
