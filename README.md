# Migrating Your Domain DNS Server From GoDaddy To AWS


>***Note**: The steps below are performed after you purchased your domain name from GoDaddy

###Prerequisites:
- Check out the DNS hosting charges for Route53 [here](https://aws.amazon.com/route53/pricing/)
- Basic pricing is like below:
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
13) Click **Manage Zones**
14) Search and click on you **Domain Name**
15) Scroll down to the **Nameservers** section and click **Change**
![Original Nameservers](https://github.com/hadriane/migrating_dns_from_godaddy_to_aws/blob/master/images/original-nameservers.png)
16) Click **Enter my own nameservers (advanced)**
17) Twice cliick **Add Nameservers**
18) Enter the 4 NS records (*without the . at the end of the record*) you got from AWS Route 53
19) Click **Save**
20) Wait a minute or two then refresh the page
21) Scroll down to the **Nameservers** section and you would see the changes has taken effect
![Changed Nameservers](https://github.com/hadriane/migrating_dns_from_godaddy_to_aws/blob/master/images/changed-nameservers.png)

