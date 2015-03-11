windows下visual studio编译libev:
1. 在vs下添加已存在的项目;
2. 从vs中移除ev_epoll.c, ev_kqueue.c, ev_poll.c, ev_select.c, ev_win32.c几个文件;
3. event.c中要包含winsock2.h头文件; config.h.in复制为config.h, 定义HAVE_SELECT和HAVE_SYS_SELECT_H
4. 加上ws2_32.lib

然后编译就ok了