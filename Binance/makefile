TWS=../twsapi/IBJts/builds/*.o
Helpers=ApiService.cpp ../strategies/MarketData.cpp TechnicalAnalysis.cpp ../strategies/Strategy.cpp
CFLAGS=-lboost_system -lcrypto -lssl -lcpprest -lpthread
BASE_SRC_DIR=../
INCLUDES=-I${BASE_SRC_DIR}
GPERFTOOLS=-L/usr/local/lib

test:
	g++ -std=c++11 Test.cpp -o Test.exe
binance:
	g++ -std=c++11 $(INCLUDES) $(Helpers) Binance.cpp $(TWS) -o Binance.exe $(CFLAGS)
binance_prof:
	g++ -std=c++11 $(INCLUDES) ${GPERFTOOLS} $(Helpers) Binance.cpp $(TWS) -o Binance.exe $(CFLAGS) -Wl,--no-as-needed -lprofiler -ltcmalloc -Wl,--as-needed
