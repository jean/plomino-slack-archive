# plomino-slack-archive

Import Slack JSON export to a Plomino app 

This is a very quick and dirty import of Slack's JSON archive export (request
an export from https://TEAM.slack.com/services/export where TEAM is the name of
your team).

To use this, create a Plomino db in a local Plone site, browse to the _Design_
interface, and specify the directory where you cloned this to import 
_From server folder_. To import to a remote Plomino db, start from the local
one.

Currently, this app doesn't make it very convenient to import the JSON. You 
need to unzip the export, and import users, channels, and then messages per
channel separately. Messages are archived as a JSON file per month. You can
select all the files for a channel at once.

Limitations include:

- Plomino formulas don't have access to regular expressions, so markdown-style
  formatting in messages is very basic.
- Plomino formulas can't deal with zip files, so you need to unzip the archive
  first.

