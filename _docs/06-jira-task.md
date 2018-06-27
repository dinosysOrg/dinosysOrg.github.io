---
title: "How to receive task and what to do when it's done"
permalink: /docs/jira-task/
excerpt: "How to report that you have been useful"
last_modified_at: 2018-03-20T15:58:49-04:00
toc: true
---

This repository purpose is to document the process of Agile Project Management using Jira at the tool.

Table of contents:

1.  Introduction to Jira
    - Project Space
2.  Setup Jira project
3.  Align Jira ticket type with Agile methodology
4.  Configure Jira project
    - Board Configuration
    - Ticket type Configuration
    - Priority Configuration
    - Components Configuration
    - Workflow Configuration
5.  Import Trello board to Jira
6.  Using Jira
    - All ticket type status flow
    - Ticket Creation
    - Estimation & Priority
    - Sprint Creation
    - Sprint Planning
    - Dual-track Scrum
    - Daily Activity

# 1. Introduction to Jira

Jira is one of top-of-the-line project management tools used by Agile team.

Advantage:

- Provide developers visual tracking on the progress, statuses, stages, obstacles of tickets they are working on
- Provide PM with tracking the progress of the whole project team, burn-down chart, velocity to calculate the performance of team member
- Built-in tools adapted to Agile methodology

Disadvantage:

- High cost
- Configuration is difficult
- Redundant features

## Project Space

Each Project will have:

