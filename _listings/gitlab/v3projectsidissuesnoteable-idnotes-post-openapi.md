---
swagger: "2.0"
x-collection-name: GitLab
x-complete: 0
info:
  title: GitLab Post Projects Issues Noteable Notes
  version: 1.0.0
  description: Post projects issues noteable notes.
host: localhost:3000
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/groups/{id}/issues:
    get:
      summary: Get Groups Issues
      description: Get a list of group issues
      operationId: getV3GroupsIdIssues
      x-api-path-slug: v3groupsidissues-get
      parameters:
      - in: path
        name: id
        description: The ID of a group
      - in: query
        name: labels
        description: Comma-separated list of label names
      - in: query
        name: milestone
        description: Return issues for a specific milestone
      - in: query
        name: order_by
        description: Return issues ordered by `created_at` or `updated_at` fields
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      - in: query
        name: sort
        description: Return issues sorted in `asc` or `desc` order
      - in: query
        name: state
        description: Return opened, closed, or all issues
      responses:
        200:
          description: OK
      tags:
      - Groups
      - Issues
  /v3/projects/{id}/issues/{issue_id}/award_emoji:
    get:
      summary: Get Projects Issues Issue Award Emoji
      description: Get projects issues issue award emoji.
      operationId: getV3ProjectsIdIssuesIssueIdAwardEmoji
      x-api-path-slug: v3projectsidissuesissue-idaward-emoji-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: issue_id
        description: The ID of an Issue, Merge Request or Snippet
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Award
      - Emoji
    post:
      summary: Post Projects Issues Issue Award Emoji
      description: Post projects issues issue award emoji.
      operationId: postV3ProjectsIdIssuesIssueIdAwardEmoji
      x-api-path-slug: v3projectsidissuesissue-idaward-emoji-post
      parameters:
      - in: path
        name: id
      - in: path
        name: issue_id
      - in: formData
        name: name
        description: The name of a award_emoji (without colons)
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Award
      - Emoji
  /v3/projects/{id}/issues/{issue_id}/award_emoji/{award_id}:
    get:
      summary: Get Projects Issues Issue Award Emoji Award
      description: Get projects issues issue award emoji award.
      operationId: getV3ProjectsIdIssuesIssueIdAwardEmojiAwardId
      x-api-path-slug: v3projectsidissuesissue-idaward-emojiaward-id-get
      parameters:
      - in: path
        name: award_id
        description: The ID of the award
      - in: path
        name: id
      - in: path
        name: issue_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Award
      - Emoji
      - Award
    delete:
      summary: Delete Projects Issues Issue Award Emoji Award
      description: Delete projects issues issue award emoji award.
      operationId: deleteV3ProjectsIdIssuesIssueIdAwardEmojiAwardId
      x-api-path-slug: v3projectsidissuesissue-idaward-emojiaward-id-delete
      parameters:
      - in: path
        name: award_id
        description: The ID of an award emoji
      - in: path
        name: id
      - in: path
        name: issue_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Award
      - Emoji
      - Award
  /v3/projects/{id}/issues/{issue_id}/notes/{note_id}/award_emoji:
    get:
      summary: Get Projects Issues Issue Notes Note Award Emoji
      description: Get projects issues issue notes note award emoji.
      operationId: getV3ProjectsIdIssuesIssueIdNotesNoteIdAwardEmoji
      x-api-path-slug: v3projectsidissuesissue-idnotesnote-idaward-emoji-get
      parameters:
      - in: path
        name: id
      - in: path
        name: issue_id
      - in: path
        name: note_id
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Notes
      - Note
      - Award
      - Emoji
    post:
      summary: Post Projects Issues Issue Notes Note Award Emoji
      description: Post projects issues issue notes note award emoji.
      operationId: postV3ProjectsIdIssuesIssueIdNotesNoteIdAwardEmoji
      x-api-path-slug: v3projectsidissuesissue-idnotesnote-idaward-emoji-post
      parameters:
      - in: path
        name: id
      - in: path
        name: issue_id
      - in: formData
        name: name
        description: The name of a award_emoji (without colons)
      - in: path
        name: note_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Notes
      - Note
      - Award
      - Emoji
  /v3/projects/{id}/issues/{issue_id}/notes/{note_id}/award_emoji/{award_id}:
    get:
      summary: Get Projects Issues Issue Notes Note Award Emoji Award
      description: Get projects issues issue notes note award emoji award.
      operationId: getV3ProjectsIdIssuesIssueIdNotesNoteIdAwardEmojiAwardId
      x-api-path-slug: v3projectsidissuesissue-idnotesnote-idaward-emojiaward-id-get
      parameters:
      - in: path
        name: award_id
        description: The ID of the award
      - in: path
        name: id
      - in: path
        name: issue_id
      - in: path
        name: note_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Notes
      - Note
      - Award
      - Emoji
      - Award
    delete:
      summary: Delete Projects Issues Issue Notes Note Award Emoji Award
      description: Delete projects issues issue notes note award emoji award.
      operationId: deleteV3ProjectsIdIssuesIssueIdNotesNoteIdAwardEmojiAwardId
      x-api-path-slug: v3projectsidissuesissue-idnotesnote-idaward-emojiaward-id-delete
      parameters:
      - in: path
        name: award_id
        description: The ID of an award emoji
      - in: path
        name: id
      - in: path
        name: issue_id
      - in: path
        name: note_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Notes
      - Note
      - Award
      - Emoji
      - Award
  /v3/projects/{id}/issues/{issue_id}/time_estimate:
    post:
      summary: Post Projects Issues Issue Time Estimate
      description: Post projects issues issue time estimate.
      operationId: postV3ProjectsIdIssuesIssueIdTimeEstimate
      x-api-path-slug: v3projectsidissuesissue-idtime-estimate-post
      parameters:
      - in: formData
        name: duration
        description: The duration to be parsed
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: issue_id
        description: The ID of a project issue
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Time
      - Estimate
  /v3/projects/{id}/issues/{issue_id}/reset_time_estimate:
    post:
      summary: Post Projects Issues Issue Reset Time Estimate
      description: Post projects issues issue reset time estimate.
      operationId: postV3ProjectsIdIssuesIssueIdResetTimeEstimate
      x-api-path-slug: v3projectsidissuesissue-idreset-time-estimate-post
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: issue_id
        description: The ID of a project issue
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Reset
      - Time
      - Estimate
  /v3/projects/{id}/issues/{issue_id}/add_spent_time:
    post:
      summary: Post Projects Issues Issue Add Spent Time
      description: Post projects issues issue add spent time.
      operationId: postV3ProjectsIdIssuesIssueIdAddSpentTime
      x-api-path-slug: v3projectsidissuesissue-idadd-spent-time-post
      parameters:
      - in: formData
        name: duration
        description: The duration to be parsed
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: issue_id
        description: The ID of a project issue
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - ""
      - Spent
      - Time
  /v3/projects/{id}/issues/{issue_id}/reset_spent_time:
    post:
      summary: Post Projects Issues Issue Reset Spent Time
      description: Post projects issues issue reset spent time.
      operationId: postV3ProjectsIdIssuesIssueIdResetSpentTime
      x-api-path-slug: v3projectsidissuesissue-idreset-spent-time-post
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: issue_id
        description: The ID of a project issue
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Reset
      - Spent
      - Time
  /v3/projects/{id}/issues/{issue_id}/time_stats:
    get:
      summary: Get Projects Issues Issue Time Stats
      description: Get projects issues issue time stats.
      operationId: getV3ProjectsIdIssuesIssueIdTimeStats
      x-api-path-slug: v3projectsidissuesissue-idtime-stats-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: issue_id
        description: The ID of a project issue
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Time
      - Stats
  /v3/projects/{id}/issues:
    get:
      summary: Get Projects Issues
      description: Get a list of project issues
      operationId: getV3ProjectsIdIssues
      x-api-path-slug: v3projectsidissues-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: query
        name: iid
        description: Return the issue having the given `iid`
      - in: query
        name: labels
        description: Comma-separated list of label names
      - in: query
        name: milestone
        description: Return issues for a specific milestone
      - in: query
        name: order_by
        description: Return issues ordered by `created_at` or `updated_at` fields
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      - in: query
        name: sort
        description: Return issues sorted in `asc` or `desc` order
      - in: query
        name: state
        description: Return opened, closed, or all issues
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
    post:
      summary: Post Projects Issues
      description: Create a new project issue
      operationId: postV3ProjectsIdIssues
      x-api-path-slug: v3projectsidissues-post
      parameters:
      - in: formData
        name: assignee_id
        description: The ID of a user to assign issue
      - in: formData
        name: confidential
        description: Boolean parameter if the issue should be confidential
      - in: formData
        name: created_at
        description: Date time when the issue was created
      - in: formData
        name: description
        description: The description of an issue
      - in: formData
        name: due_date
        description: Date time string in the format YEAR-MONTH-DAY
      - in: path
        name: id
        description: The ID of a project
      - in: formData
        name: labels
        description: Comma-separated list of label names
      - in: formData
        name: merge_request_for_resolving_discussions
        description: The IID of a merge request for which to resolve discussions
      - in: formData
        name: milestone_id
        description: The ID of a milestone to assign issue
      - in: formData
        name: title
        description: The title of an issue
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
  /v3/projects/{id}/issues/{issue_id}:
    get:
      summary: Get Projects Issues Issue
      description: Get a single project issue
      operationId: getV3ProjectsIdIssuesIssueId
      x-api-path-slug: v3projectsidissuesissue-id-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: issue_id
        description: The ID of a project issue
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
    put:
      summary: Put Projects Issues Issue
      description: Put projects issues issue.
      operationId: putV3ProjectsIdIssuesIssueId
      x-api-path-slug: v3projectsidissuesissue-id-put
      parameters:
      - in: formData
        name: assignee_id
        description: The ID of a user to assign issue
      - in: formData
        name: confidential
        description: Boolean parameter if the issue should be confidential
      - in: formData
        name: created_at
      - in: formData
        name: description
        description: The description of an issue
      - in: formData
        name: due_date
        description: Date time string in the format YEAR-MONTH-DAY
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: issue_id
        description: The ID of a project issue
      - in: formData
        name: labels
        description: Comma-separated list of label names
      - in: formData
        name: milestone_id
        description: The ID of a milestone to assign issue
      - in: formData
        name: state_event
        description: State of the issue
      - in: formData
        name: title
        description: The title of an issue
      - in: formData
        name: updated_at
        description: Date time when the issue was updated
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
    delete:
      summary: Delete Projects Issues Issue
      description: Delete projects issues issue.
      operationId: deleteV3ProjectsIdIssuesIssueId
      x-api-path-slug: v3projectsidissuesissue-id-delete
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: issue_id
        description: The ID of a project issue
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
  /v3/projects/{id}/issues/{issue_id}/move:
    post:
      summary: Post Projects Issues Issue Move
      description: Post projects issues issue move.
      operationId: postV3ProjectsIdIssuesIssueIdMove
      x-api-path-slug: v3projectsidissuesissue-idmove-post
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: issue_id
        description: The ID of a project issue
      - in: formData
        name: to_project_id
        description: The ID of the new project
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Move
  /v3/projects/{id}/merge_request/{merge_request_id}/closes_issues:
    get:
      summary: Get Projects Merge Request Merge Request Closes Issues
      description: Get projects merge request merge request closes issues.
      operationId: getV3ProjectsIdMergeRequestMergeRequestIdClosesIssues
      x-api-path-slug: v3projectsidmerge-requestmerge-request-idcloses-issues-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: merge_request_id
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Merge
      - Request
      - Merge
      - Request
      - Closes
      - Issues
  /v3/projects/{id}/merge_requests/{merge_request_id}/closes_issues:
    get:
      summary: Get Projects Merge Requests Merge Request Closes Issues
      description: Get projects merge requests merge request closes issues.
      operationId: getV3ProjectsIdMergeRequestsMergeRequestIdClosesIssues
      x-api-path-slug: v3projectsidmerge-requestsmerge-request-idcloses-issues-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: merge_request_id
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Merge
      - Requests
      - Merge
      - Request
      - Closes
      - Issues
  /v3/projects/{id}/milestones/{milestone_id}/issues:
    get:
      summary: Get Projects Milestones Milestone Issues
      description: Get all issues for a single project milestone
      operationId: getV3ProjectsIdMilestonesMilestoneIdIssues
      x-api-path-slug: v3projectsidmilestonesmilestone-idissues-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: milestone_id
        description: The ID of a project milestone
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Milestones
      - Milestone
      - Issues
  /v3/projects/{id}/issues/{noteable_id}/notes:
    get:
      summary: Get Projects Issues Noteable Notes
      description: Get a list of project +noteable+ notes
      operationId: getV3ProjectsIdIssuesNoteableIdNotes
      x-api-path-slug: v3projectsidissuesnoteable-idnotes-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Noteable
      - Notes
    post:
      summary: Post Projects Issues Noteable Notes
      description: Post projects issues noteable notes.
      operationId: postV3ProjectsIdIssuesNoteableIdNotes
      x-api-path-slug: v3projectsidissuesnoteable-idnotes-post
      parameters:
      - in: formData
        name: body
        description: The content of a note
      - in: formData
        name: created_at
        description: The creation date of the note
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Noteable
      - Notes
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