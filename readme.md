
相信每一个码农的内心都向往一个自己的团队，这个团队所向披靡，攻无不克，不管在团队协作上还是工作上都能展现出无限的能量，像自己的一个小家庭一样。

1.工作制度

2.代码制度
变量全部用let和const 如果必须设置全局变量，书写规则全部大写，设置在独立的代码块中。
条件控制语句 如果只有一行，可以不加代码块
结束必须以分号做结尾
不要设置全局变量
在同一个数组内不许放入不同类型的对象
将通用的代码封装成Function
避免使用delete关键字，这会对V8的性能有影响，可以用null代替。
当某些对象具有相同的属性的时候，尽可能的为他们创建一个构造函数，这样V8的性能会有所提升
尽量用forEach代替for，避免使用for-in,如果对数组中的值做操作的画，尽可能的使用map

在async/await中，视情况使用Promise.all 例如：：
// bad
async function someAsyncFunc() {
    const user = await asyncGetUser();
    const categories = await asyncGetCategories();
    const mapping = await asyncMapUserWithCategory(user, categories);
}
 
// good
async function someAsyncFunc() {
    const [user, categories] = await Promise.all([
        asyncGetUser(),
        asyncGetCategories()
    ]);
    const mapping = await asyncMapUserWithCategory(user, categories);
}
没必要的串行变成并行


3.交流制度