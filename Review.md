##MongoDB

https://www.mongodb.com/docs/languages/python/pymongo-arrow-driver/current/quick-start/

$ python -m pip install pymongoarrow

from pymongoarrow.monkey import patch_all

patch_all()

from pymongoarrow.api import Schema

schema = Schema({'_id': int, 'amount': float, 'last_updated': datetime})

df = client.db.data.find_pandas_all({'amount': {'$gt': 0}}, schema=schema)


