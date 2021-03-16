# Cloud Computing AS2
UNIs: Lukas Geiger (lg2960) and Maxwell Amsterdam (ma3705)

We used this [AWS project](https://aws.amazon.com/blogs/compute/uploading-to-amazon-s3-directly-from-a-web-or-mobile-application/) to deploy our upload API and frontend. Specifically it created the uploadphotoAS2 HTTP API which calls a lambda function to return the presigned url for the frontend to use. We modified the frontend to display the image uploaded. The assignment did not specify whether or not we should be able to upload multiple images as once so the user is only allowed to upload one JPG image under 10 MB. 

To build our audio search frontend we used template code from [this](https://github.com/amazon-archives/amazon-transcribe-websocket-static) Github project. You must enter your own AWS Access ID and Secret Key to launch a transcribe job. It returns the words you spoke through the microphone. In order to access the microphone we had to host our S3 frontend on Cloudfront and provide an SSL certificate so Chrome would allow us access to the microphone. We then modified it to search using our SDK and lambda function to dispay images. 

Website URL: https://d2xpm8ndx987ff.cloudfront.net/index.html