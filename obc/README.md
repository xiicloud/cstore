# obc-env
github.com/hyperledger/fabric  Environment



# cli

peer chaincode deploy -p github.com/hyperledger/fabric/examples/chaincode/go/chaincode_example02 -c '{"Function":"init", "Args": ["a","100", "b", "200"]}'

a5389f7dfb9efae379900a41db1503fea2199fe400272b61ac5fe7bd0c6b97cf10ce3aa8dd00cd7626ce02f18accc7e5f2059dae6eb0786838042958352b89fb


peer chaincode query -n a5389f7dfb9efae379900a41db1503fea2199fe400272b61ac5fe7bd0c6b97cf10ce3aa8dd00cd7626ce02f18accc7e5f2059dae6eb0786838042958352b89fb -p github.com/hyperledger/fabric/examples/chaincode/go/chaincode_example02 -c '{"Function":"query", "Args": ["a"]}'

100



peer chaincode invoke -n a5389f7dfb9efae379900a41db1503fea2199fe400272b61ac5fe7bd0c6b97cf10ce3aa8dd00cd7626ce02f18accc7e5f2059dae6eb0786838042958352b89fb -p github.com/hyperledger/fabric/examples/chaincode/go/chaincode_example02 -c '{"Function":"notdelete", "Args": ["a", "b", "20"]}'

3d44e663-0acb-46c5-8b8e-5d8d43fbd471


peer chaincode query -n a5389f7dfb9efae379900a41db1503fea2199fe400272b61ac5fe7bd0c6b97cf10ce3aa8dd00cd7626ce02f18accc7e5f2059dae6eb0786838042958352b89fb -p github.com/hyperledger/fabric/examples/chaincode/go/chaincode_example02 -c '{"Function":"query", "Args": ["a"]}'

200




peer chaincode deploy -p github.com/hyperledger/fabric/examples/chaincode/go/chaincode_example02 -c '{"Function":"init", "Args": ["c","10", "d", "2000"]}'

598e4e2cefd0d806251971f1ac83e3a29424e4bc536174f95daaf696da47ba87379994bc2160fe6239d0f7fc80ca43d7dfdd5c768b153c18dcd5792ae357a0b3



peer chaincode query -n 598e4e2cefd0d806251971f1ac83e3a29424e4bc536174f95daaf696da47ba87379994bc2160fe6239d0f7fc80ca43d7dfdd5c768b153c18dcd5792ae357a0b3 -p github.com/hyperledger/fabric/examples/chaincode/go/chaincode_example02 -c '{"Function":"query", "Args": ["c"]}'

10