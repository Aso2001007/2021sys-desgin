```stratuml
@startuml

package "ECサイト" as target_system {
  entity "顧客マスタ" as Entity01 <m_customers> {
    + customer_code [PK]
    --
    pass
    name
    address
    tel
    mail
    del_flag
    reg_date
  }



  entity "購入テーブル" as Entity02 <d_purchase> {
    + order_id [PK]
    --
    # customer_code [FK]
    purchase_date
    total_price
  }


  entity "購入詳細テーブル" as Entity03 <d_purchase_detail> {
    + order_id [PK]
    + datail_id [PK]
    --
    # item_code [FK]
    price
    num
  }
  
  entity "商品マスタ" as Entity04 <m_items> {
    + item_code [PK]
    --
    item_name
    price
    # category_id [FK]
    image
    detail
    del_flag
    reg_date
  }
  
  entity "カテゴリマスタ" as Entity05 <m_category> {
    + category_id [PK]
    --
    name
    reg_date
  }
  
}

Entity01|-r-{Entity02
Entity02}|-r-||Entity03
Entity03}|-d-||Entity04
Entity04}|-l-||Entity05



@enduml    
```
