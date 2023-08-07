#SSM Secret

### Parameters Policies:

- Allow to assign a TTL to parameter to force updating or deleting sensitive data.
- Can assign multiple policies at a time

Policy Samples:

```json
//Expiration Policy
{
    "Type": "Expiration",
    "Version": "1.0",
    "Attributes": {
        "Timestamp": "2018-12-02T21:34:33.000Z"
    }
}

//ExpirationNotification
{
    "Type": "ExpirationNotification",
    "Version": "1.0",
    "Attributes": {
        "Before": "15",
        "Unit": "Days"
    }
}
```

Note: If using Lambda to get parameters from AWS PS. IAM that attached to Lambda must be attached permission such as **GetParameters**,...

### Limitation

|                                                         | Standard           | Advanced                               |
| ------------------------------------------------------- | ------------------ | -------------------------------------- |
| Total number of parameters (per AWS account adn region) | 10.000             | 100.000                                |
| Maximum size of a parameter value                       | 4KB                | 8KB                                    |
| Parameter policies available                            | No                 | Yes                                    |
| Cost                                                    | No addition Charge | Charges apply                          |
| Storage Pricing                                         | Free               | $0.05 per advanced parameter per month |
