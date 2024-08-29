# Highly-Available-and-Scalable-Web-Application-on-AWS

## Project Overview
This project focuses on building a highly available, scalable, and secure web application hosted on the AWS Cloud. The application is designed to meet best practices outlined in the AWS Well-Architected Framework, with a focus on load balancing, scalability, high availability, and cost optimization.

## Project Phases
The project is divided into four key phases:

### Phase 1: Planning the Design and Cost Estimation
- **Architectural Diagram**: Create a visual representation of the AWS services used and their interactions.
- **Cost Estimation**: Estimate the cost of running the application using the AWS Pricing Calculator.

### Phase 2: Creating a Basic Functional Web Application
- **Virtual Network Creation**: Set up a Virtual Private Cloud (VPC) with the necessary subnets and security groups.
- **Virtual Machine Deployment**: Deploy an EC2 instance running Ubuntu to host the web application.
- **Testing Deployment**: Ensure the web application is accessible and functional.

### Phase 3: Decoupling the Application Components
- **VPC Configuration**: Update the network to support a separate database layer.
- **Amazon RDS Setup**: Create and configure a MySQL database using Amazon RDS.
- **Secrets Management**: Use AWS Secrets Manager to securely store and retrieve database credentials.
- **Web Server Configuration**: Deploy the web application on a new EC2 instance, connecting it to the RDS database.
- **Database Migration**: Migrate data from the original database to the new RDS instance.
- **Application Testing**: Perform functionality tests to ensure the application works with the new database setup.

### Phase 4: Implementing High Availability and Scalability
- **Application Load Balancer**: Deploy an Application Load Balancer to distribute traffic across multiple instances.
- **Auto Scaling**: Configure an Auto Scaling group to ensure the application can scale based on demand.
- **Accessing the Application**: Test the application through the load balancer’s endpoint.
- **Load Testing**: Perform load testing to monitor the application’s scaling capabilities.

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
[Tasneem Sherif Ahmed](mailto:your-email@example.com)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
