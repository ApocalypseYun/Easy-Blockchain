# Easy-Blockchain

## 块内信息

一个区块中应当保存当前块的索引（index）、时间戳（timestamp）、数据（data）、前块哈希的加密哈希（previous_hash）。同时声明一个hash_block函数用于加密。

## Hash加密函数

首先构造一个使用sha256（安全哈希算法）的hash对象sha ，然后将区块信息通过update() 函数加入sha这一hash对象。这里我遇到了一个问题，就是在使用update() 函数时要确认其更新的数据的编码形式，于是使用encode() 函数确认数据为 “utf-8” 编码形式。最后通过hexdigest() 函数返回hash 对象的 hash 值。

## 创建创世区块

创建创世区块。

## 创建后续区块

这个函数将把链中的前一个块作为参数，创建要生成的块的数据，并使用适当的数据返回新块。当新的块哈希信息来自前面的块时，区块链的完整性会随着每个新块而增加。如果不这样做，外部组织就更容易“改变过去”，用全新的方式取代已有的链条。这一系列的散列可以作为加密的证据，有助于确保一旦将块添加到区块链，它就不能被替换或删除。

## 测试程序

列表的第一个为创世区块，之后我们通过for循环创建20个区块，为了更加直观的展示区块的创建。当每一个区块创建后我们通过Print来展示其中相关的数据。如：
Block #1 has been added to the blockchain!
Hash: cd16fdc26fa300e5bdb0d9232790628c35a175b4f717b4d90c8cc2d177d5a78b

## 测试结果
运行成功，成功创建了20个去块：
Block #1 has been added to the blockchain!
Hash: cd16fdc26fa300e5bdb0d9232790628c35a175b4f717b4d90c8cc2d177d5a78b

Block #2 has been added to the blockchain!
Hash: 1de3821ed68c09a2d1432e04900d28dd0f4d2396f5008e7ae89bb61fe7298855

Block #3 has been added to the blockchain!
Hash: 07b9bdb9133f7b84d14073c12e0f8d0b0a4eb6ad3490033fe29ae87bea25417a

Block #4 has been added to the blockchain!
Hash: 3bf1adad5bcbb1ace515ce382269387f6c4ea27d5ece7fe0a094b10ef377fa45

Block #5 has been added to the blockchain!
Hash: b44bef3cff660018926d70bc28ede564bdaf5a4b88aa5b3086cd9fbfea551af9

Block #6 has been added to the blockchain!
Hash: 8a60514e5db6443e6721285891c06a8e76eb9d8e7853a360344b213d4d149eda

Block #7 has been added to the blockchain!
Hash: d1e77e1711311bb2a6d6f2cbb1c492559df2839242bde862dbbde638c41103a9

Block #8 has been added to the blockchain!
Hash: 077368b3d4ab63971533bbbcc2aa0c3381d7efcd6466c542d25cfd1964dd1d5f

Block #9 has been added to the blockchain!
Hash: 278857a8adc0258043f90b7ef5c2522f8ee2ae546aa0993448e09bd0f3d643fd

Block #10 has been added to the blockchain!
Hash: cc5ae7de20c53c3d9d96548c59cc42af2f5fcb49d2e34cceb39e0c990ff6bf57

Block #11 has been added to the blockchain!
Hash: 1db37ab51ec47e102984e061234234b84c7807fa71687f16a225f8731852b97d

Block #12 has been added to the blockchain!
Hash: 0ffe55135b795cd29467145c679b80f1d96d7f34f72eb9168c59d98f161683a5

Block #13 has been added to the blockchain!
Hash: 860a62f7ce0d0a8fff012b0b67dcbf3bf49fbd58ac7af1d55dac94011391b963

Block #14 has been added to the blockchain!
Hash: 86823c316d05ed1ec41f409810aa935d7a751cd3389c1fcc70dff7f0d288ad67

Block #15 has been added to the blockchain!
Hash: 7c36192d245885e111fd812166d025ab23f32ccb1452178bdf8ee81000e74cb1

Block #16 has been added to the blockchain!
Hash: c0d5c5b681f29bfab26bbc0c17462c44b59eda7434fe1902b18ca12a30fb23a7

Block #17 has been added to the blockchain!
Hash: ba44ee6388dbf7c15227d1d27b2eb631568d825c0affcbe6edef96c58e8ceec5

Block #18 has been added to the blockchain!
Hash: 54447cebe883c972927ca7abe9f5def642d4b21c16550ccfb16d583c8d6fdf71

Block #19 has been added to the blockchain!
Hash: 9f1b41a46dd7200b134037751a97ec92cd07118ae5ccb53a70ec8ae93a5363f2

Block #20 has been added to the blockchain!
Hash: 0cfb478d9fb2bbe67b400bb2d8be210f896e09713ec820254e49a88ffb85de0d

[Finished in 0.2s]
