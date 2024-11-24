# iterator
Design Pattern - Iterator

說明:

1. Aggregate

    IDepartment 是聚合介面, 定義了getIterator()方法.
    Company 是聚合類別, 使用指定的固定大小的字串陣列來佔儲存部門名稱, 且實作了getIterator()方法.

2. Iterator
    IDepartmentIterator 是走訪器介面, 定義了 hasNext(), next()兩個方法.
    DepartmentIterator 實作了走訪行為 hasNext(), next(), 若有特別的走訪條件, 可在此實作.

3. main() 在執行時, 先是定義了個部分的名稱, 而後使用DepartmentIterator來走訪公司各部門的名稱.


優點:
1. 不依頼集合框架, 使用純陣列來實現走訪行為, 適合於固定大小的集合.
2.  靈活的走訪邏輯, 可擴展走訪行為, 例如條件式的走訪或修件過濾.
3. 簡單易用, 適合小型集合的應用.
