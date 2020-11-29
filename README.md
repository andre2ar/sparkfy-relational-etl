# Sparkify

Sparkify is a startup company that provides music streaming to their clients. All users activities has been saved in a JSON file and the company is trying to extract useful information from this data.

## Problem

As data grows has become harder to analyze the data stored in these JSON files and the company is looking for a better solution to extract the data.

## Solution

A possible solution for this problem is store these data in a relational database designed for fast retrieval of data.
This goal can be achieved using a star schema.

### Star Schema
   
The STAR schema consists of one fact table referencing any number of dimension tables which helps the Sparkify for solving simplified common business logic.

- What is the next song Sparkify user would like to listen based on his past behavior.
- Which song user would be more interested in listening to that particular point of time.
And much more complex business logics can be easily solved using the STAR schema method.

Created a STAR schema, optimized for song play analysis.

- Fact Table: songplays: attributes referencing to the dimension tables.
- Dimension Tables: users, songs, artists and time table.

This database will help the internal departments of the Sparkify company to do different kinds of analysis to recommend a Sparkify user.

- Favorite songs of user based on the week day: By joining songplay and songs and user table based on level.
- Recent listened to songs: By joining songplays and user table can show recommendation on the app based on subscription level.
- Can help in recommending most popular songs of the day/week.

## ETL

- Created songs, artist dimension tables from extracting songs_data by selected columns.
- Created users, time dimension tables from extracting log_data by selected columns.
- Created the most important table fact table from the dimensison tables and log_data called songplays.