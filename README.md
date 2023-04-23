Download Link: https://assignmentchef.com/product/solved-ac12-accounting-mis-solved
<br>



<table>

 <tbody>

  <tr>

   <td colspan="3" width="715"><strong>Table name: Package </strong>PACK PACKNAME            PACKV PAcKTYPE            PACKCOST—- ————-      ——-  —–        ————-AC11 Quick Accounting     4.1   Accounting           754.95AC12 Accounting MIS       4.0   Accounting          2000.00AC13 QuickBook            2005  Accounting           300.00DB11 Manta                1.5   Database             380.00DB13 SQL Server           2005  Database             500.00DB14 My SQL               2005  Database             300.00DB22 Manta                2.1   Database             430.25SS11 EasyCal              5.5   Spreadsheet          225.15WP04 Word Power           2     Word Processing      118.00WP07 Good Word            3.2   Word Processing      35.00WP14 GOOGLE               2     Word Processing      118.00</td>

  </tr>

  <tr>

   <td colspan="2" width="463"><strong>Table name: Software</strong>PACK TAGNUM INSTDATE                SOFTCOST—- —— ———————————-AC11 32807  1995-09-13 00:00:00.000 754.95AC11 32809  1998-09-13 00:00:00.000 754.95AC11 37691  1998-09-13 00:00:00.000 754.95AC12 32809  1998-09-13 00:00:00.000 2000.00DB11 32808  1996-12-03 00:00:00.000 380.00DB11 37691  1995-06-15 00:00:00.000 380.00DB22 37691  1997-05-27 00:00:00.000 430.25DB22 57772  1997-05-27 00:00:00.000 430.25WP04 32808  1996-01-12 00:00:00.000 180.50WP04 37691  1995-06-15 00:00:00.000 180.50WP04 57772  1998-05-27 00:00:00.000 180.50WP07 59836  1995-10-30 00:00:00.000 35.00WP07 77740  1995-05-27 00:00:00.000 70.00</td>

   <td width="252"><strong>Table name: Computer </strong>COMP MFRNAME    PROCT—- ———- ——C101 COMPAQ     486DXC102 COMPAQ     PENTIC103 COMPAQ     PENTID111 Dell       simmD145 DELL       486DXD155 DELL       486DXD165 DELL MIC   486DXD245 DELL       PENTIH120 NULL       NULLH125 HP         486SXH225 HP         486DX</td>

  </tr>

  <tr>

   <td width="358"><strong>Table name: Employee </strong> empnum empname         empphone—— ————— ——–119    Robert Oden     1312123    Douglas Daly    1213223    Tim Duncan      1213356    Tracy Yao       1214456    David Johnson   1214525    Tracy Sharp  Jr 1311533    Tracy Sharp II  1412625    Tracy Sharp     1311633    Tracy Johnson   1412911    Robert NoPC     1312</td>

   <td colspan="2" width="358"><strong>Table name: PC </strong> tagnum comp empnum location—— —- —— ————-32807  D145 NULL   Accounting32808  D145 123    Sales32809  C101 356    Sales32810  C101 456    Accounting37691  D155 625    Info Sys37692  H125 456    Home37693  H125 NULL   Home57772  H225 123    Info Sys59836  H225 625    Info Sys59837  H225 633    Info Sys77739  C102 625    NULL77740  C101 625    Accounting</td>

  </tr>

  <tr>

   <td width="354"></td>

   <td width="104"></td>

   <td width="249"></td>

  </tr>

 </tbody>

</table>













Drop table software

Drop table pc

Drop table package

Drop table employee

Drop table computer




CREATE TABLE [employee] (

[empnum] [char] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL ,

[empname] [varchar] (15) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL ,

[empphone] [char] (4) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,

PRIMARY KEY  CLUSTERED

(

[empnum]

)  ON [PRIMARY]

) ON [PRIMARY]

GO







CREATE TABLE [computer] (

[COMP] [char] (4) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL ,

[MFRNAME] [char] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,

[PROCT] [char] (6) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,

PRIMARY KEY  CLUSTERED

(

[COMP]

)  ON [PRIMARY]

) ON [PRIMARY]

GO







CREATE TABLE [package] (

[PACK] [char] (4) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL ,

[PACKNAME] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,

[PACKV] [char] (4) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,

[PAcKTYPE] [char] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,

[PACKCOST] [numeric](10, 2) NULL ,

PRIMARY KEY  CLUSTERED

(

[PACK]

)  ON [PRIMARY]

) ON [PRIMARY]

GO







CREATE TABLE [pc] (

[tagnum] [char] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL ,

[comp] [char] (4) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,

[empnum] [char] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,

[location] [char] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,




) ON [PRIMARY]

GO







CREATE TABLE [software] (

[PACK] [char] (4) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL ,

[TAGNUM] [char] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL ,

[INSTDATE] [datetime] NULL ,

[SOFTCOST] [numeric](10, 2) NULL ,




) ON [PRIMARY]

GO




insert into package values (‘AC11′,’Quick Accounting’,’4.1 ‘,’Accounting          ‘,754.95)

insert into package values (‘AC12′,’Accounting MIS’,’4.0 ‘,’Accounting          ‘,2000.00)

insert into package values (‘AC13′,’QuickBook’,’2005′,’Accounting          ‘,300.00)

