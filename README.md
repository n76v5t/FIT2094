java c
FIT2094 Databases 
Assignment 1 Logical - ReadMore Community Library (RCL) 
Purpose 
Given the provided case study from Assignment 1 - Conceptual, and additional 
forms/documents related to the case study, students will be asked to transform the information provided into a sound database design and implement it in Oracle. This task covers learning outcomes: 
1.   Apply the theories of the relational database model. 
2. Develop a sound relational database design. 
3. Implement a relational database based on a sound database design. 
Your task 
This is an open-book group task (students will work in groups of two or three, with members selected randomly). The final output for this task will be a logical model implemented in the Oracle RDBMS 
INSTRUCTIONS 
Please note that your group must not start the modelling task until each member individually has completed the Applied 6 logical model for the property rental case study, pushed it to their private repo, and compared your answer with that provided in the sample solution to check their understanding. The completion of this individual task will be checked via your GitLab account pushes. 
This task continues the work you have started in Assignment 1 Conceptual by refining/extending the model you developed and implementing it as a set of tables under your Monash Oracle database account. 
Since this is an ongoing development process based on your assignment 1 conceptual submission and marker feedback, you must ensure that they remain confidential and are only seen by your group members and the unit teaching staff. 
The Assignment 1 Conceptual brief must be read in conjunction with the Assignment 1 Logical brief (this document) - i.e. your final model must encompass both sets of requirements. You may modify your Assignment 1 Conceptual model in any manner you wish as you work through Assignment 1 Logical, provided your final model meets both requirements. Your Assignment 1 Conceptual model will not be submitted or assessed again; any modifications you make to your conceptual model are only part of the group working towards your logical model.
In developing your final logical data model, composite attributes present in your conceptual model must be expanded into their component simple attributes unless explicitly directed otherwise. If the supplementary material presented in this document does not guide you in deciding the components, you may make any reasonable decision on their simple component attributes.
Further discussions with Read More Community Library have revealed the points listed below:
●  RCL has expanded the previous details supplied to indicate that, as well as Counter Reserve status; they assign a status value to indicate if a book is:
○   On Counter Reserve,
○    On Loan, or
○   Available for borrowing.
●  RCL assigns a Borrower Class to each registered borrower. The classes which they
currently use are Adult, Child and Organisation. A borrower’s class controls how many   books the borrower can have on loan at any time and their standard loan period in days (the number of days a book can be borrowed). RCL has indicated that they wish to add  other classes of borrowers in the future.
●  If a borrower has an overdue loan, RCL prevents the borrower from borrowing any
further books (bans them) until the outstanding loan is returned. On returning the
outstanding loan, the borrower is charged a fine based on the number of days they are late (the number of days late is not required to be stored in the system). RCL has
indicated that only around 1.8% of loans are returned late.
●  If a book copy is currently on loan, a borrower may reserve it and be informed when it becomes available. To use this service, a borrower must provide a contact phone number so they can be informed when the copy becomes available. RCL records the date and time the borrower placed the reserve. A given book copy may have several outstanding reserves against it. When the book is available, the borrower with the oldest reserve is informed via a telephone call and a loan is arranged.  This borrower’s reserve will then be removed from the system. 
●  RCL has book copies that are stolen, lost, or damaged and can thus no longer be  assigned in a loan. They have asked for your advice on how their database should handle such copies and ask that this be included in your design.
●  RCL has indicated they wish to treat the branch address, LGA contact name, and all phone numbers as simple attributes.
Read More Community Library has supplied the following two forms as samples of those used within their business.
You should note: 
● The data shown is incomplete and only representative of the type of data for each item. The forms contain fabricated data, so you are aware of typical requirements. 
● Several examples of a form maybe provided to show you the variety of the data; you only need to do ONE normalisation per type of report. 
(i) ReadMore Community Library Catalogue Search Output: 
Sample A: 

Sample B: 

