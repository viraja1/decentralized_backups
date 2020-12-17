# Decentralized Backups using Textile Buckets

1) Clone Textile Repo
   ```
   git clone https://github.com/textileio/textile.git
   cd textile
   ```
          
2) Ensure that make, docker and docker-compose are installed for your OS
          
3) Start Textile Bucket containers (Can be hosted remotely too)
   ```
   make buck-up
   ```

4) Download the buck command line utility 

   Download the buck_* command line utility for your OS from https://github.com/textileio/textile/releases and install it

5) Go to the directory which needs to be backed up

6) Initialize the bucket

   ```
   buck --api 127.0.0.1:3006 init --name={bucket_name} --private=true
   ```
   
   Replace {bucket_name} with the actual bucket name

7) Push the bucket contents

   ```
   buck --api 127.0.0.1:3006 push
   ```

8) Pull from an existing bucket

   ```
   buck --api 127.0.0.1:3006 init --name={bucket_name} --private=true --existing
   ```
   
   Replace {bucket_name} with the actual bucket name
   
          
**Note:** Above backup process can also be automated by writing a simple cron script
