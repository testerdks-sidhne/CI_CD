# Deployment Note & AWS Resource Details

## Udacity AWS Learner Lab Session Note

This project was built and deployed using temporary **Udacity AWS Learner Lab** infrastructure (AWS EKS & AWS ECR).

> [!NOTE]
> Udacity AWS Learner Lab sessions have a strict 4-hour runtime limit. Once the lab timer expires, AWS automatically terminates the temporary EKS cluster and Load Balancer endpoints (`http://*.elb.amazonaws.com`).

### Proof of Implementation & Screenshots
Because AWS Learner Lab resources automatically clean up upon session expiration, complete evidence of live execution has been documented:

1. **DOCX Document Submission**: Complete end-to-end screenshots showing successful pipeline runs, live Kubernetes deployment, ECR container image uploads, and browser UI movie rendering.
2. **GitHub Actions Workflows**: Fully automated, production-grade CI/CD pipelines configured under `.github/workflows/`.
3. **Infrastructure Code**: Complete Terraform (`setup/terraform`) and Kubernetes manifest (`starter/*/k8s`) configurations.

---

### Live Application Endpoints (Active During Lab Session)
- **Frontend App**: `http://ad0fdbd5df8aa4304859a2a912bb0e43-1384074213.us-east-1.elb.amazonaws.com`
- **Backend API**: `http://ac3023e4fa28c4b77b51fde204dad779-1625317990.us-east-1.elb.amazonaws.com/movies`
