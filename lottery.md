# 题目：某公司假设有300名员工，开年会抽奖，奖项如下：
# 一等奖3名：泰国5日游
# 二等奖6名：Iphone手机
# 三等奖30名：小型空气净化剂一盒
# 抽奖规则：
# 1.共抽三次，第一次抽三等奖，第二次抽二等奖，第三次压轴抽一等奖。
# 2.每个员工限中奖一次，不得重复。
# 准备员工列表
# 准备中奖计划
# 一共抽三次奖
# 准备中奖人数列表
# 打印中奖人员名单
# 从总的员工列表中踢出中奖人员

import random
yg = []
for i in range(1,301):
    yg.append(f'员工{i}')
zj=[30,6,3]
count=0
while count<3:
    choice=input(f'正在进行{3-count}等奖的抽取')
    winner=random.sample(yg,zj[count])
    print(winner)
    
    for p in winner:
        yg.remove(p)

    count+=1
print(yg)
