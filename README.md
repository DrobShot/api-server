# api-server
This repo contain the python script and the "requirements.txt" file for the virtual environment that contains all the necessary dependency. The server framework we are going to use is Flask with RESTful api together with MySQL database. We might also include GraphQL support in the future. 

For handling all the request we are going to use Nginx as the reverse proxy and load balancing. Provided by Aruba Cloud. OS = SOME LINUX DISTRO
ALL THE OTHER SERVER ARE BEHIND NGINIX AND NOT SECURED BY SSL.
Apart from Apache all the other server must only respond to request made by Ngnix server ip or other backend server ip.
For file storage we are using Apache server (for serving the content through https) and NFS server (for reaching and uploading content from other backend server). Self Hosted. OS = UBUNTU LTS
For storing information we are using MySQL. Provided by Aruba Cloud. OS = SOME LINUX DISTRO
For API we are using probably two nodes. Self hosted. OS = DEBIAN
For AI processing we are using probably a two or three Nvidia jetson nano board. Self hosted. OS = UBUNTU LTS


All api endpoint must be properly commented (in English) and exported with postman, in order to let the "client side" team understand how the backend work, without the need to reed all the script.
When a major version of the API is created upload it with {VERSION_NUMBER}---main, and contact the server admin for rollup. 
We are going to maintain in parallel the latest two version of the api, in order to let the "client side" team and the user, time to update the client app.
