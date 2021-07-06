```stratuml
@startuml

package "ECサイト" as target_system {
  entity "顧客マスタ" as Entity01 <m_customers> {
    + customer_code [PK]
    --
    pass
    name
  }



  entity "購入テーブル" as Entity02 <d_purchase> {
    + order_id [PK]
    --
    # customer_code [FK]
    purchase_date
    total_price
  }

}

Entity01}|..||Entity02


@enduml    
```
