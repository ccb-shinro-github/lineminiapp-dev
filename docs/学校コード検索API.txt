

※メソッドはいずれも GET となります。

認証情報
リクエストヘッダー	値
Authorization	Bearer形式でトークンを指定
トークンの一覧、発行はこちらから
Accept	application/json
学校一覧取得
指定できるパラメータ
項目	必須・
任意	複数項目の
指定可否	説明
pref_code	任意	不可	
都道府県コードを1～47で指定します。
zip_code	任意	不可	
郵便番号を指定します。
ハイフンは含めません。
school_type_code	任意	不可	
「小学校」はB1、「中学校」はC1のように指定します。
school_founder_code	任意	可	
「国立」は1、「公立」は2のように指定します。
複数指定する場合は、school_founder_code=1,2のようにカンマ区切りで指定します。
school_status_code	任意	可	
「本校」は1、「分校」は2のように指定します。
複数指定する場合は、school_status_code=2,9のようにカンマ区切りで指定します。
keyword	任意	可	
検索キーワードを指定します。キーワードは半角または全角スペースで区切って複数指定できます。
複数指定した場合、各キーワードのAND条件で検索されます。
例）「東京都　品川区」
キーワードの区切り文字で半角／全角を混在させないでください。
結果およびページングについて
※以下は説明のために、実際のAPI結果と順序を変更している箇所があります。

{
"schools": {
"data": [
{
"school_code": "G102110100721",
"school_name": "八戸工業高等専門学校",
"school_locate_at": "八戸市大字田面木字上野平１６－１",
"school_type_code": "G1",
"school_type": "高等専門学校",
"zip_code": "0391192",
"pref_code": "02",
"pref": "青森県",
"school_status_code": "1",
"school_status": "本校",
"school_founder_code": "1",
"school_founder": "国立",
"obsolete_school_code": "6516",
"school_code_unique": "292P",
"updated_at": "2021/01/20"
},
...省略...
],
"first_page_url": "https://dev-api.edu-data.jp/api/v1/school?pref_code=02&page=1",
"next_page_url": "https://dev-api.edu-data.jp/api/v1/school?pref_code=02&page=2",
"last_page_url": "https://dev-api.edu-data.jp/api/v1/school?pref_code=02&page=10",
"path": "https://dev-api.edu-data.jp/api/v1/school",
"links": [],
"current_page": 1,
"last_page": 10,
"per_page": 100,
"from": 1,
"to": 100,
"total": 916
}
本APIでは、1回のリクエストで最大100件の結果を取得できます。リクエストした結果が1ページにおさまらない場合は結果がページングされます。次のページがある場合、 next_page_urlパラメータが示されますので、当該URLをAPIリクエストすることで次ページの結果が取得できます。 linksパラメータで、特定ページの結果が取得できます。

学校取得
指定できるパラメータ
項目	必須・任意	説明
school_code	必須	
学校コードを指定します。
結果
{
"school": {
"school_code": "F101110100029",
"school_name": "北海道教育大学",
"school_locate_at": "札幌市北区あいの里５条３－１－３",
"zip_code": "0028501",
"obsolete_school_code": "0104",
"school_type_id": 9,
"school_code_unique": "BPQ2",
"pref": "北海道",
"pref_code": "01",
"school_status": "本校",
"school_status_code": "1",
"school_type_code": "F1",
"school_type": "大学",
"school_founder_code": "1",
"school_founder": "国立",
"updated_at": "2021年01月20日"
}
}