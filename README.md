# cafemamba
REST API for Cafe Mamba

### 2 ways to use the API
> Local Install
* Clone the Repo
* cd to cafemamba directory
* run ```sh
npm install
```
* run ```sh
npm start
```

> Docker Image
* Pull the latest Docker Image 
```sh
$ docker pull dhawalrank/cafemamba
```
* Run the image
```sh
$ docker run dhawalrank/cafemamba
```

### API Calls
* GET /api/drinks -> get all drinks
* POST /api/drinks -> add a new drink 
* GET /api/drinks/$name -> Get drinks matching the $name
* DELETE /api/drinks/$name -> Delete drinks matching $name
* GET /api/drinks?date=$date -> Get all drinks available on $date
* GET /api/drinks?offset=$offset&count=$count -> Get all drinks starting from position $offset(default 0) upto $count(default 10)

### Drinks Model
* id -> unique, autogenerated mongo Object ID
* name -> String, unique, required
* type -> String, optional
* price -> String, required
* startDate -> String, required
* endDate -> String, required
* contents -> String, optional

### Sample Document
```sh
{
    "_id": "5abf0251f36d287dbca44a36",
    "name": "Oolong Tea Latte",
    "type": "Bubble Tea",
    "price": "6.65",
    "startDate": "2017/11/27",
    "endDate": "2018/11/27",
    "contents": "latte,tapioca,water,oolong tea,tea,sugar"
}
```