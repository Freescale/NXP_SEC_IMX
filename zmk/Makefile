# list of platforms which want this test case
INCLUDE_LIST:= IMX6QP

OBJS = zmk.o

ifeq ($(PLATFORM),$(findstring $(PLATFORM),$(INCLUDE_LIST)))
#TARGET =$(OBJDIR)/zmk
TARGET = zmk
else
TARGET =
endif

all : $(TARGET)

$(TARGET): $(OBJS)
	$(CC) -o $(TARGET) $(OBJS)

.PHONY: clean
clean :
	rm -f $(OBJS) $(TARGET)
