# Military information: user wants to access their military information
**Last updated: February 8, 2023 -- added users that have military info**

For LOA3 users who sign in, go to the profile, and click into the military information section, they can view their service history if they have a Department of Defense (DoD) ID.

If they don't have a DoD ID, don't have a service history, or are a non-veteran, they'll see an alert instead of a service history.

This page isn’t editable.

## UX
### User has DoD ID
* A user lands on the military information page; they can see data points for all periods of service the VA knows about from their military record.
	* Branch of service
	* The month, day, and year they started with that branch
	* The month, day, and year they completed service with that branch.  
		* There are some instances where the end date will be blank.
* The page has an [additional info component](https://design.va.gov/components/additional-info) with information in case the military service information doesn’t look right.
*  [Desktop mockup](https://www.sketch.com/s/fc96664a-1c62-40ed-9fcd-90218c54e775/a/g0YO03a) 
*  [Mobile mockup](https://www.sketch.com/s/fc96664a-1c62-40ed-9fcd-90218c54e775/a/DPDA8Wk) 

### User does not have DoD ID
* If DEERS does not return a DoD ID the user will see an alert on the page telling them we don't have their military information.
* The additional info component is not displayed.
* Uses the [warning alert component](https://design.va.gov/components/alert#warning-alert) from the design system
*  [Desktop mockup](https://www.sketch.com/s/fc96664a-1c62-40ed-9fcd-90218c54e775/a/8yQObmR) 
*  [Mobile mockup](https://www.sketch.com/s/fc96664a-1c62-40ed-9fcd-90218c54e775/a/zxvZ4Le) 

### User does not have a service history
* If the user does not have a service history, the service history array will be empty. The user will see an alert on the page telling them we can't access their military information. _**Note:** A user can have a DoD ID but no military service._
* The additional info component is not displayed.
* Uses the [warning alert component](https://design.va.gov/components/alert#warning-alert) from the design system
*  [Desktop mockup](https://www.sketch.com/s/fc96664a-1c62-40ed-9fcd-90218c54e775/a/8yQObmR) 
*  [Mobile mockup](https://www.sketch.com/s/fc96664a-1c62-40ed-9fcd-90218c54e775/a/52vgV88) 

### User is not a Veteran
* If the user is confirmed to be a non-Veteran, they will see an informational alert on the page telling them they don't have any military information.
* The additional info component is not displayed.
* Uses the [warning alert component](https://design.va.gov/components/alert#warning-alert) from the design system
*  [Desktop mockup](https://www.sketch.com/s/fc96664a-1c62-40ed-9fcd-90218c54e775/a/VrJq5jr) 
*  [Mobile mockup](https://www.sketch.com/s/fc96664a-1c62-40ed-9fcd-90218c54e775/a/zxvZ4Le) 

View this [Slack thread](https://dsva.slack.com/archives/C909ZG2BB/p1670342254856829) for more information on the difference between these alerts. 

## Codes
N/A

## How to reproduce
### User has DoD ID
1. Go staging.va.gov/profile/military-information
2. Log in with users 41, 54, or 80 ([staging user info](https://github.com/department-of-veterans-affairs/va.gov-team-sensitive/blob/master/Administrative/vagov-users/mvi-staging-users.csv))

### User does not have DoD ID
1. Go staging.va.gov/profile/military-information
2. ???

### User does not have a service history
1. Go staging.va.gov/profile/military-information
2. Log in with vets.gov.user+111 ([staging user info](https://github.com/department-of-veterans-affairs/va.gov-team-sensitive/blob/master/Administrative/vagov-users/mvi-staging-users.csv))

### User is not a Veteran
1. Go staging.va.gov/profile/military-information
2. Log in with vets.gov.user+10 ([staging user info](https://github.com/department-of-veterans-affairs/va.gov-team-sensitive/blob/master/Administrative/vagov-users/mvi-staging-users.csv))
