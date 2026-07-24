# Deployment Note & AWS Resource Details

## Udacity AWS Learner Lab Session Note

This project was built and deployed using temporary **Udacity AWS Learner Lab** infrastructure (AWS EKS & AWS ECR).

> [!NOTE]
> Udacity AWS Learner Lab sessions have a strict 4-hour runtime limit. Once the lab timer expires, AWS automatically terminates the temporary EKS cluster and Load Balancer endpoints (`http://*.elb.amazonaws.com`).

### Proof of Implementation & Screenshots
Because AWS Learner Lab resources automatically clean up upon session expiration, complete evidence of live execution has been documented:

1. **DOCX Document Submission**: Complete end-to-end screenshots showing successful pipeline runs, live Kubernetes deployment, ECR container image uploads, and browser UI movie rendering.
2. **GitHub Actions Workflows**: Fully automated, production-grade CI/CD pipelines configured under `.github/workflows/`.
