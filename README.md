# TiShiCiZhushou
# todolist
补齐剩余的提示词等内容

文献综述能不能用代码自动生成这些文件目录，并且放在目标文件夹下？并且是打开那个我设置好的的Doxt文件

希望能实现程序自动识别该论文中的各小节的题目，然后自动填空，我现在正在写第几章xx的第几节xxx

针对性的提示词增加按钮
把之前的论文一个个检查一遍，差的提示词补上
## 25.9.4
提示词大部分都已经补齐了
增加了提示文本的功能
## 25.9.3
开题报告部分的内容搞完了，后面部分的提示词以及文本复制功能都只需要按着框架来就行
增加功能：输入框中一次性输入专业，学历和题目然后自动识别并填入对应的框中
各部分的子导航栏能出现在正确的位置
增加了回到顶部按钮
==
                <!-- 文本复制完善：
                    1,复制框架后 修改id和title 
                    2,搜索id：copySectionTitleBtn 查看另一处要改的内容
                    【实际操作：另一处复制框架后 修改第一个id之后AI会自动完成剩余内容】
                -->

                    <button id="" class="ml-3 text-primary hover:text-blue-700 text-base" title="">
                            <i class="fa fa-copy"></i>
                    </button>

==
                <!-- 提示词完善：
                    1,复制框架后 修改id和data-group  （data-group = id去掉Prompt） 
                    2,增加activePrompts和basePrompts的内容
                    【实际操作：修改注释之后回车AI会自动完成剩余内容】
                -->
                <!-- 部分 -->
                <div class="mt-8">
                    <h3 class="text-lg font-semibold mb-4 flex items-center">
                        <span class="inline-block w-6 h-6 rounded-full bg-primary text-white text-sm flex items-center justify-center mr-2"></span>
                        
                    </h3>

                    <div class="bg-neutral p-4 rounded-lg mb-4 relative">
                        <div class="flex flex-wrap gap-2 mt-2">
                            <button class="prompt-btn bg-white text-xs px-2 py-1 rounded border border-gray-300 hover:bg-gray-50 btn-effect" data-prompt="请分点阐述，但不要使用数字序号" data-group="">
                                <i class="fa fa-list text-primary mr-1"></i>分点阐述
                            </button>
                        </div>
                        <pre id="" class="text-sm whitespace-pre-line">提示词</pre>
                    </div>

                    <div class="flex justify-end">
                        <button class="copy-btn bg-primary text-white px-4 py-2 rounded-lg flex items-center btn-effect" data-target="">
                            <i class="fa fa-copy mr-2"></i>关键词
                        </button>
                    </div>
                </div>
==
                    <!--  -->

==
                    <!-- 永久显示的提示文本 -->
                    <span class="ml-3 text-sm text-gray-500">
                        <i class="fa fa-info-circle mr-1"></i>删除每段最后的总结语句
                    </span>
==
                    <div>
                        <label for="" class="block text-sm font-medium text-gray-700 mb-1">请输入专业major</label>
                        <input type="text" id="" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary/50 focus:border-primary outline-none transition-all" placeholder="例如：计算机科学与技术">
                    </div>