(ii) ReadMore Community Library Borrowers Quarterly Report: 

REMEMBER to keep up to date with the Ed Assignment 1 Logical forum, where further clarifications may be posted (this forum is to be treated as your client).
Please be careful not to publicly post anything that includes your reasoning, logic, or any part of your work to this forum. Doing so violates Monash plagiarism/collusion rules    and carries significant academic penalties. If you need to discuss your approach, ensure you use Ed private posts.You can make assumptions if needed; however, they must align with the details in this brief and the assignment forums and be documented (see the required submission files). Other than surrogate keys, where appropriate, you must remember the design adage "All that is required has been included, and all that has been included is required", i.e. you must  not add features outside the requirements expressed in the brief.
Group Communication 
Your group MUST use your private group channel in MS Teams for all group communication during this assignment, which is not face-to-face. Microsoft Teams provides facilities to support group interaction, including chat, group email, shared desktop, meetings, video/audio calling and shared files.
Activity in your private group channel is only visible to your group members and the teaching staff. It is important that you use Microsoft Teams for your group activities, as your marker may need to check the group members' contributions to the task and attendance at meetings—such a decision will be based on the activity in your private group channel ONLY.
Git Management 
Ensure your group name is on every page of any document you submit. If a document is multipage (such as the normalisation), please include page numbers on every page.
GIT STORAGE Your work for these tasks MUST be saved in your group's local working directory (repo) in  the Ass1 Logical folder. As a start, in your local repo, create a folder named rcl_model and then in this folder, save your model as rcl_logical, i.e. save it as rcl_logical.dmd inside the rcl_model folder. 
Your model must be regularly pushed to the FIT GitLab server to build a clear history of its development. At least nine pushes of your Oracle Data Modeller model to the FIT Git Lab   server are required. Please note that nine pushes is a minimum; in practice, we would expect significantly more. This number of pushes must be evenly distributed amongst group members. All commits代 写FIT2094 Databases Assignment 1 Logical - ReadMore Community Library
代做程序编程语言 must include a meaningful commit message that clearly describes what the particular commit is about and must be correctly assigned to a valid GitLab author. 
Groups must regularly check that their pushes have been successful by logging in to the FITGit Lab server's web interface; you must not simply assume they are working. Before submission via Moodle, log in to the Git Lab server's web interface and ensure your   submission files are present.GIT automatically maintains a history of all files pushed to the server. You do not need to, and MUST not, add a version name to your various versions. Please ensure you use the  same name for all versions of a particular file.
Groups MUST NOT use REVERT or RESET when working on this assignment task.  Doing so could potentially cause severe errors in your remote repo. If you have problems  pushing to the remote group repo, move your current local group repo out of the way (to a new folder) and reclone your group repo as discussed in the Applied 2 lesson (section
A2-1.2).
Working on Oracle Data Modeler Models in your Group Repo 
If multiple students work on a logical model simultaneously, merging these changes can be difficult since the files have complex XML structures. For this reason, you must take a simple approach to working on the model - lock the remote repo when making changes. Only one member of your group can and must work on the model at a particular time.
Whenever a particular student wishes to work on the model, they should go to the Git Server web interface and check if another group member has locked the Ass1 Logical folder.
If the folder is locked, you must not carry out any work on the assignment task. 
If it has not been locked, you can proceed to lock the folder by selecting "Lock":

Ensure you are in the correct folder when this lock is applied.
You will know the items are locked as each will have a lock icon attached to it:

If you hover over the padlock icon, you can see who has the folder locked currently.
After locking the folder, you MUST do a pull (no changes must be made in your group local repo until the lock is in place AND this pull has been completed). When you have completed your work and pushed it to Git, you should return to the Git web interface and  unlock the folder:

