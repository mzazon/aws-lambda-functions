This Lambda function will take input of the following via Env Variables

NAMES
MIN_SIZE
MAX_SIZE
DESIRED_CAPACITY

NAMES is a space separated list of autoscaling groups 
MIN_SIZE, MAX_SIZE, DESIRED_CAPACITY are the parameters to set the autoscaling group upon launch

This lambda function runs and checks whether the ASGs via (NAMES) has a value of 0,0,0 and if so, applies the values
specified in MIN_SIZE, MAX_SIZE, DESIRED_CAPACITY.

If the ASG is already running it will set each value to 0 to stop all instances in the ASG.

This single function can be scheduled to run in the morning and evening for example to save costs.