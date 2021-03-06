# Distance-IoU Loss: Faster and Better Learning for Bounding Box Regression
<p>Tensorflow implementation for Distance-IoU Loss from the <a href="https://arxiv.org/pdf/1911.08287.pdf">Paper</a></p>
<p>The function return the ciou of two lists of bounding boxes, so when using apply tf.reduce_mean(), or whatever way to optimize over the ciou returned.</p>
<p>on using the ciou or diou loss, I found that -log(IoU) is more stable and converge faster than (1-IoU), so in that case ciou will become -log(IoU) + u + alpha*ar , also I would suggest using ciou along with bounding box regression using Huber loss.</p>
<p><img src="https://github.com/iamnotahumanbecauseiamabot/Distance-IoU-Loss-Faster-and-Better-Learning-for-Bounding-Box-Regression/blob/master/images/ciou2.png" width="225" />
<p><img src="https://github.com/iamnotahumanbecauseiamabot/Distance-IoU-Loss-Faster-and-Better-Learning-for-Bounding-Box-Regression/blob/master/images/ciou1.png" width="225" />
<p><img src="https://github.com/iamnotahumanbecauseiamabot/Distance-IoU-Loss-Faster-and-Better-Learning-for-Bounding-Box-Regression/blob/master/images/ciou0.png" width="225" />

