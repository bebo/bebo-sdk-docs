Database API
===============

`Bebo.Db` is for saving, retrieving and deleting data.

Bebo.Db.save
---------------

`Bebo.Db.save(table, params, callback);`

The save() function will save the data within params to our database. If the table that you pass does not yet it exist it will be created. If an id is passed into params that will become the primary key but if left out it will be created for you::

    Bebo.Db.save('score', {score: 87}, function(err, data){
        if(err){ return console.log('error saving data', err) };
        console.log('data', data); // an object containing the saved data
    });

Bebo.Db.get
---------------

`Bebo.Db.get(table, params, callback);`

The get() function will retrieve the data from our database. The keys added to params become the query::

    {count: 50} - retrieve up to 50 results
    {sort_by:'score' , count: 50} - retrieve up to 50 results sorted by score
    {id: 'id'} - retrieve a specific database entry if you provide the key
    Bebo.Db.get('score', {count: 50}, function(err, data){
        if(err){ return console.log('error retreiving data', err) };
        console.log('data', data); // an array of objects containing the data requested
    });

Bebo.Db.delete
---------------

`Bebo.Db.delete(table, params, callback);`

The delete() function will delete an entry from our database. Params must contain the entry id::

    Bebo.Db.delete('score', {id: 1}, function(err, data){
        if(err){ return console.log('error deleting data', err) };
        console.log('data', data); // an object containing the deleted entry
    });