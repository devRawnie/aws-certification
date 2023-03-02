# Monitoring

> Observing systems, collecting metrics and using the collected data to make decisions

## AWS Cloudwatch

- Tracks and Stores `Metrics`
- `Metrics` : Variables tied to your resources

### AWS Cloudwatch alarm

- Create a metric
- Set a threshold
- Alarm will trigger when value of the metric passes the set threshold

- Integrates with `SNS` to send a notification to the immediate respondent
- Reduce Mean Time to Resolution `MTTR`
- Improve Total Cost of Ownership `TCO`

## AWS Cloudtrail

- API Auditing Tool
- Every request to AWS gets logged in the CloudTrail Engine
  - Who made the request
  - When the request was made
  - How the request was made (SDK/CLI/CONSOLE)
  - What was the response

## AWS Trusted Advisor

- Evaluates resources in the AWS Account across 5 metrics
  1. Cost optimization
  2. Performance
  3. Security
  4. Fault Tolerance
  5. Service Limits

- Provides Real time recommendations in accordance with AWS Best practices
- 
