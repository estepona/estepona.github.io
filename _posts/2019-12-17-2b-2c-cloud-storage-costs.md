---
title: "2B and 2C Cloud Storage Costs"
date: 2019-12-17
categories: code

classes:
  - wide
---

Recently, I've thinking about if it's worth to get rid of the storage disks and embracing the cloud storage, so I did some research on the cost of some popular cloud storage providers, and there seems to be a simple rule behind the pricing schema (that I'm probably too dumb to realize earlier): 2B (to business) is more flexible, while 2C (to consumer) has fixed pricing but simpler.

As of today, Dec 17, 2019, here are what 2C cloud storage cost looks like, the pricing is very simple to understand and calculate based on personal usage:

Google Drive:
![googledrive](/assets/img/2019-12-17-2b-2c-cloud-storage-costs/googledrive.png)

Microsoft OneDrive:
![onedrive](/assets/img/2019-12-17-2b-2c-cloud-storage-costs/onedrive.png)

Dropbox:
![dropbox](/assets/img/2019-12-17-2b-2c-cloud-storage-costs/dropbox.png)

However, 2B is totally different. For example, [AWS S3](https://aws.amazon.com/s3/) provides so many options you can choose to balance the cost and business needs, which makes it hard to do the tradeoff and calculate the cost (probably why there's [Intelligent-Tiering](https://aws.amazon.com/about-aws/whats-new/2018/11/s3-intelligent-tiering/)).

AWS S3:
![s3](/assets/img/2019-12-17-2b-2c-cloud-storage-costs/s3.png)

If we have 100GB of files to store, it'd cost $2.3/month to store on S3 with standard storage class, which is actually more expensive than storing on Google Drive or OneDrive. If we store on S3 with S3 Glacier, it'd cost only $0.4/month, but then the data retrieval would take longer, which is not ideal for personal usage.

Not to mention figuring out all the details of S3 storage classes...
![s3-storageclass](/assets/img/2019-12-17-2b-2c-cloud-storage-costs/s3-storageclass.png)

I decide to stick to my good old HDDs for the while.
