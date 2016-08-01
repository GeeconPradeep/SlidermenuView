# SlidermenuView
View Controller.h
#import <UIKit/UIKit.h>
@interface ViewController : UIViewController
@end
View Controller.m
#import "ViewController.h"
#import "SelectedViewController.h"

@interface ViewController ()
@property (weak, nonatomic) IBOutlet UIView *sliderview;
@property (weak, nonatomic) IBOutlet UIButton *open;
@property (weak, nonatomic) IBOutlet UIButton *Close;
- (IBAction)First:(id)sender;
- (IBAction)Fifth:(id)sender;
- (IBAction)Second:(id)sender;
- (IBAction)Third:(id)sender;
- (IBAction)fourth:(id)sender;
- (IBAction)close1:(id)sender;
- (IBAction)open1:(id)sender;

@end

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
    _sliderview.hidden=YES;
    _Close.hidden=YES;
}

- (void)didReceiveMemoryWarning {
    [super didReceiveMemoryWarning];
}

- (IBAction)First:(id)sender {
    SelectedViewController *Selected=[self.storyboard instantiateViewControllerWithIdentifier:@"Selected"];
    CATransition *transition = [CATransition animation];
    transition.duration = 0.5;
    transition.timingFunction = [CAMediaTimingFunction functionWithName:kCAMediaTimingFunctionEaseInEaseOut];
    transition.type = kCATransitionPush;
    transition.subtype = kCATransitionFromRight;
    [self.view.window.layer addAnimation:transition forKey:nil];
    [self presentViewController:Selected animated:NO completion:nil];

}

- (IBAction)Fifth:(id)sender {
    SelectedViewController *Selected=[self.storyboard instantiateViewControllerWithIdentifier:@"Selected"];
    CATransition *transition = [CATransition animation];
    transition.duration = 0.5;
    transition.timingFunction = [CAMediaTimingFunction functionWithName:kCAMediaTimingFunctionEaseInEaseOut];
    transition.type = kCATransitionPush;
    transition.subtype = kCATransitionFromRight;
    [self.view.window.layer addAnimation:transition forKey:nil];
    [self presentViewController:Selected animated:NO completion:nil];
}
- (IBAction)Second:(id)sender {
    SelectedViewController *Selected=[self.storyboard instantiateViewControllerWithIdentifier:@"Selected"];
    CATransition *transition = [CATransition animation];
    transition.duration = 0.5;
    transition.timingFunction = [CAMediaTimingFunction functionWithName:kCAMediaTimingFunctionEaseInEaseOut];
    transition.type = kCATransitionPush;
    transition.subtype = kCATransitionFromRight;
    [self.view.window.layer addAnimation:transition forKey:nil];
    [self presentViewController:Selected animated:NO completion:nil];
}
- (IBAction)Third:(id)sender {
    SelectedViewController *Selected=[self.storyboard instantiateViewControllerWithIdentifier:@"Selected"];
    CATransition *transition = [CATransition animation];
    transition.duration = 0.5;
    transition.timingFunction = [CAMediaTimingFunction functionWithName:kCAMediaTimingFunctionEaseInEaseOut];
    transition.type = kCATransitionPush;
    transition.subtype = kCATransitionFromRight;
    [self.view.window.layer addAnimation:transition forKey:nil];
    [self presentViewController:Selected animated:NO completion:nil];
}
- (IBAction)fourth:(id)sender {
    SelectedViewController *Selected=[self.storyboard instantiateViewControllerWithIdentifier:@"Selected"];
    CATransition *transition = [CATransition animation];
    transition.duration = 0.5;
    transition.timingFunction = [CAMediaTimingFunction functionWithName:kCAMediaTimingFunctionEaseInEaseOut];
    transition.type = kCATransitionPush;
    transition.subtype = kCATransitionFromRight;
    [self.view.window.layer addAnimation:transition forKey:nil];
    [self presentViewController:Selected animated:NO completion:nil];
}
- (IBAction)close1:(id)sender {
    _sliderview.hidden=YES;
    _open.hidden=NO;
    _Close.hidden=YES;
    CATransition *transition = [CATransition animation];
    transition.duration = 0.5;
    transition.type = kCATransitionPush;
    transition.subtype = kCATransitionFromRight;
    [transition setTimingFunction:[CAMediaTimingFunction functionWithName:kCAMediaTimingFunctionEaseInEaseOut]];
    [_sliderview.layer addAnimation:transition forKey:nil];
}
- (IBAction)open1:(id)sender {
    _sliderview.hidden=NO;
    _open.hidden=YES;
    _Close.hidden=NO;
    CATransition *transition = [CATransition animation];
    transition.duration = 0.5;
    transition.type = kCATransitionPush;
    transition.subtype = kCATransitionFromLeft;
    [transition setTimingFunction:[CAMediaTimingFunction functionWithName:kCAMediaTimingFunctionEaseInEaseOut]];
    [_sliderview.layer addAnimation:transition forKey:nil];
}
@end
SelectedViewController.h
#import <UIKit/UIKit.h>

@interface SelectedViewController : UIViewController

@end
SelectedViewController.m
#import "SelectedViewController.h"
#import "ViewController.h"

@interface SelectedViewController ()
- (IBAction)Back:(id)sender;

@end

@implementation SelectedViewController

- (void)viewDidLoad {
    [super viewDidLoad];
}

- (void)didReceiveMemoryWarning {
    [super didReceiveMemoryWarning];
}


- (IBAction)Back:(id)sender {
    ViewController *view=[self.storyboard instantiateViewControllerWithIdentifier:@"view"];
    CATransition *transition = [CATransition animation];
    transition.duration = 0.5;
    transition.timingFunction = [CAMediaTimingFunction functionWithName:kCAMediaTimingFunctionEaseInEaseOut];
    transition.type = kCATransitionPush;
    transition.subtype = kCATransitionFromLeft;
    [self.view.window.layer addAnimation:transition forKey:nil];
    [self presentViewController:view animated:NO completion:nil];


}
@end


