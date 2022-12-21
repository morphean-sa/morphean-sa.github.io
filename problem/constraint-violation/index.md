# Problem 

Work inherited from https://github.com/zalando/problem-spring-web.

## Constraint Violation

A problem that indicates a syntactically correct, yet semantically illegal request. It’s not meant to be used for 
end-user input validation, but for client developer convenience. Any constraint violation problem happening in 
production should be considered a bug.

```
{
    "type": "https://zalando.github.io/problem/constraint-violation",
    "title": "Constraint Violation",
    "status": 400,
    "violations": [
        {
            "field": "billing_address.first_name",
            "message": "may not be empty"
        },
        {
            "field": "groups",
            "message": "must not contain multiple different delivery addresses"
        },
        {
            "field": "groups[0].delivery_options.delivery_service",
            "message": "not supported"
        }
    ]
}
```
