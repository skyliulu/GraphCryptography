# 哈希函数

哈希函数将文本或二进制数据转换为固定长度的散列值，并且要具有抗冲突性和不可逆性。
- 抗冲突
  - 意味着输入不同，hash函数的输出不同。或者说很难找的两个输入，他们的hash值是一样的。
- 不可逆
  - 计算hash值很容易，但是根据hash值推断出hash函数的输入很难，其概率是可忽略的。
```mermaid
graph LR
    subgraph 抗冲突
        A("hash(x)") -- easy --> B(y)
        C("hash(x')") -- very hard --> B
    end
    subgraph 不可逆
        B1 -- very hard --> A1
        A1("hash(x)") -- easy --> B1(y)
    end    
```

## 常用的哈希算法
现在密码学是不断发展的，没有绝对安全的哈希算法。过去有些常用的哈希算法已经被证明不安全的(MD5、SHA0、SHA1),有些现在仍然被认为是安全的，比如SHA-2，SHA-3和BLAKE2。但这并不意味着以后这些算法依然安全。
### 目前安全的哈希算法
- SHA-2, SHA-256, SHA-512
- SHA-3, SHA3-256, SHA3-512, Keccak-256
- BLAKE2, BLAKE2s , BLAKE2b


