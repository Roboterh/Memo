### 会话的管理

- `tmux ls` : 查看所有tmux会话 快捷键 ctrl+b s
- `tmux new -s <session_name>` : 创建一个新的会话
- `tmux rename-session -t <old_name> <new_name>` 快捷键 ctrl+b $
- `tmux detach` 分离会话 快捷键 ctrl+b d
- `tmux attach -t <session_name>` 重新连接会话
- `tmux kill-session -t <session_name>` 杀死会话

### 窗格的布局

- `tmux split` 划分上下两个窗格 快捷键 ctrl+b "
- `tmux split -h` 划分左右两个窗格 ctrl+b %
- `ctrl+b x` 关闭当前窗格
- `tmux select-pane -U` 光标切换到上面窗格 快捷键 ctrl+b ↑ 其他移动类似

### 窗口的操作

- `ctrl+b c` 创建新窗口
- `ctrl+b &` 关闭当前窗口
- `ctrl+b number` 切换到指定窗口
- `ctrl+b p` 切换到上一窗口
- `ctrl+b n` 切换到下一窗口
- `ctrl+b w` 通过窗口列表切换窗口
- `ctrl+b ,` 重命名窗口
- `ctrl+b .` 修改当前窗口编号
- `ctrl+b f` 在所有窗口中查找指定文本

### 小技巧

1. 在使用 rz/sz卡死的情况
> 按住ctrl, 连续单击五次x

2. 使用鼠标点击的方式移动窗格和进行操作
> 首先准备配置文件，也即是`${HOME}/.tmux.conf`，在其中添加`set -g mouse on`，之后就是将配置文件进行加载
`tmux source tmux.conf`, 最后就能够成功使用
