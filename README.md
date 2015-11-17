# SDI
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
