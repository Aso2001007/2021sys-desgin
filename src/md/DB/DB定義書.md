# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001007/2021sys-desgin/blob/main/src/md/ER%E5%9B%B3/entity.md "ER図はこちら")

# DBテーブルカラム詳細一覧
### データベース詳細
*****
 d_purchase
| 属性名 | 型 | PK | NN | FK |
|-------|----|----|----|----|
|order_id|bigint(20)|○|○|-  |
|custimer_code|varchar(50)|- |○|- |
|purchase_date|date|- |○|- |
|total_price|int(11)|- |○|- |

 d_purchase_detail
| 属性名 | 型 | PK | NN | FK |
|-------|----|----|----|----|
|derail_id|bigibt(20)|○|○|- |
|order_id|bigint(20)|○|○|○|
|item_code|int(11)|- |○|- |
|price|int(11)|- |○|- |
|num|int(11)|- |○|- |

 m_custimers
| 属性名 | 型 | PK | NN | FK |
|-------|----|----|----|----|
|customer_code|varchar(50)|○|○|- |
|pass|varchar(50)|○|○|○|
|name|varchar(20)|- |○|- |
|address|varchar(100)|- |○|- |
|tel|varchar(20)|- |○|- |
|mail|varchar(100)|- |○|-|
|del_flag|int(11)|- |- |- |
|reg_date|date|- |○|- |

 m_category
| 属性名 | 型 | PK | NN | FK |
|-------|----|----|----|----|
|category_id|int(11)|○|○|- |
|name|varchar(20)|- |○|- |
