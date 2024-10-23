# Java04-流程控制

### 1.

> 查询可知，闰年的判定规则是：
>
> 如果年份能被4整除但不能被100整除，则是闰年；
>
> 如果能被400整除，则也是闰年。

```java
//这个函数用于判断传入的年份是否为闰年
//是闰年返回1，不是闰年返回2
bool isLeapYear(int year){
    if( (year%4==0&&year%100!=0) || (year%400==0) )
        return 1;
    else
        return 2; 
}
```

### 2.

```java
//这个函数打印一个高度为n的空心菱形，保证n为奇数
//如n=5,则打印如下图形：
//  *
// * *
//*   *
// * *
//  *
void print(int n){
    int blank_num=(n-1)/2;//循环外引入变量`blank_num`表示空格数

    // 打印上半部分
    for(int i=0;i<(n+1)/2;i++){
        //第i+1行
        for(int j=0;j<blank_num;j++){
            System.out.print(" "); // 打印左边*前空格
        }
        System.out.print("*"); // 打印左边的*
        if(i>0){//排除第一行
            for(int j=0;j<(n-2-2*blank_num;j++){
                System.out.print(" "); // 打印中间的空格
            }
            System.out.print("*"); // 打印右边的星号
		}
                
        System.out.println(); // 换行
        blank_num--;            
    }

    // 同理，打印下半部分,
    blank_num=1; // 重置空格数
                
    for(int i=（n+1)/2;i>=0;i--){
        for(int j=0;j<blank_num;j++){
            System.out.print(" ");
        }
        System.out.print("*");

        if(i>0) {
            for(int j=0;j<2*i-1;j++){
                System.out.print(" ");
            }
            System.out.print("*");
        }

        System.out.println();
        blank_num++;
    }
}
```

