```
@interface student{
     @public
        NSString* name;
        NSString* major;
     @private
        int age;
}

@property(copy) NSString *name;
@property(readonly) int age;
-(void) study:(float)time; // 类方法

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
