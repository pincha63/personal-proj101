# personal-proj101 (versions will be 101 .. 199)

Allows users to track progress in pre-defined projects

Tech stack
----------

* Ruby (Windows 2.4.2-2)
* Devkit
* Local with DataMapper + SQLite (maybe also Sequel and/or PostgreSQL)
* Hosted with Sequel + PostgreSQL

Data Architecture
-----------------

*  There will be a table of users 
    (for the time being, login will have username but no password)
*  There will be a table of projects
    (one user can have zero to many projects, each project has one user)
*  Each project will have one or more periods (days or weeks)
*  For each period within a project we'll collect metrics
  (Values of metrics can either be picked from a value list...
    or be numberic wihin a range...
    usually an integer, but let's allow decimals)
*  Once a project achieves a milestone, report on progress per...
    a pre-defined success formula
*  Once a project is done, same, and archive to the user's history
    (which means there is a User 1:N Proj_History persistence)

Application Principles
----------------------
Procedure for log-in and/or sign-up
* allow federated via Google Twitter or Facebook (?)

Procedure for creating project
*  Project Name
*  Duration
*  Metrics (maybe allow choosing from set of existing metrics)
*  Success criterion (formula)

Procedure for entering data
*  Choose period
*  Enter metric value for period
*  Repeat for all metrics

Procedure for seeing reports
*  Milestone report by metric
*  Milestone report by success formula
*  Project report (only if project has finished)

Allowances
----------
* Suspend and resume project
* Choose song for project
* Choose theme for project
