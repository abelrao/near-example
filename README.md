# near-example

    // 合约地址
    https://explorer.testnet.near.org/transactions/85dwmYapTgRiDsjGRDTAuBnpsnEdH8T5Z5ASiXEycG35

    // init 
    near call abel01-test.testnet new_default_meta '{"owner_id": "abel01-test.testnet"}' --account-id abel01-test.testnet

    // nft_mint
    near call abel01-test.testnet nft_mint '{"token_id": "1", "token_owner_id": "'abel-test01.testnear'", "token_metadata": { "title": "Olympus Mons", "description": "Tallest mountain in charted solar system", "copies": 1}}' --account-id abel01-test.testnet

    // 部署 
    near deploy --wasmFile target/wasm32-unknown-unknown/release/music_nft.wasm --accountId abel-test.testnet


    // 添加存证
    near call abel-test.testnet insert_claim '{"claim": "music-hash01"}' --account-id abel02-test.testnet
    
    // 查看存证
    near call abel-test.testnet get_claim_owner_id '{"claim": "music-hash01"}' --account-id abel02-test.testnet
    
    // 撤销存证
    near call abel-test.testnet revoke_claim '{"claim": "music-hash01"}' --account-id abel02-test.testnet
    
    // 转移存证
    near call abel-test.testnet transfer_claim '{"claim": "music-hash01","to":"abel01-test.testnet"}' --account-id abel02-test.testnet