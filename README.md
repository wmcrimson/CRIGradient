#CrimsonKit

This source is licensed under the terms of the Attribution License.  Copyright &copy; 2010-2011, Waqar Malik.

    CKGradient *gradient = [[CKGradient alloc] initWithStartingColor:[UIColor colorWithRGBAHex:0x0000ffff] endingColor:[UIColor yellowColor]];
    [gradient drawInRect:rect angle:45.0f];
    [gradient release];

    UIBezierPath *path = [UIBezierPath bezierPathWithRoundedRect:CGRectInset(rect, 10, 20) cornerRadius:30];
    gradient = [[CKGradient alloc] initWithStartingColor:[UIColor colorWithRGBAHex:0x00ff00ff] endingColor:[UIColor redColor]];
    [gradient drawInBezierPath:path angle:0];
    [gradient release];

    path = [UIBezierPath bezierPathWithOvalInRect:CGRectInset(rect, 30, 80)];
    gradient = [[CKGradient alloc] initWithStartingColor:[UIColor cyanColor] endingColor:[UIColor magentaColor]];
    [gradient drawInBezierPath:path angle:180];
    [gradient release];
    CGRect myRect = CGRectInset(rect, 40, 110);
    path = [UIBezierPath bezierPathWithOvalInRect:myRect];
    [path appendPath:[UIBezierPath bezierPathWithOvalInRect:CGRectInset(myRect, 20, 20)]];
    path.usesEvenOddFillRule = YES;
    [path addClip];
    gradient = [[CKGradient alloc] initWithStartingColor:[UIColor orangeColor] endingColor:[UIColor purpleColor]];
    [gradient drawFromPoint:CGPointMake(CGRectGetMinX(myRect), CGRectGetMinY(myRect)) toPoint:CGPointMake(CGRectGetMinX(myRect), CGRectGetMaxY(myRect)) options:0];
    [gradient release];

<center>
<img src="https://github.com/wmalloc/CKGradient/raw/master/CKGradient.png" />
</center>
