#### Passenger.h
```
#import "Person.h"

NS_ASSUME_NONNULL_BEGIN

@interface Orders : NSObject

@property(nonatomic, copy) NSString *PassengerName;
@property(nonatomic, copy) NSString *TrainNo;
@property(nonatomic, assign) NSDate *StartDate;
@property(nonatomic, assign) NSDate *EndDate;
@property(nonatomic, copy) NSNumber *SeatNo;

- (instancetype)initOrder:(NSString *) PassengerName trainnumber:(NSString *) TrainNo startdate:(nonnull NSDate *) StartDate enddate:(nonnull NSDate *) EndDate seatnumber:(NSNumber *) SeatNo;


@end

@interface Passenger : Person
// @property 属性
@property(nonatomic, assign) bool if_18; // 是否年满 18 岁

@property(nonatomic, assign) NSMutableArray *HistoryOrders; // 历史订单 （数组）
@property(nonatomic, assign) NSMutableArray *NoTravelOrder  // 未出行订单 （数组）

    // Function 方法
- (void)book : (Orders *)book_order; // 去订票
- (void)check: (Orders *)check_order; // 去检票
@end

NS_ASSUME_NONNULL_END
```

#### Passenger.m
```
#import "Passenger.h"


@implementation Orders

- (instancetype)initOrder:(NSString *) PassengerName trainnumber:(NSString *) TrainNo startdate:(nonnull NSDate *) StartDate enddate:(nonnull NSDate *) EndDate seatnumber:(NSNumber *) SeatNo;
        if(self = [super init]){
        [self createOrder:PassengerName trainnumber:TrainNo startdate:StartDate enddate:EndDate seatnumber:SeatNo];
    }
    return self;

- (void)createOrder:(NSString *) PassengerName trainnumber:(NSString *) TrainNo startdate:(nonnull NSDate *) StartDate enddate:(nonnull NSDate *) EndDate seatnumber:(NSNumber *) SeatNo{
    
    self.PassengerName=PassengerName;
    self.TrainNumber=TrainNumber;
    self.StartTime=StartTime;
    self.EndTime=EndTime;
    self.SeatNumber=SeatNumber;
}

@end

@implementation Passenger

- (bool) if_18{
    return self.age >= 18;
}

- (void) book:(Orders *) book_order{
    [self.NoTravelOrder addObject:book_order];
}

- (void) check:(Orders *) check_order{
    [self.HistoryOrder addObject:check_order];
    [self.NoTravelOrder removeObject:order];
}

@end

```
