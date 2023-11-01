# airflow_quickstart

1. Create an ec2 instance on AWS. Create key pair to connect to the instance and save it for later.
2. Connect to the ec2 instance using the ssh client, and change the permissions of the .pem file before connecting to the instance.

   <img width="601" alt="Screen Shot 2023-10-31 at 6 20 06 PM" src="https://github.com/bowtruckle30/airflow_quickstart/assets/25841184/6869a34b-900e-4aaf-8927-261dcba8f48f">

3. Execute the following commands after connecting to the instance:
<ul>
  <li>sudo apt-get update</li>
  <li>sudo apt install python3-pip</li>
  <li>sudo pip install apache-airflow</li>
  <li>sudo pip install pandas</li>
  <li>sudo pip install s3fs</li>
  <li>sudo pip install bs4</li>
  <li>sudo pip install awscli</li>
  </ul>
  
4. Create a directory called airflow on the ec2 instance using mkdir command and copy the fire_dags folder inside it
5. Don't forget to update the airflow.cfg file with the dags_folder path
6. On the AWS console, attach IAM role to the ec2 instance by creating a new role and adding ec2 access and s3 access permissions to the role.
7. Execute airflow standalone command on the ec2
8. Save the admin credentials displayed on the terminal console to login to the airflow server.
9. To access the airflow server, use the <Public IPv4 DNS of the ec2 instance>:8080 in the browser, and use admin credentials created in step 8. to login.
10. Run the fires_ca_dag on the airflow console
