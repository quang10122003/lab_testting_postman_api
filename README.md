# API Testing Report
# Mục tiêu kiểm thử
Mục tiêu của việc kiểm thử là xác định tính đúng đắn của các endpoint trong Random Data API phiên bản 2.
# Lựa chọn API và phân tích tài liệu: random data api : https://random-data-api.com/api/v2/ 

# sử dụng api ko có endpoint  (https://random-data-api.com/api/v2/) sử dụng phương thực get 
![anh1](https://github.com/quang10122003/lab_testting_postman_api/assets/124878902/7556ca88-fd2f-4504-9ee9-3bae41b2cfb9)
- api trả về status 404 lỗi 
- lỗi ko có endpoint
# Lấy thông tin người dùng ngẫu nhiên.
- sử dụng endpoint users 
- url: https://random-data-api.com/api/v2/users
![anh2](https://github.com/quang10122003/lab_testting_postman_api/assets/124878902/21469e75-250e-4254-a340-897593c22861)
 - api trả về status 200 tức trạng thái ok tức là không lỗi
 - phương thức sử dụng : GET 
 - api trả về Response: 
 {
    "id": 815,
    "uid": "3c0e01e7-f16c-4c70-ab6b-23deef2980cc",
    "password": "jyUwp30Idh",
    "first_name": "Daphne",
    "last_name": "Wisoky",
    "username": "daphne.wisoky",
    "email": "daphne.wisoky@email.com",
    "avatar": "https://robohash.org/omniseosrerum.png?size=300x300&set=set1",
    "gender": "Non-binary",
    "phone_number": "+1-473 186-101-9349 x2371",
    "social_insurance_number": "515501310",
    "date_of_birth": "1995-10-03",
    "employment": {
        "title": "Regional Technology Orchestrator",
        "key_skill": "Communication"
    },
    "address": {
        "city": "New Apryl",
        "street_name": "Fernanda Station",
        "street_address": "149 Christiansen Manor",
        "zip_code": "72716",
        "state": "Colorado",
        "country": "United States",
        "coordinates": {
            "lat": -29.1148015279734,
            "lng": -80.78316893885224
        }
    },
    "credit_card": {
        "cc_number": "6771-8922-8357-6910"
    },
    "subscription": {
        "plan": "Platinum",
        "status": "Blocked",
        "payment_method": "Paypal",
        "term": "Monthly"
    }
}
- kiểm thử ko lỗi 
# thêm thông tin của người dùng ngẫn nhiên 
- url: https://random-data-api.com/api/v2/users
![anh3 ](https://github.com/quang10122003/lab_testting_postman_api/assets/124878902/d8e32c44-a26b-4b21-9e3f-46b677066d73)
- thêm 1 user: 
{
    "id": 814,
    "uid": "3c0e01e7-f16c-4c70-ab6b-23deef2980cc",
    "password": "jyUwp30Idh",
    "first_name": "quang",
    "last_name": "cuon",
    "username": "daphne.wisoky",
    "email": "daphne.wisoky@email.com",
    "avatar": "https://robohash.org/omniseosrerum.png?size=300x300&set=set1",
    "gender": "Non-binary",
    "phone_number": "+1-473 186-101-9349 x2371",
    "social_insurance_number": "515501310",
    "date_of_birth": "1995-10-03",
    "employment": {
        "title": "Regional Technology Orchestrator",
        "key_skill": "Communication"
    },
    "address": {
        "city": "New Apryl",
        "street_name": "Fernanda Station",
        "street_address": "149 Christiansen Manor",
        "zip_code": "72716",
        "state": "Colorado",
        "country": "United States",
        "coordinates": {
            "lat": -29.1148015279734,
            "lng": -80.78316893885224
        }
    },
    "credit_card": {
        "cc_number": "6771-8922-8357-6910"
    },
    "subscription": {
        "plan": "Platinum",
        "status": "Blocked",
        "payment_method": "Paypal",
        "term": "Monthly"
    }
}
- sử dụng method: post 
- status: 404
- dự đoán nguyên nhân lỗi : api ko hỗ trợ phương thức post cho endpoint users

# xóa thông tin của người dùng ngẫn nhiên 
- url: https://random-data-api.com/api/v2/users
![anh4](https://github.com/quang10122003/lab_testting_postman_api/assets/124878902/07a34ea9-a734-40c1-8658-a5230df8a9a6)
- sử dụng method: delete 
- status: 404
- dự đoán nguyên nhân lỗi : api ko hỗ trợ phương thức delete cho endpoint users

# Lấy thông tin ngân hàng ngẫu nhiên.
![anh5](https://github.com/quang10122003/lab_testting_postman_api/assets/124878902/98191898-f326-443b-97a8-ada469f200a7)
- sử dụng endpoint banks 
- url: https://random-data-api.com/api/v2/banks
- api trả về status 200 tức trạng thái ok tức là không lỗi
- phương thức sử dụng : GET 
- api trả về Response: 
 {
    "id": 9142,
    "uid": "1cff7ad2-1061-400f-bc7c-0e47a8758763",
    "account_number": "0188399853",
    "iban": "GB67GYAX94569565548446",
    "bank_name": "ALLIED BANK PHILIPPINES (UK) PLC",
    "routing_number": "107054551",
    "swift_bic": "BOFAGB22CLS"
}
- kiểm thử ko lỗi 
# thêm và xóa ngân hàng ngẫu nhiên
- sử dụng endpoint banks 
- url: https://random-data-api.com/api/v2/banks
- api trả về status 404 tức trạng thái ok tức là không lỗi
- phương thức sử dụng : post và delete  
![anh6](https://github.com/quang10122003/lab_testting_postman_api/assets/124878902/ebcbc725-1284-4c7b-8626-d2d41c550cca)

![anh7](https://github.com/quang10122003/lab_testting_postman_api/assets/124878902/a7a09a4b-2927-451b-8e5e-746381ba8415)

- status : 404 
- dự đoán lỗi: endpoint k hỗ trợ method delete and post
