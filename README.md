# near-example

    // 部署
    near deploy --wasmFile target/wasm32-unknown-unknown/release/music_nft.wasm --accountId abel03-test.testnet

    // 合约地址
    https://explorer.testnet.near.org/transactions/Ec8p4SCSVoQfXP2cDA56TXVthL9V65tc2eiTffxE9jJP
    

    // init 
    near call abel03-test.testnet new_default_meta '{"owner_id": "abel03-test.testnet"}' --account-id abel03-test.testnet

    // nft_mint
    near call abel03-test.testnet nft_mint '{"token_id": "3", "token_owner_id": "'abel03-test.testnet'", "token_metadata": { "title": "Olympus Mons", "description": "Tallest mountain in charted solar system", "copies": 1}}' --account-id abel03-test.testnet --deposit 10

    // 转移
    near call abel03-test.testnet nft_transfer '{"token_id": "3", "receiver_id": "abel01-test.testnet", "memo": "transfer ownership"}' --accountId abel03-test.testnet --deposit 0.000000000000000000000001

