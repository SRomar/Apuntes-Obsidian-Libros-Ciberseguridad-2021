In several cases where a combination of flaws is present, it can even result in a solution that is *less* secure than a normal login based on username and password.

An application with multistage login:
- may assume that a user who accesses stage three must have cleared stage one and two.
- may trust some of the data being processed at stage two because this was validated at stage one. 
- may assume that the same user identity is used to complete each stage.

