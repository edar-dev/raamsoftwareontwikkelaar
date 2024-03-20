---
title: Develop Hugo Project on GitPod
description: " Learn how to configure GitPod to create a cloud developer environment for your first Hugo project."
date: 2024-03-11T20:01:19.794Z
preview: ""
tags: []
categories: []
type: default
---
First things first, let's analyze the main actors:

GitPod is a cloud development environment designed for teams to efficiently and securely develop software. With the free tier, you can get up to 50 hours per month for free, and even if you need more hours, it remains cost-effective (0.36 euro per hour at the time of writing).

Hugo is the world's fastest framework for building websites. With just a few commands, you can create a website, generate new content, and manage draft, future, and published pages.

But how can we integrate these two parts and create a fully working developer environment?
Getting Started

1. **Create a GitPod Account:** Begin by creating an account on GitPod.

1. **Add Your Repository:** Easily add your repository to GitPod by prefixing the GitHub, BitBucket, or GitLab repository URL with gitpod.io/#.

1. **Edit Permissions:** Edit permissions for your chosen provider by navigating to https://gitpod.io/user/integrations. From the desired provider, edit permissions and grant repo and/or public_repo permissions.

1. **Create a Workspace:** Create a new workspace starting from the linked repository.

1. **Enable Prebuild:** Go to https://gitpod.io/repositories/, choose the target repository, and enable prebuild. Follow the prompted steps to enable it.

1. **Configure .gitpod.yml:** Start the workspace and create a new file called .gitpod.yml in the root of your repository. Alternatively, you can run gp init to automatically generate the base configuration. Edit .gitpod.yml with the content provided here. This file instructs GitPod to install Hugo while starting the desired workspace.

1. **Check Prebuild Status:** Stop the workspace and go to the prebuild page at https://gitpod.io/prebuilds. If everything is configured correctly, you should see the result of the newly configured prebuild.

1. **Start Workspace:** Start the workspace again. This time, if you run `hugo version` in the console, you should see the version of the Hugo package that is automatically installed in the workspace.

By following these steps, you'll have successfully set up a GitPod environment for your Hugo project, enabling seamless development and collaboration in the cloud.

Happy coding!