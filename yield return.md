yield return 是 C# 中用來實現延遲執行 (lazy evaluation) 的關鍵字，可以用來產生一個可列舉 (enumerable) 的序列，而不必等到所有元素都計算完畢才返回結果。
```cs
public static IEnumerable<int> GenerateNumbers()
{
    for (int i = 1; i <= 10; i++)
    {
        yield return i;
    }
}

foreach (int number in GenerateNumbers())
{
    Console.WriteLine(number);
}
```
需要注意的是，使用 yield return 來實現延遲執行時，方法的返回類型必須是 IEnumerable 或 IEnumerable<T>
