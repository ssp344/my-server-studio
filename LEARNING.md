# Lesson 01 - Conversation Evidence

Lesson: STUDIO-001

## Prediction

Before deployment, I predicted that the browser would go to my domain, Traefik would receive the HTTPS request, and Docker would run the calculator.

I did not record the separate request-path prediction before running the plan. I am documenting that missing record honestly.

## Check interpretation

I ran the prepared verification checks after deploying the calculator. The tests passed.

The multiplication test returned 42 with HTTP 200. Division by zero returned HTTP 400, and invalid numeric input returned HTTP 422.

The checks also confirmed trusted HTTPS and that the existing Docker containers were unchanged. These checks do not prove that the entire server is secure.

## Browser observation

I opened https://calc.shiv-is373.xyz in Chrome.

I entered 6 and 7, selected Multiply, and clicked Calculate.

The browser result was 42, and the API result was also 42. The website displayed "Results match."

## Keep decision

I decided to keep the calculator deployment because the website worked correctly, HTTPS was trusted, and the existing services remained unchanged during the checks.

## Review

I reviewed the deployment results and my browser test with my AI coach. I learned that DNS connects my domain to my server, Traefik routes HTTPS requests, and Docker runs the calculator.

I used the supplied calculator image. I did not build the calculator application or its CI/CD pipeline.

## AI Work and Next Step

AI helped me understand the assignment, check my DigitalOcean server, configure the calculator deployment, and interpret the test results.

I completed the deployment commands and tested the public website myself.

My calculator is deployed, local tests and GitHub Actions passed, and I created issue #1 and pull request #2. My next step is to review and merge the pull request. The missing pre-plan prediction record remains disclosed.
