# Aptos Fixed Price Market


## 合约交互示例

### 批量挂单 batch list transaction

https://explorer.aptoslabs.com/txn/55095677

### 批量购买 batch buy transaction

https://explorer.aptoslabs.com/txn/55050185

### 批量取消挂单 batch delist transaction

https://explorer.aptoslabs.com/txn/55014220


### 批量更改挂单价格 batch change_price transaction

https://explorer.aptoslabs.com/txn/55091778

## 合约交互

souffl3_contract_address: 0xf6994988bd40261af9431cd6dd3fcf765569719e66322c7a05cc78a89cd366d4

| 函数id | 入参泛型 | 入参  |
|------|--|---|
| {{souffl3_contract_address}}::FixedPriceMarket::batch_list_script | 0x1::aptos_coin::AptosCoin |  token_owner: &signer
creator_lists: vector<address>
collection_lists: vector<String>
name_lists: vector<String>
property_version_lists: vector<u64>
token_amount_lists: vector<u64>
coin_amount_lists: vector<u64>
locked_until_secs_lists: vector<u64>
market_address_lists: vector<address>
market_name_lists: vector<String>   |

### Listing payload

```
{
  "function": "0xf6994988bd40261af9431cd6dd3fcf765569719e66322c7a05cc78a89cd366d4::FixedPriceMarket::batch_list_script",
  "type_arguments": [
    "0x1::aptos_coin::AptosCoin"
  ],
  "arguments": [
    [
      "0xf51d0def60d022111012fca89cd8abdb5623db94b8d09037372e4b4c6747dc9e",
      "0xdfad342e78a2f339287bfe7d305887e0fbb9d08d718579280914376ea4331f3b",
    ],
    [
      "Souffl3 BakeOff - Flour",
      "Souffl3 BakeOff - Sugar",
    ],
    [
      "Flour #14423",
      "Sugar #16253",
    ],
    [
      "1",
      "1",
    ],
    [
      "1",
      "1",
    ],
    [
      "100000",
      "100000",
    ],
    [
      "0",
      "0",
    ],
    [
      "0xf6994988bd40261af9431cd6dd3fcf765569719e66322c7a05cc78a89cd366d4",
      "0xf6994988bd40261af9431cd6dd3fcf765569719e66322c7a05cc78a89cd366d4",
    ],
    [
      "souffle",
      "souffle",
    ]
  ],
  "type": "entry_function_payload"
}
```

### Buy

```
{
  "function": "0xf6994988bd40261af9431cd6dd3fcf765569719e66322c7a05cc78a89cd366d4::Aggregator::batch_buy_script_V1",
  "type_arguments": [],
  "arguments": [
    [
      "Souffl3"
    ],
    [],
    [
      "280000000"
    ],
    [
      "1"
    ],
    [
      "0xe7fbaab107f818f91111bde00f31308981fde6236a788bf2c4bbc28d72e97cbb"
    ],
    [
      "Aptos Farmlands"
    ],
    [
      "Farm Land #45"
    ],
    [
      "0"
    ],
    [
      "0xf6994988bd40261af9431cd6dd3fcf765569719e66322c7a05cc78a89cd366d4"
    ],
    [
      "souffle"
    ]
  ],
  "type": "entry_function_payload"
}

```

### delist

```
{
  "function": "0xf6994988bd40261af9431cd6dd3fcf765569719e66322c7a05cc78a89cd366d4::Aggregator::batch_delist_script_V1",
  "type_arguments": [],
  "arguments": [
    [
      "Souffl3"
    ],
    [
      "1"
    ],
    [
      "0x829290d9fc84d4da0db3f9274d7a4bf098630055f996da415c60fc9ebd0ea982"
    ],
    [
      "P-GANG"
    ],
    [
      "P-GANG #123"
    ],
    [
      "0"
    ],
    [
      "0xf6994988bd40261af9431cd6dd3fcf765569719e66322c7a05cc78a89cd366d4"
    ],
    [
      "souffle"
    ]
  ],
  "type": "entry_function_payload"
}
```

### batch_change_price

Arguments 中数组分别为
Creator
Collection
Name
property_version
token_amount
coin_amount
locked_until_secs
market_address
market_name

```
{
  "function": "0xf6994988bd40261af9431cd6dd3fcf765569719e66322c7a05cc78a89cd366d4::Aggregator::batch_change_price_script_V1",
  "type_arguments": [],
  "arguments": [
    [
      "Souffl3"
    ],
    [
      "0x1a79b04bd7c2096ca358351d6e80e4b877d3cdc102af7955addb51dac4dc63eb"
    ],
    [
      "Oishii Moechann"
    ],
    [
      "Oishii Moechann #2803"
    ],
    [
      "1"
    ],
    [
      "1"
    ],
    [
      "45000000"
    ],
    [
      "0"
    ],
    [
      "0xf6994988bd40261af9431cd6dd3fcf765569719e66322c7a05cc78a89cd366d4"
    ],
    [
      "souffle"
    ]
  ],
  "type": "entry_function_payload"
}
```
