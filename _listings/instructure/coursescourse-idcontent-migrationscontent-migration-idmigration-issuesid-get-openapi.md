---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Courses API Get a migration issue
  description: Get a migration issue.
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /courses/{course_id}/content_migrations/content_migration_id/migration_issues:
    get:
      summary: List migration issues
      description: List migration issues.
      operationId: list-migration-issues
      x-api-path-slug: coursescourse-idcontent-migrationscontent-migration-idmigration-issues-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Content
      - Migrations
      - Content
      - Migration
      - Id
      - Migration
      - Issues
  /courses/{course_id}/content_migrations/content_migration_id/migration_issues/{id}:
    get:
      summary: Get a migration issue
      description: Get a migration issue.
      operationId: get-a-migration-issue
      x-api-path-slug: coursescourse-idcontent-migrationscontent-migration-idmigration-issuesid-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Content
      - Migrations
      - Content
      - Migration
      - Id
      - Migration
      - Issues
      - Id
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---