- A backlog board which lists all stories in backlog and planned sprints
  ![](https://image.prntscr.com/image/vdrf6B9dQdqF0X19yQsGSw.png)
- A Scrum board which lists all sub-tasks and the ability for users to drag & drop tasks, each action will automatically change status
  ![](https://image.prntscr.com/image/lXe3RxuWRWqV84op8EWmfQ.png)

# 2. Setup Jira Project

Actor: Jira Admin

Go to Project/Create a Project
![](https://image.prntscr.com/image/95sVDd_YTCmbHTxdJ8mdRg.png)

Choose the project template: Scrum software development
![](https://image.prntscr.com/image/5a2sNIXmRnWnoqU2wNdhfw.png)

Input a project name and key (key will be used as prefix for all ticket title)
![](https://image.prntscr.com/image/w4PlH76wTlup3FxzctFo2w.png)

# 3. Align Jira ticket type with Agile methodology

In Agile, we divide the work into:

- Module

- Backlog

- Task

In Jira, we have correspondent ticket types:

![](https://www.atlassian.com/dam/jcr:7f4cf655-1938-41b3-9bdd-49793d7f24fa/epics-vs-stories-agile-development.png)

- Epic ![](https://image.prntscr.com/image/b24phtnaTBevfoumoQG7RQ.png)

  Each epic is written as a big module and can contain multiple stories.

  Ex: Path Management, etc.

- Story ![](https://image.prntscr.com/image/4NMhJXjsTDWdi4qo-erqHw.png)

  Each story is written as a functional user story, it should be as precise and specific as possible.

  Ex: As a visitor, I can see introduction videos of paths.

- Task ![](https://image.prntscr.com/image/s6v-1ZD0RiSn8kDYFOwfJQ.png)

  Each task can be written in technical terms. We use task when we need to do something that doesn't impact functionalities of the application, but to improve the performance.

- UX Design ![](https://image.prntscr.com/image/hYDFhZiaS5aT6ZT-u5bs-g.png)

  This is the type for design task. We can breakdown design task into multiple sub-tasks to keep track of the design progress.

- Sub-task ![](https://image.prntscr.com/image/zhg4v8ktSF_jmayfqH4gxQ.png)

  Each sub-task can be written in technical terms. These sub-tasks are divided after the technical team decided what need to be done for the functional story.

  Ex: [BE] Database - Create the DB schema.

# 4. Configure Jira Project

## Board Configuration

Actor: Project Lead

Go to Board -> Configure
![](https://image.prntscr.com/image/dbTtPeAxRKSrwoOnjXJYbw.png)

### General

In this tab, we can configure the condition to determine which tickets will be displayed in the board by filter.

As default, all tickets (Story, Task, UX Design) will be displayed on the board. But it can be editable to filter tickets by conditions (Type, Status, Component, Assignee, etc.)

![](https://image.prntscr.com/image/-h036mlKQBaQ4wTa4wlwLw.png)

### Columns

In this tab, we can configure which columns we want to show on the active sprint board
![](https://image.prntscr.com/image/t4T-QtkPTWS-YPdYeuoKXQ.png)

In the column configuration, all ticket statuses will need to be mapped on one column.
(!Note: Tickets with unmapped statuses won't be displayed on the board).

### Swimlanes

In this tab, we can configure on using the row to group issues. The good way is Stories

## Priority Configuration

Actor: Jira Admin

Go to Jira Admin -> Issues -> Priorities

Priority is defined by priority level descending (highest on top and lowest at the bottom)

By Agile methodology, we define priority level as: Must -> Should -> Could

![](https://image.prntscr.com/image/uQiuDzSaTRiBQPlKkikwSw.png)

## Ticket Type Configuration

### Create, edit or delete a ticket type

Actor: Jira Admin

We need to create the list of all ticket types before we can activate the ticket type for a project

In order to create a ticket type, go to Jira Admin -> Issues -> Issue types

![](https://image.prntscr.com/image/idmkmN4ES9CprGUWUXkllg.png)

Click Add issue type (![](https://image.prntscr.com/image/n9XfgnmKS-CnxTNDBEVaQw.png)) to create a new type.
There will be 2 type: Standard Issue Type (for a normal type) or Sub-Task Issue Type (for a sub level type under a normal type)

### Activate ticket type to a project

Actor: Project Lead

In the project setting, go to Issue types, choose Actions and Edit Issue Type
![](https://image.prntscr.com/image/aafEOIQaT-m-qSUOt4X8Lg.png)

In the Issue Type Scheme page, drag and drop Issue Types to activate them for the current scheme.
![](https://image.prntscr.com/image/Su09wLNvSoWwTxiSSQrS-g.png)

## Components Configuration

Actor: Project Lead

Open the project space, navigate to Components
![](https://image.prntscr.com/image/YmN7pOzQRMOLCh1PKL7Wmw.png)

There will be 4 attributes: Component name, Component lead, Component description & Default Assignee
![](https://image.prntscr.com/image/kJpHSaejSgOq9picR4xT6A.png)

## Workflow Configuration

### Workflow Creation

Actor: Jira admin
Go to Jira Admin -> Issues -> Workflows -> Add workflow

In the Diagram, we can Add status ![](https://image.prntscr.com/image/zXA03oDARNWVgd4U2BPfAw.png) or Add transition ![](https://image.prntscr.com/image/zXiOb7MfTlqRWJmMeCULbA.png)

There are 3 categories of status:
![](https://image.prntscr.com/image/dtheig0qQH2NDba1_2tyIQ.png)

For transition, we can link between 2 statuses or allow all statuses to transition to a specific status.

### Activate workflow for project

Actor: Project Lead

In Project Settings, go to Workflows, choose Add Workflow, Add Existing.

We can choose an existing workflow and assign it to an issue type.

After confirm, we will need to map statuses from the old workflow to the new one.

# 5. Import Trello Board to Jira

Actor: Jira Admin

## Install import add-on

To import all Trello board, we use free add-on: Trello Importer Plugin for JIM (https://marketplace.atlassian.com/plugins/com.atlassian.jira.plugins.jira-importers-trello-plugin/server/overview)

After download the add-on, go to Jira Admins -> Add-ons -> Manage Add-ons. Choose Upload add-on ![](https://image.prntscr.com/image/GVJlqCnBR62IZRHNY44XGg.png)

Open the path to the atlassian-plugin.xml in jira-importers-trello-plugin-1.5.0 folder

## Import Trello board

Go to Jira Admins -> System -> External System Import -> Trello.

You will need to login in Trello at the same time to authorize for the importing.

After authorized, you can choose the board you want to import, it will create a NEW project space in Jira.
![](https://image.prntscr.com/image/6cRp7TIBStmzynqgLpVSzw.png)

# 6. Using Jira

## All ticket type status flow

Epic:

![](https://image.prntscr.com/image/zUahiwO1QZKMESjXfWbEyg.png)

Story:

![](https://image.prntscr.com/image/DYVi_Uc5QJuLBx4YinFD2g.png)

Sub-task:

![](https://image.prntscr.com/image/iigc0aYHSlumc1cr_aDWYQ.png)

## Ticket Creation

### Version creation

Actor: Project Lead

On tab Releases, we can create Release Version.

Each version should have a start date, release date and description (these 3 are optional).

After created, version will be displayed on Backlog list, we can drag and drop backlogs to each version to track the release.

![](https://image.prntscr.com/image/TCc_THdeS8CyOeaAq5dnGg.png)

After all tasks are completed, we can choose to build and release the version to production environment.

### Epic creation

Actor: Project Lead

Each epic should contains multiple backlogs that are unable to fit inside one sprint.

#### How to create an Epic

There are 2 ways to create an Epic:

1.  Create and Issue Type = Epic
    ![](https://image.prntscr.com/image/UiZNbkWgREy4zb05pnjGQQ.png)
2.  On Backlog board, choose Create epic in Epics navigation panel
    ![](https://image.prntscr.com/image/hYj-EAg4SiW--pDwNT9wHA.png)

#### Field requirement

**Epic Name:** label of the epic

**Summary:** epic title

### Story creation

Actor: Project Lead

A story backlog is a functional feature that we want to develop on the product. It should be written as clear and specific as possible.

Ex: As a visitor, I can see the teacher information.

Ideally, each story should be linked to a version and epic so that we know that story will contribute to the vision of the application. In Jira backlog board, the version and epic of the story will appear on the right side of it if everything is done properly.

![](https://image.prntscr.com/image/C8argPxuRF_bZSDY3O8CSQ.png)

#### How to create a Story

There are 2 ways to create a story:

1.  Use Create button and Issue Type = Story
    ![](https://image.prntscr.com/image/8LcOG4p-QKK5W-dstnSArg.png)

2.  In Backlog Board, choose Create issue, type = Story
    ![](https://image.prntscr.com/image/MrH7dyAWTR_K6WfGfcXJxA.png)

#### Field requirements

**Summary:** Story title

**Epic Link:** choose Epic label to link Story to an Epic

**Priority:** priority of the story (Must, Should, Could)

**Story Points:** measurement of complexity

**Fix Version/s:** Release version of the story

**Assignee:** the person in charge, usually PM

**Description:** describe the functionality of the story

### Sub-task Creation

After a story is created, we need to breakdown the story into tasks, which need to be done in order to complete the story.

#### Breakdown sub-task

In story ticket page, we can choose to add a sub-task into the story
![](https://image.prntscr.com/image/Ckr_fZtAQjiFFmTImHRGxg.png)
In the sub-task creation form, we need to fill in information
![](https://image.prntscr.com/image/qNfk_1kpRxCQR_m_AXcs-w.png)

#### Field Requirement

**Summary:** name of task

**Priority:** Must, Should, Could

**Component/s:** technical type of task (Frontend, backend, iOS, Android, etc.)

**Story points:** Measurement of complexity

**Assignee:** the performer

**Description:** describe the list of task need to be performed on this task

## Estimation & Priority

After all stories are broken down into sub-tasks, we need to estimate and give priority to each tasks.

### Estimation

For each sub-task, the development team needs to estimate complexity point of the task (Story Point). The point is usually given by Fibonacci series (1/2 1 2 3 5 8 13 ...)

**The estimation of a story = sum of all estimations of all sub-tasks.**

For example: if a story contains 2 sub-tasks, each has an estimation of 3 and 5, respectively, then the estimation of the story is 8.
![](https://image.prntscr.com/image/4J_QGBZXR5q_LDHHv4scVA.png)

### Priority

Each story will have a priority, defined by stakeholders (PO, PM, tech lead).

Priority level:

**Must** = highest level of priority, these features are very essential and must be implemented ASAP

**Should** = medium level of priority, these features can bring high values but not necessarily as essential as Must priority

**Could** = low level of priority, these features are nice to have
![](https://image.prntscr.com/image/uQiuDzSaTRiBQPlKkikwSw.png)

## Sprint Creation

When all backlogs are ready (task breakdown, give priority), we can initiate the sprint.

In Backlog board, we can create the sprint by clicking Create Sprint
![](https://image.prntscr.com/image/2PraLMXvQLWFqHTrZHgBUQ.png)

After that, it will create an empty sprint, we can drag and drop backlogs into the sprint to plan them
![](https://image.prntscr.com/image/Vj5cCEd3ShmAbHVlTwxjrw.png)

When all backlogs are planned, we can start the sprint by clicking Start Sprint. It will open a popup for PM to input the duration of the sprint
![](https://image.prntscr.com/image/8vUzYa8XTmq3tiBsJq0A8w.png)

## Sprint Planning

During the sprint planning meeting, the PM need to go through all backlogs and assign each sub-task to a team member.

PM can do it by changing the Assignee of the sub-task ticket
![](https://image.prntscr.com/image/_AYGotvcTz6if_yqIHrKyg.png)

## Dual-track Scrum

### Why we need to use dual-track Scrum

This is mainly for design tasks as we need to work on a story, the design should be completed and approved for that story already. Therefore, within the current sprint, the designer need to work on tasks that will be developed in the following sprint.
![](https://dbcms.s3.amazonaws.com/devbridgecom/bcms/image/f80d324b8b3e4d8b988b045ad7fa9983/2016_02_BlogPost_01.jpg)

### How to setup dual-track

In each sprint, we can plan stories (![](https://image.prntscr.com/image/Ok1kLbZ-Q_eVrD1L_e9I6A.png)) and UX design tasks together (![](https://image.prntscr.com/image/3XL2J9ffQNqq_PCdALJzeg.png))

The UX design tasks should be tasks that will be developed in next sprints and linked together with these stories.

In the active sprint board, we will have developers coding the current sprint and designers working on tasks for next sprints.

![](https://image.prntscr.com/image/xDIKPKGcRimqLIbfx593OQ.png)

## Daily Activity

Everyday, during work, team members can use the Sprint board to view all assigned tasks
![](https://image.prntscr.com/image/7WXl85yTTjOgbEqsHktGsw.png)

While working, team members have to drag and drop sub-task tickets to update their states following the workflow
![](https://image.prntscr.com/image/Mwe0uRy6TxSRYWHwtKFzxQ.png)

When all tasks are completed for a story, team members can choose to update the status of the story to Done
