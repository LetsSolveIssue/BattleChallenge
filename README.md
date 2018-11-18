# Game of Thrones Battle Api Challenge


Project is hosted on Amazon Web Service

URL = http://13.127.163.244:3000/api/battle/list


FOR API OF THIS CHALLENGE

API are hosted on Amazon Web Service

**GET LOCATION API**

URL = http://13.127.163.244:3000/api/battle/list
Returns the list of distinct battle location

**GET BATTLE COUNT API**

URL = http://13.127.163.244:3000/api/battle/count
Returns total battle count


**GET STATS**

URL = http://13.127.163.244:3000/api/battle/stats
- Returns Battle stats.
- Response
```
{
    "most_active": {
        "attacker_king": "Joffrey/Tommen Baratheon",
        "defender_king": "Robb Stark",
        "name": "Battle of Moat Cailin",
        "region": "The Riverlands"
    },
    "defender_size": {
        "min": 100,
        "max": 20000,
        "avg": 6428.1578947368425
    },
    "battle_type": [
        "siege",
        "ambush",
        "pitched battle"
    ],
    "attacker_outcome": {
        "win": 32,
        "loss": 5
    }
}
```

**SEARCH**

URL = http://13.127.163.244:3000/api/battle/search 
Generic search allows you to search with any attribute.
king = `attacker_king` or `defender_king` (rest of the attributes have a one to one mapping)
Eg: http://13.127.163.244:3000/api/battle/search?king=Robb Stark&location=Golden Tooth&battle_type=pitched battle

##To run this project locally on your system

1) Download and unzip or clone the url  
2)  run `npm install`  
3)  change the api in src/dataservice.ts to the api given below
4)  The api should be up and running on http://localhost:9001 
 http://localhost:9001/api/battle/list
 http://localhost:9001/api/battle/count
 http://localhost:9001/api/battle/stats
 http://localhost:9001/api/battle/search
 http://localhost:9001/api/battle/search?king=Robb Stark

 ## Note
MongoDb should be running on your system and data should be uploaded to...
DB name `got-battle`
Collection name `battle`

Now go  to src folder
1) Run ng serve

The project ui should run on localhost:4200 



