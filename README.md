# near-example

    // 部署
    near deploy --wasmFile target/wasm32-unknown-unknown/release/music_nft.wasm --accountId abel03-test.testnet

    // 合约地址
    https://explorer.testnet.near.org/transactions/Ec8p4SCSVoQfXP2cDA56TXVthL9V65tc2eiTffxE9jJP
    

    // init 
    near call abel03-test.testnet new_default_meta '{"owner_id": "abel03-test.testnet"}' --account-id abel03-test.testnet

    // nft_mint
    near call abel03-test.testnet nft_mint '{"token_id": "1", "token_owner_id": "'abel-test03.testnear'", "token_metadata": { "title": "Olympus Mons", "description": "Tallest mountain in charted solar system", "copies": 1}}' --account-id abel03-test.testnet


    // 添加存证
    near call abel-test.testnet insert_claim '{"claim": "music-hash01"}' --account-id abel02-test.testnet
    
    // 查看存证
    near call abel-test.testnet get_claim_owner_id '{"claim": "music-hash01"}' --account-id abel02-test.testnet
    
    // 撤销存证
    near call abel-test.testnet revoke_claim '{"claim": "music-hash01"}' --account-id abel02-test.testnet
    
    // 转移存证
    near call abel-test.testnet transfer_claim '{"claim": "music-hash01","to":"abel01-test.testnet"}' --account-id abel02-test.testnet