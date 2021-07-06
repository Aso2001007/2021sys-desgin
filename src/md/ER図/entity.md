```stratuml
@startuml


!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue
package "ECサイト" as target_system {
entity "顧客マスタ" as Entity01 <m_customers> <<M,MASTER_MARK_COLOR>> {
+ customer_code [PK]
--
pass
name
}



entity "購入テーブル" as Entity02 <d_purchase> <<T,TRANSACTION_MARK_COLOR>> MAIN_ENTITY {
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
