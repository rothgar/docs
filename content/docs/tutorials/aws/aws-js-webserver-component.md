---
title: "AWS Web Server component example"
---

<p class="mb-4 flex">
    <a class="flex flex-wrap items-center rounded text-xs text-white bg-blue-600 border-2 border-blue-600 px-2 mr-2 whitespace-no-wrap hover:text-white" style="height: 32px" href="https://github.com/pulumi/examples/tree/master/aws-js-webserver-component" target="_blank">
        <span><i class="fab fa-github pr-2"></i> View Code</span>
    </a>

    <a href="https://app.pulumi.com/new?template=https://github.com/pulumi/examples/tree/master/aws-js-webserver-component" target="_blank">
        <img src="https://get.pulumi.com/new/button.svg" alt="Deploy">
    </a>
</p>


Deploy an EC2 instance using `@pulumi/aws`, using a common module for creating an instance. A function `createInstance` is defined in [webserver.js](https://github.com/pulumi/examples/blob/master/aws-js-webserver-component/webserver.js) which is then used in main program.

For a walkthrough of the main example, [Infrastructure on AWS](https://www.pulumi.com/docs/reference/tutorials/aws/tutorial-ec2-webserver/).

