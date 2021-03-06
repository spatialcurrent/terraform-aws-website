<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
Creates a static website hosted on S3 and served from CloudFront.

Creates the following resources:

* ACM Certificate
* S3 Bucket
* CloudFront Distribution
* Route53 Records

## Usage

```hcl
module "website" {
  source = "spatialcurrent/website/aws"

  origin_id            = "${var.origin_id}"
}
```

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| acm\_tags |  | map | `{}` | no |
| cloudfront\_404\_response\_code |  | string | `"404"` | no |
| cloudfront\_404\_response\_path |  | string | `""` | no |
| cloudfront\_comment |  | string | n/a | yes |
| cloudfront\_forwarded\_query\_strings |  | string | `"false"` | no |
| cloudfront\_logs\_bucket\_domain\_name |  | string | n/a | yes |
| cloudfront\_logs\_prefix |  | string | `""` | no |
| cloudfront\_origin\_read\_timeout |  | string | `"5"` | no |
| cloudfront\_origin\_ssl\_protocols |  | list | `[ "SSLv3", "TLSv1", "TLSv1.1", "TLSv1.2" ]` | no |
| cloudfront\_tags |  | map | `{}` | no |
| error\_document |  | string | `""` | no |
| fqdn |  | string | n/a | yes |
| index\_document |  | string | `""` | no |
| origin\_id |  | string | n/a | yes |
| price\_class |  | string | `"PriceClass_100"` | no |
| route53\_zone\_id |  | string | n/a | yes |
| routing\_rules |  | string | `""` | no |
| s3\_bucket\_name |  | string | n/a | yes |
| s3\_cors |  | list | `[]` | no |
| s3\_cors\_allowed\_headers |  | list | `[]` | no |
| s3\_cors\_allowed\_methods |  | list | `[]` | no |
| s3\_cors\_allowed\_origins |  | list | `[]` | no |
| s3\_logs\_bucket\_id |  | string | n/a | yes |
| s3\_logs\_prefix |  | string | `"logs/s3"` | no |
| s3\_tags |  | map | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| domain\_name |  |
| hosted\_zone\_id |  |
| s3\_bucket\_arn |  |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
