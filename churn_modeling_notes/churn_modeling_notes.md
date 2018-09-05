## The Challenge
There is no magic bullet for churn modeling. Every domain can be different and require different techniques. It can be hard to even identify what "churn" really is. For example, are customers who are cancelling and renewing often churning?

## Lift
Say you've identified churners, and have an answer in the form of a step discount to incentive them to stay. What if it's monetarily infeasible to offer this discount to every customer our model says is at risk of churning? In that case, having high precision becomes an important factor of our model's performance.

## Types of Churn
Very broadly, churn can be though of fitting into 4 general buckets:
* Contractual
    * Customers make purchases at discrete intervals
    * Cancellation event is observed and recorded
* Non-contractual
    * Customers are free to buy (or not) at any time
    * Churn event may not be, or never is, explicitly observed
Voluntary
* Customers make the choice to leave
* Involuntary
    * Customers are forced to leave due to circumstances outside of their control
    * Examples: Moving out of service, credit card expiration.

It's important to note that these groups are not mutually exclusive: involuntary churn can happen in contractual and none contractual situations, and they can have overlapping difficulties. So much of the literature in churn modeling focuses on Voluntary Churn specifically because it can be very difficult to figure out the root cause for customer's churn in that scenario.


## Metrics
Thinking about the scope of the problem and what _exactly_ we are trying to optimize will inform what the metric should be. For example, if the cost of retention is high (like offering steep discounts) then the precision would likely be the metric that mattered most to reduce the false-positive rate. In general, if you solution could become it's own problem, then precision should be a factor in decision making. 