insert into package values (‘DB11′,’Manta’,’1.5 ‘,’Database            ‘,380.00)

insert into package values (‘DB13′,’SQL Server’,’2005′,’Database            ‘,500.00)

insert into package values (‘DB14′,’My SQL’,’2005′,’Database            ‘,300.00)

insert into package values (‘DB22′,’Manta’,’2.1 ‘,’Database            ‘,430.25)

insert into package values (‘SS11′,’EasyCal’,’5.5 ‘,’Spreadsheet         ‘,225.15)

insert into package values (‘WP04′,’Word Power’,’2   ‘,’Word Processing     ‘,118.00)

insert into package values (‘WP07’,’Good Word ‘,’3.2 ‘,’Word Processing     ‘,35.00)

insert into package values (‘WP14′,’GOOGLE’,’2   ‘,’Word Processing     ‘,118.00)




insert into computer values (‘C101’,’COMPAQ    ‘,’486DX ‘)

insert into computer values (‘C102’,’COMPAQ    ‘,’PENTI ‘)

insert into computer values (‘C103’,’COMPAQ    ‘,’PENTI ‘)

insert into computer values (‘D111’,’Dell      ‘,’simm ‘)

insert into computer values (‘D145’,’DELL      ‘,’486DX ‘)

insert into computer values (‘D155’,’DELL      ‘,’486DX ‘)

insert into computer values (‘D165’,’DELL MIC  ‘,’486DX ‘)

insert into computer values (‘D245’,’DELL  ‘,’PENTI’)

insert into computer values (‘H120’,NULL, NULL)

insert into computer values (‘H125’,’HP        ‘,’486SX ‘)

insert into computer values (‘H225’,’HP        ‘,’486DX ‘)




insert into employee values (‘119’,’Robert Oden  ‘,’1312’)

insert into employee values (‘123′,’Douglas Daly’,’1213′)

insert into employee values (‘223′,’Tim Duncan’,’1213′)

insert into employee values (‘356′,’Tracy Yao’,’1214′)

insert into employee values (‘456′,’David Johnson’,’1214′)

insert into employee values (‘525′,’Tracy Sharp  Jr’,’1311′)

insert into employee values (‘533′,’Tracy Sharp II’,’1412′)

insert into employee values (‘625’,’Tracy Sharp  ‘,’1311’)

insert into employee values (‘633′,’Tracy Johnson’,’1412′)

insert into employee values (‘911’,’Robert NoPC  ‘,’1312’)







insert into pc values (‘32807′,’D145’, NULL,’Accounting          ‘)

insert into pc values (‘32808′,’D145′,’123’,’Sales               ‘)

insert into pc values (‘32809′,’C101′,’356’,’Sales         ‘)

insert into pc values (‘32810′,’C101′,’456’,’Accounting          ‘)

insert into pc values (‘37691′,’D155′,’625’,’Info Sys            ‘)

insert into pc values (‘37692′,’H125′,’456’,’Home                ‘)

insert into pc values (‘37693′,’H125’, NULL,’Home                ‘)

insert into pc values (‘57772′,’H225′,’123’,’Info Sys            ‘)

insert into pc values (‘59836′,’H225′,’625’,’Info Sys            ‘)

insert into pc values (‘59837′,’H225′,’633’,’Info Sys            ‘)

insert into pc values (‘77739′,’C102′,’625’,Null)

insert into pc values (‘77740′,’C101′,’625’,’Accounting          ‘)







insert into software values (‘AC11′,’32807′,’1995-09-13 00:00:00’,754.95)

insert into software values (‘AC11′,’32809′,’1998-09-13 00:00:00’,754.95)

insert into software values (‘AC11′,’37691′,’1998-09-13 00:00:00’,754.95)

insert into software values (‘AC12′,’32809′,’1998-09-13 00:00:00’,2000)

insert into software values (‘DB11′,’32808′,’1996-12-03 00:00:00’,380.00)

insert into software values (‘DB11′,’37691′,’1995-06-15 00:00:00’,380.00)

insert into software values (‘DB22′,’37691′,’1997-05-27 00:00:00’,430.25)

insert into software values (‘DB22′,’57772′,’1997-05-27 00:00:00’,430.25)

insert into software values (‘WP04′,’32808′,’1996-01-12 00:00:00’,180.50)

insert into software values (‘WP04′,’37691′,’1995-06-15 00:00:00’,180.50)

insert into software values (‘WP04′,’57772′,’1998-05-27 00:00:00’,180.50)

insert into software values (‘WP07′,’59836′,’1995-10-30 00:00:00’,35.00)

insert into software values (‘WP07′,’77740′,’1995-05-27 00:00:00’,70.00)
















QUESTIONS:







<ol>

 <li>Create a procedure to find out the computer model (computer tables) installed in more than one department that have the accounting software installed.</li>

</ol>

2.      Create a procedure to find out the information of the employee who uses the highest total amount of software package.

<ol start="3">

 <li>Create a procedure to find out all the information of the PCs that do not have the highest total amount of cost of a software package type, given the name of the type (e.g., accounting). Check the validity of the given type.</li>

</ol>

4.      Create a procedure to list all the information of employee, given the name of the employee (e.g., Tracey), who use more than three PCs made by one particular vendor, given the name of the vendor (e.g., Dell), or use a particular type of software package, given the type of the package (e.g., accounting). Check the validity of these given information.


