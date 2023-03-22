# ElbAutoscaling

Project Funcionalities:

- Create EC2 virtual machines;
- Prepare an elastic infrastructure;
- Test your elastic infrastructure.

## Test Instructions:

```
## - Download and install Locust 
brew install locust

## - Confirm Locust installation
locust -V

## - Execute Locust
locust -f charge.py

## - Open your browser
get your external IP and paste in your browser, followed by the port configured in locust (stardard is 8089)
> Ex.: http://192.168.101.6:8089/
The Locust innitial page will open.

## - Test your application
Copy the DNS name from your Load Balancer and paste in your browser, followed by the port configured in application (standard is 8000)
> Ex.: Poc-ELB-646483222.us-east-1.elb.amazonaws.com:8000

We have 3 fields:
- Number of users;
> This refers to the number of simultaneous users that will be used for the test;
- Spawn rate;
> This refers to the number of users that will be added to the test per second;
- Host.
> Here you can paste the red line link of your application's innitial page (Please remove quotation marks and the last slash)
> Ex.: http://poc-elb-646483222.us-east-1.elb.amazonaws.com:8000/clientes

After filling the fields press "Start swarming"
- You can follow the requests through the 'Charts' tab.
- You can change the values through the edit button at the top of the page.

```
