# workshop-uncool-mlops

**NOTE FROM ME**
The workflow step "Create a P.R. with CML" is broken.
<details>
  <summary>Full error output</summary>
  ```
{"data":{"enablePullRequestAutoMerge":null},"errors":[{"locations":[{"column":13,"line":8}],"message":"[\"Pull request Pull request is in clean status\"]","path":["enablePullRequestAutoMerge"],"type":"UNPROCESSABLE"}],"headers":{"access-control-allow-origin":"*","access-control-expose-headers":"ETag, Link, Location, Retry-After, X-GitHub-OTP, X-RateLimit-Limit, X-RateLimit-Remaining, X-RateLimit-Used, X-RateLimit-Resource, X-RateLimit-Reset, X-OAuth-Scopes, X-Accepted-OAuth-Scopes, X-Poll-Interval, X-GitHub-Media-Type, X-GitHub-SSO, X-GitHub-Request-Id, Deprecation, Sunset","connection":"close","content-encoding":"gzip","content-security-policy":"default-src 'none'","content-type":"application/json; charset=utf-8","date":"Thu, 14 Apr 2022 09:58:38 GMT","referrer-policy":"origin-when-cross-origin, strict-origin-when-cross-origin","server":"GitHub.com","strict-transport-security":"max-age=31536000; includeSubdomains; preload","transfer-encoding":"chunked","vary":"Accept-Encoding, Accept, X-Requested-With","x-content-type-options":"nosniff","x-frame-options":"deny","x-github-media-type":"github.v3; format=json","x-github-request-id":"07C2:5CD5:11594E8:326474F:6257F04D","x-ratelimit-limit":"1000","x-ratelimit-remaining":"997","x-ratelimit-reset":"1649931312","x-ratelimit-resource":"graphql","x-ratelimit-used":"3","x-xss-protection":"0"},"level":"error","message":"Request failed due to following response errors:\n - [\"Pull request Pull request is in clean status\"]","name":"GraphqlResponseError","request":{"query":"\n          mutation autoMerge(\n            $pullRequestId: ID!\n            $mergeMethod: PullRequestMergeMethod\n            $commitHeadline: String\n            $commitBody: String\n          ) {\n            enablePullRequestAutoMerge(\n              input: {\n                pullRequestId: $pullRequestId\n                mergeMethod: $mergeMethod\n                commitHeadline: $commitHeadline\n                commitBody: $commitBody\n              }\n            ) {\n              clientMutationId\n            }\n          }\n        ","variables":{"mergeMethod":"MERGE","pullRequestId":"PR_kwDOHK6g1c42OkcI"}},"response":{"data":{"enablePullRequestAutoMerge":null},"errors":[{"locations":[{"column":13,"line":8}],"message":"[\"Pull request Pull request is in clean status\"]","path":["enablePullRequestAutoMerge"],"type":"UNPROCESSABLE"}]},"stack":"GraphqlResponseError: Request failed due to following response errors:\n - [\"Pull request Pull request is in clean status\"]\n    at /usr/lib/node_modules/@dvcorg/cml/node_modules/@octokit/graphql/dist-node/index.js:81:13\n    at async Github.prAutoMerge (/usr/lib/node_modules/@dvcorg/cml/src/drivers/github.js:412:7)\n    at async Github.prCreate (/usr/lib/node_modules/@dvcorg/cml/src/drivers/github.js:367:7)\n    at async CML.prCreate (/usr/lib/node_modules/@dvcorg/cml/src/cml.js:414:17)\n    at async Object.exports.handler (/usr/lib/node_modules/@dvcorg/cml/bin/cml/pr.js:11:16)"}
  ```
  </details>

![Overview](./docs/imgs/overview.png)

- :star: -> https://github.com/iterative/dvc
- :star: -> https://github.com/iterative/dvclive
- :star: -> https://github.com/iterative/cml
- :star: -> https://github.com/huggingface/transformerss

## Current status

1. [Local Reproducibility](./docs/1-local-reproducibility.md)

---

You should be able to follow all the steps bellow without leaving the browser, after:

- Forking this repo https://github.com/iterative/workshop-uncool-mlops

- Open fork in GitHub code editor

Navigate to your for fork and press `.` or change the URL from "github.com" to "github.dev"

---

## Workshop

2. [Shared Reproducibility](./docs/2-shared-reproducibility.md)

3. [Online Reproducibility](./docs/3-online-reproducibility.md)

4. [Deployment](./docs/4-deployment.md)

5. [Automation](./docs/5-automation.md)
