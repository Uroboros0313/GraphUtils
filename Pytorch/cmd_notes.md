# Notes for Pytorch

## `Tensor.contiguous()`

torch中一些操作会改变原数据——`narrow()`,`view()`,`expand()`,`transpose()`等操作。这些操作pytorch并不会创建新的tensor，而是修改了tensor原地址中的一些元数据。转置的tensor和原tensor的**内存是共享的**——`contiguous`方法就类似深拷贝，使得上面这些操作不会改变元数据

## `torch.randperm(n)`

torch.randperm(random permutation): 将`[0, n-1]`随机打乱后获得的数字序列。