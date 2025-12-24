CXX ?= g++

DEBUG ?= 1
ifeq ($(DEBUG), 1)
    CXXFLAGS += -g
else
    CXXFLAGS += -O2

endif

server: ./Source_Code/main.cpp  ./timer/lst_timer.cpp ./http/http_conn.cpp ./log/log.cpp ./CGImysql/sql_connection_pool.cpp  ./webserver/webserver.cpp ./config/config.cpp
	$(CXX) -o server  $^ $(CXXFLAGS) -lpthread -L/usr/lib64/mysql -lmysqlclient 

clean:
	rm  -r server
