```
@interface student{
          @property(nonatomic, copy) NSString *name;
          @property(nonatomic, copy) NSString *major;
          @property(nonatomic, readonly) NSInteger age;
}

-(void) study:(float)time; 

@end

@implementation student

-(void) study : (float)time
{
    NSLog(@"%f", time);
}
@end

#import <Foundation/Foundation.h>

int main (int argc, const char *argv[])
{

        student * s = [[student alloc] init];
        [s study:3.5];
    return 0;
}
```
