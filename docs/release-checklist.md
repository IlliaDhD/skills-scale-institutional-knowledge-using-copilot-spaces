# Release Checklist

This checklist expands on the [Release & Deployment Guide](octoacme-release-and-deployment.md) with step-by-step pre-release, deploy, and post-release checks to ensure release readiness and safe production rollout.

## Pre-Release Checks

### Code Quality & CI
- [ ] All CI checks pass (build, tests, linting)
- [ ] Unit test coverage meets project standards
- [ ] Integration tests pass
- [ ] Security scans complete with no critical vulnerabilities
- [ ] Code reviews completed and approved
- [ ] All blocking issues resolved

### Documentation
- [ ] Release notes drafted and reviewed
- [ ] Changelog updated with user-facing changes
- [ ] API documentation updated (if applicable)
- [ ] User guide or help docs updated for new features
- [ ] Runbooks updated for operational changes

### Release Artifacts
- [ ] Version number updated according to semantic versioning
- [ ] Release branch or tag created
- [ ] Build artifacts generated and validated
- [ ] Deployment manifests reviewed and updated
- [ ] Configuration changes documented and reviewed

### Testing & Validation
- [ ] End-to-end smoke tests pass in staging
- [ ] Manual QA completed for critical flows
- [ ] Regression testing completed for affected areas
- [ ] Performance testing completed (if applicable)
- [ ] Accessibility testing completed for UI changes

### Rollback Preparedness
- [ ] Rollback plan documented and reviewed
- [ ] Previous stable version identified and accessible
- [ ] Database migration rollback tested (if applicable)
- [ ] Feature flags configured for gradual rollout (if applicable)

### Stakeholder Alignment
- [ ] Product Manager approves release
- [ ] Project Manager confirms readiness
- [ ] On-call engineer identified and notified
- [ ] Customer support team notified of changes
- [ ] Marketing/comms team notified (if user-facing)

---

## Deploy Checks

### Pre-Deployment
- [ ] Deployment window confirmed and communicated
- [ ] On-call rotation coverage verified
- [ ] Incident response team on standby
- [ ] Deployment runbook reviewed
- [ ] Monitoring dashboards open and ready

### Staging Deployment
- [ ] Deploy to staging environment
- [ ] Smoke tests pass in staging
- [ ] Manual validation of critical flows in staging
- [ ] Performance metrics reviewed in staging
- [ ] Logs reviewed for errors or warnings

### Production Deployment
- [ ] Announce deployment start to relevant channels
- [ ] Execute deployment following runbook
- [ ] Monitor deployment progress in real-time
- [ ] Verify deployment completes successfully
- [ ] Check application starts and is healthy

---

## Post-Release Checks

### Immediate Validation (0-15 minutes)
- [ ] Smoke tests pass in production
- [ ] Critical user flows validated manually
- [ ] Error rates within expected range
- [ ] Latency/performance metrics normal
- [ ] No spike in 4xx or 5xx errors
- [ ] Key endpoints responding correctly

### Monitoring & Observability (15 minutes - 1 hour)
- [ ] Application logs reviewed for errors
- [ ] Infrastructure metrics (CPU, memory, disk) normal
- [ ] Database performance metrics normal
- [ ] External dependencies healthy
- [ ] Alerts configured and functional
- [ ] User activity and traffic patterns normal

### Communication & Follow-up (1 hour - 24 hours)
- [ ] Announce deployment completion to relevant channels
- [ ] Update status page (if applicable)
- [ ] Monitor support channels for user-reported issues
- [ ] Track key business metrics and KPIs
- [ ] Schedule post-release review meeting
- [ ] Document any issues encountered during deployment

### Post-Release Documentation
- [ ] Publish final release notes
- [ ] Update version documentation
- [ ] Archive deployment logs and metrics
- [ ] Document lessons learned
- [ ] Update runbooks based on deployment experience
- [ ] Close related issues and PRs in issue tracker

---

## Rollback Triggers

Initiate rollback if any of the following occur:
- Critical production incident or outage
- Error rates exceed baseline by >50%
- Performance degradation >30% from baseline
- Data corruption or data loss detected
- Security vulnerability discovered in release
- Business-critical functionality broken

---

## Notes

- Adjust checklist items based on project size and risk profile
- Use automation (CI/CD, smoke tests, monitoring) to reduce manual checks
- Archive completed checklists for retrospectives and audits
- Review and update this checklist based on release retrospectives
