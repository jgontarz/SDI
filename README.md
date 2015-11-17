--SDI Video 1
--Scrips for SDI Workshop

--Run as SYSTEM user
call grant_activated_role('sap.hana.xs.ide.roles::Developer', 'HTA##');
grant execute on grant_activated_role to HTA##;
grant execute on revoke_activated_role to HTA##;

grant create remote source to HTA##;
grant adapter admin to HTA##;
grant agent admin to HTA##;

--Run as HTAxx
grant select, insert, update, delete, execute on schema HTA## to _sys_repo with grant option;

--SDI Video 2
drop table employees cascade;
create column table employees
	(id integer,
	 name varchar(20),
	 role varchar(20)
	 );
	 
insert into employees values (1, 'Christopher', 'Manager');
insert into employees values (2, 'Eric', 'Manager');
insert into employees values (3, 'Rita', 'Director');
insert into employees values (4, 'Sachin', 'Director');
insert into employees values (5, 'Doreen', 'Manager');
insert into employees values (6, 'Gabriel', 'Manager');
insert into employees values (7, 'Angel', 'Director');
insert into employees values (8, 'Robin', 'Director');
insert into employees values (9, 'Sarah', 'Manager');
insert into employees values (10, 'Ryan', 'Manager');

select * from employees;
