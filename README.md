# Headers_API
```

Link Giao diện : https://www.figma.com/file/OCp7QIpYscWwBGECCQlYnB/Fitness-Calculator?type=design&node-id=0-1&mode=design&t=GOIK6TaJHW7xzbMp-0


#API GET DANH SÁCH HOẠT ĐỘNG
const options = {
  method: 'GET',
  url: 'https://fitness-calculator.p.rapidapi.com/activities',
  params: {
    intensitylevel: '1' // Truyền bằng 1
  },
  headers: {
    'X-RapidAPI-Key': '235cc78a3amshf3d2575cef0c6ffp163219jsnd73c7623ede3',
    'X-RapidAPI-Host': 'fitness-calculator.p.rapidapi.com'
  }
};

Response
{
    "status_code": 200,
    "request_result": "Successful",
    "data": [
        {
            "_id": "61732979343c73779c42093f",
            "id": "ho_16",  //Id hoạt động
            "activity": "home activities",  //Tên hoạt đông
            "metValue": "1.8",
            "description": "wash dishes, standing or in general (not broken into stand/walk components)", // Mô tả
            "intensityLevel": 1
        },
        ]
}
#API GET CALO Theo Hoạt động

const options = {
  method: 'GET',
  url: 'https://fitness-calculator.p.rapidapi.com/burnedcalorie',
  params: {
    activityid: 'ho_16', // ID get từ hoạt động
    activitymin: '25', // Truyền cố định
    weight: '75' // Cân năng cá nhân
  },
  headers: {
    'X-RapidAPI-Key': '235cc78a3amshf3d2575cef0c6ffp163219jsnd73c7623ede3',
    'X-RapidAPI-Host': 'fitness-calculator.p.rapidapi.com'
  }
};
Response
{
    "status_code": 200,
    "request_result": "Successful",
    "data": {
        "burnedCalorie": "56.25",
        "unit": "calorie"
    }
}


#API TÍNH CHỈ SỐ API

const options = {
  method: 'GET',
  url: 'https://fitness-calculator.p.rapidapi.com/bmi',
  params: {
    age: '25', // Truyền tuổi của bản thân
    weight: '65', // Cân nặng
    height: '180' // Chiều cao
  },
  headers: {
    'X-RapidAPI-Key': '235cc78a3amshf3d2575cef0c6ffp163219jsnd73c7623ede3',
    'X-RapidAPI-Host': 'fitness-calculator.p.rapidapi.com'
  }
};

Response
{
    "status_code": 200,
    "request_result": "Successful",
    "data": {
        "bmi": 20.06,
        "health": "Normal",
        "healthy_bmi_range": "18.5 - 25"
    }
}
```


