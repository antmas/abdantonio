# abdantonio

![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/03/Flag_of_Italy.svg/280px-Flag_of_Italy.svg.png)                                                  ![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/59/Flag_of_Lebanon.svg/280px-Flag_of_Lebanon.svg.png)


```c
int main()
{
  int i=0;
  i++;
  return 0;
}
```

```bash
initDATE=$(date)
sleep 3
finDATE=$(date)
d1=$(date -d "`echo $initDATE`" +%s)
d2=$(date -d "`echo $finDATE`" +%s)
S=`(echo $d2-$d1) | bc`
H=`echo "$S/(60*60)" | bc`;R=`echo "($S-3600*$H)" | bc`;M=`echo "$R/60" | bc`;R=`echo "($R-60*$M)" | bc`
      #"   init  : Fri Oct 19 17:14:09 CEST 2018"
printf "                      \e[32m%2.2d:%2.2d:%2.2d\e[39m\n" $H $M $R
```
