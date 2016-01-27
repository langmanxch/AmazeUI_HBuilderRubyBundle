# AmazeUI_HBuilderRubyBundle

根据AmazeUI官网（http://amazeui.org/getting-started?_ver=2.x）
提供的sublime snippets修改的HBuilder的html snippets

#使用方法：
#1、打开 HBuilder 菜单栏“工具”-->"扩展代码块"-->"自定义html代码块"

#2、将_combinText.sublime-snippet 里的内容复制到 以下粗体字： “自定义代码块”的位置，请注意文件结尾一定要有 end

......
with_defaults :scope => 'text.html text' do |bundle|  =====HTML标签代码块================================================================================
如下是一个示例代码块，可以复制后再添加新代码块
  snippet 'div_class' do |cmd|  #div_class是显示名称，代码助手提示列表显示时可见
    cmd.trigger = 'divc'        #divc是激活字符，即按下divc后会触发该代码块
    cmd.expansion = "<div class=\"$1\">
    $0
</div>"                         #expansion是代码块的输出内容，其中$0、$1是光标的停留和切换位置。$1是第一个停留光标，$0是最后回车时停留的光标。
                                                          #如果输出涉及到换行和tab，也需严格在这里使用换行和tab。
                                                          #输出双引号在前面加\来转义，输出$使用\$(单引号中)或\\$(双引号中)转义
    cmd.needApplyReContentAssist = true  #这句话的意思是输出后同时激活代码助手，即在$1的位置直接拉出样式列表
  end #div_class代码块结束
  
  snippet 'ng-pluralize' do |cmd|
    cmd.trigger = 'ngp'
    cmd.expansion = "<ng-pluralize>$1<-pluralize>"
  end

#自定义代码块
                                                                                                                                                                                      
end  