The model must not be completed by only one member of the group. In assessing 
your group's work, we will examine the commit log to ensure all group members have contributed to building the model.
Tasks to complete 
1.   Perform. normalisation to 3NF for the data depicted in the two supplied sample
documents. Remember there are only two documents to normalise (you have been given several samples to help you understand the likely content).
The approach you must use is shown in the normalisation applied class solutions. The normalisation must be carried out form. by form. (i.e., one form. at a time), beginning by    representing the document you are working on as a single UNF relation and then
moving through 1NF, 2NF, and 3NF. No marks will be awarded if you use a different approach.
During normalisation, you must:
○ Not add surrogate keys.
○ Include all attributes (you must not remove any attribute as derivable)
○    Clearly show UNF, 1NF, 2NF and 3NF.
○   Clearly show all candidate keys for each relation in 1NF.
○ Identify the Primary Key in all relations by underlining the PK attribute/s.
○ Identify all dependencies at the various normalisation stages (Partial at 1NF, Transitive at 2NF and Full at 3NF). You should use the same notation as
depicted in the normalisation sample solutions, for example:
attr1 -> attr2, attr3
If none exist, you must note this by stating:
No partial dependencies present and/or No transitive dependencies present 
○ Carry out attribute synthesis.
The relation and attribute names used throughout your normalisation and those on your subsequent logical model must be the same.
Your normalisation must be carried out in an MS Word document in your group’s
private MS Teams channel so that a full development history is available. All group members must contribute to this normalisation (i.e. be visible as editors in the document history). The document does not need to be pushed to Git Lab other than as listed in Submission Requirements.
2.   Prepare a logical level design for the Read More Community Library database based on your group's Assignment 1 Conceptual model, your marker's feedback, your reading of  this case study, and the normalisations you carried out in step 1 above.
○   The logical model must be drawn using the Oracle Data Modeler. Information engineering or Crow’s foot notation must be used to draw the model. Your
logical model must not show data types.
○   All relations depicted must be in 3NF. Candidate keys are possible natural
keys; you must ensure your model protects all candidate keys to maintain the business rules.
○   You must add at least one surrogate key to your design (you are free to
select the most appropriate relation to make this change in). You must 
explain why you added the surrogate key to your chosen relation as part of your assumptions. We have a unit rule about requiring a surrogate key if   the relation has a composite key with more than two attributes, but this is not the only reason you might add a surrogate. You may add surrogate keys to multiple relations if you wish.
○   All attributes must be commented in the database (i.e., the comments
must be part of the table structure, not simply comments in the schema file).
○   Check clauses/look-up tables must be applied to attributes where appropriate.
○   You MUST include the legend in your model. Please edit the legend panel to show your group name.
○    Please carefully check slide 37 from the Topic 5 Workshop and ensure you follow the steps listed. 
○   Your GIT repository must indicate your development history with multiple commits/pushes as you work on your model.
3. Generate the database schema in Oracle Data Modeler and use the schema to create the database in your Oracle account (this should be tested in your 
individual Oracle accounts - a group Oracle account is unavailable).
The only edit you are permitted to carry out to the generated schema file is to add
header comment/s containing your details (group/members names) and the commands to spool/echo your run of the script. In generating your schema file, ensure you:
○  Capture the output of the run of your schema statements using the spool command.
○  Ensure your script. includes drop table statements at the start of the script.
○ Name the schema file as rcl_schema.sql. 
4.   Maintain a Group Diary that records when the group met to discuss/work on the task, including the date, who was present and a brief statement of what occurred. This
Group Diary must be maintained in Microsoft Teams as a shared document in your  private group channel. It should continue the diary you started in Assignment 1 Conceptual. It does not need to be pushed to Git Lab other than as listed in
Submission Requirements.
As part of your assignment submission, each group member will be required to provide confidential feedback on the group member's performance/interactions via FeedbackFruits.
Please note when working with your model, ensure that you NEVER select any export options from the Data Modeler menu:

such actions can fill your Oracle account space and render it unusable.





         
加QQ：99515681  WX：codinghelp
