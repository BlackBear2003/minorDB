# minorDB ———— 世界上最小的DB

## 安装教程

复制或者拉取两个shell脚本到你的本地

```shell
chmod +x ./dbset.sh 
chmod +x ./dbget.sh 
```

## 使用教程

```shell
# set操作
./dbset.sh "key" "value"

# get操作
./dbget.sh "key"

# 查看所有记录
cat database
```

## 功能评估

### 持久化 

支持持久化，所有数据保存到`database`文件中。

### 写操作

属于log追加写入类型，在保证持久化的情况下性能极高！

### 读操作

使用grep和sed来完成读操作，时间复杂度在O(N)。考虑后续加入参考bitcask实现简单的内存hash索引。



