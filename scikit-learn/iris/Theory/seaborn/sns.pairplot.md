[**pairplot**](https://seaborn.pydata.org/generated/seaborn.pairplot.html)

1. data*,  데이터 프레임
2.  *hue=None*, 특정 feature를 다른 색으로 매핑해준다
3. *hue_order=None*,  적용되는 색상의 순서를 지정한다 =['a','b']
4. *palette=None*, 전체 테마
5. *vars=None*, 보고 싶은 컬럼만 적어서 제한시킨다 
   1. vars = ['a' , 'b'] 이면 a,b feature만 보여준다
6. *x_vars=None*, 
7. *y_vars=None*, 
8. *kind='scatter'*, *{‘scatter’, ‘kde’, ‘hist’, ‘reg’}* 그래프 종류
9. *diag_kind='auto'*, *{‘auto’, ‘hist’, ‘kde’, None}* 대각선에 있는 그래프의 종류
   1. kde =[Kernel Density Estimation]()
   2. 관측된 데이터들의 분포로부터 원래 변수의 (확률) 분포 특성을 추정하고자 하는 것이 density estimation(밀도추정)이다.
10. *markers=None*, 점 모양 'o', 'x', '+', 'D'등등으로 지정
11. *height=2.5*, 그래프의 크기 조절
12. *aspect=1*, 각 면의 너비(인치)
13. *corner=False*, *d*  대각선을 기준으로 대칭인데 True의 경우 한쪽만 남게 된다
14. *ropna=False*, 그리기 전에 null값 삭제 여부
15. *plot_kws=None*, 투명도 설정
16. *diag_kws=None*, 
17. *grid_kws=None*, *size=None*)

