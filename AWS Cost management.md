- Add tagging to all projects to be able to have cost view by project
- Add tagging to useless files to mark them for deletion
	- erg-lifecycle=delete7days ?
	- erg-lifecycle=delete30days


## EC2 instance review
us-east-2
nginx proxy  ip-10-133-1-199.us-east-2.compute.internal

## us-east-1
10.127.27.110 databricks-imp - offline processor for databricks (chronicles to json)
Machien is overkill. Costs 676$ a month, only using ~11% for one 3h burst per day.
Turns out it is memory limited because it loads whole files at once, so we need enough memory