# Migrating Your Domain DNS Server From GoDaddy To AWS


>***Note**: The steps below are performed after you purchased your domain name from GoDaddy

Prerequisites:
1) Check out the DNS hosting charges for Route53 [here](https://aws.amazon.com/route53/pricing/)
2) Basic pricing is like below:
    1) $0.50 per hosted zone / month for the first 25 hosted zones
    2) $0.40 per million queries – first 1 Billion queries / month (for standard queries)

### On AWS
1) Login you your **AWS console**
2) Go to **Route 53** landing page
3) If you dont have any DNS hosted zone with AWS, click **Get started now** in the **DNS management** section
4) Click **Create hosted zone**
5) Click **Create hosted zone** again
6) You should see an new section show up to your right. Enter your domain name in the **Domain Name:** field
7) Click **Create**
8) Two types of records should populate, SOA and NS. We need to add these records to GoDaddy DNS

### On GoDaddy
9) Logn to your GoDaddy DNS account
10) Click the **drop-down** arrow nect to your account name
11) Click **manage domains**
12) Click on the **DNS drop-down** at the top
13) Click **manage zones**
14) Search and click on you **Domain Name**
15) 
