They made the ibrand role. No db.
No postgres role. or db.

The easiest way to reassign the postgres role is to be in a db and type:
`CREATE USER postgres SUPERUSER;`

BUT you had to `createdb` in ibrand to do that.
