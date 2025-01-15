# 抖音a_bogus算法

适用抖音，巨量百应等平台

## 验证(需梯子）

### post接口
请求参数
- url --- 你请求的url参数 // 不包含host、pathname
- ua -- 你的user_agent

响应
```json
{
    "abogus": "mX4RhFyyxZ%2FRFRZuYKGA7rQl4oEArNWyAMT%2FKDNJexz3Gh0Ghx1Yj3SrjxwNswgSN8Bvqq37VnUlYEnc%2FM4w1CnpwmpDS04yk%2F%2FcIWmLhHL0TPvhHrL0KibNHJac%2FRYLa%2F1GxVDms4Vn3weg9IqtBBAy7KJeWf%3D%3D",
    "payload": {
        "url": "aid=6383&msToken=Y1dCVyPt10vSv0dNhFExofq6Q9pPcbDAdKY88e163MNaSTET_0AsYL7xmdtbcaBSS0Q_yTrwMRiOxR18MH5eOaHx6Fcn2pSdrASUd08_wiOMGzAnc6rsOF9F6Ed91z6H32mF1maT1dWDQBYiXO49nftpX-J-UV9Pwg%3D%3D&verifyFp=verify_m5waplio_rQkLsJdm_7dop_4b5y_BG4z_ba1jvNlzcJZe&fp=verify_m5waplio_O757fIuI_I3G6_4ez3_996z_okqRmhWe0qrQ",
        "ua": "Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.93 Safari/537.37"
    }
}
```

返回abogus拼上你的url参数即可
  
#### curl
```shell
curl 'https://abogus.spoon123.workers.dev/' \
  --data-raw '{"url":"aid=6383&msToken=Y1dCVyPt10vSv0dNhFExofq6Q9pPcbDAdKY88e163MNaSTET_0AsYL7xmdtbcaBSS0Q_yTrwMRiOxR18MH5eOaHx6Fcn2pSdrASUd08_wiOMGzAnc6rsOF9F6Ed91z6H32mF1maT1dWDQBYiXO49nftpX-J-UV9Pwg%3D%3D&verifyFp=verify_m5waplio_rQkLsJdm_7dop_4b5y_BG4z_ba1jvNlzcJZe&fp=verify_m5waplio_O757fIuI_I3G6_4ez3_996z_okqRmhWe0qrQ","ua":"Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.93 Safari/537.37"}' \
```
#### python
```python
import requests

data = {
    "url": "aid=6383&msToken=Y1dCVyPt10vSv0dNhFExofq6Q9pPcbDAdKY88e163MNaSTET_0AsYL7xmdtbcaBSS0Q_yTrwMRiOxR18MH5eOaHx6Fcn2pSdrASUd08_wiOMGzAnc6rsOF9F6Ed91z6H32mF1maT1dWDQBYiXO49nftpX-J-UV9Pwg%3D%3D&verifyFp=verify_m5waplio_rQkLsJdm_7dop_4b5y_BG4z_ba1jvNlzcJZe&fp=verify_m5waplio_O757fIuI_I3G6_4ez3_996z_okqRmhWe0qrQ",
    "ua": "Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.93 Safari/537.37"
}

response = requests.post('https://abogus.spoon123.workers.dev/', json=data)
res_json = response.json()
print("res", res_json)
print(res_json.get('abogus'))

```
