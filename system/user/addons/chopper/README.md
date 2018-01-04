# Environmentall:EE Friendly

**Environmentall:EE Friendly** simplifies managing your multi-environment config file. While there are various ways out there to do this, they all require you to manually configure your system **`config.php`** file.

Many of the questions we see are regarding managing multiple environments and how to modify or edit the **`config.php`** file in order to better ease the workflow.

For some developers this is an easy process. Many have their own methods already established.

For others, this is confusing and/or problematic.

Using **Environmentall:EE Friendly** makes this extremely easy. Manage all of your variables from the control panel.

As an added **BONUS**, if you go to your **Menu Manager** via **`Settings->Menu Manager`** and either create your own or edit the **`Default`** menu set, you can add **`Environmentall:EE Friendly`** to your main CP so you always know which environment you are working in.

*One caveat is that if you manually configure or set your variables in the form, they must be correct or you will not be connected.*

(Same as with your config.php file itself)

## Requirements

 - ExpressionEngine 3+ (EE3+)
 - [Windows - WampServer](http://www.wampserver.com/en/ "Download WampServer")
 or
 - [Mac - MAMP or MAMP PRO](https://www.mamp.info/en/ "Download MAMP")

## Installation

Installing **Environmentall:EE Friendly** is easy. Simply load the **`environmentallee_friendly`** folder to your user addons system folder and load the themes folder to the user themes folder on the **`public_html`** location.

## Usage

Once installed, you simply enter the information as you would for your **Development** and **Production** environments for each environment respectively.

### `Development`

Click on **`Development`** in the left sidebar to enter or edit your development environment settings.

You will be able to manage two groups of settings for your environment.

The top section will allow you to specify your **development TLD**, your **development `{base_path}`**, and your **development `{base_url}`**.

To make this easier to manage, we have added a **`Use Current`** button which will grab your default settings you have already set for the current environment you are in.

The bottom section will allow you to manage your database information for your development environment.

Like the top section, we have added a **`Use Current`** button which will grab your default settings you have already set for the current environment you are in.

### `Production`

Click on **`Production`** in the left sidebar to enter or edit your production environment settings.

You will be able to manage two groups of settings for your environment.

The top section will allow you to specify your **production TLD**, your **production `{base_path}`**, and your **production `{base_url}`**.

To make this easier to manage, we have added a **`Use Current`** button which will grab your default settings you have already set for the current environment you are in.

The bottom section will allow you to manage your database information for your production environment.

Like the top section, we have added a **`Use Current`** button which will grab your default settings you have already set for the current environment you are in.

### `Basic`

A standard usage of **Environmentall:EE Friendly** would follow this flow:

1. Build development website in **WAMP/MAMP** normally using the domain **`your-domain.dev`**
2. Install **Environmentall:EE Friendly**
3. Click on **`Development`**
4. Click on **`Use Current`** on both top and bottom sections
5. Click **`Save Settings`**
6. Click on **`Production`**
7. Set your **`TLD`** for the production server/live site
8. Set your **`Path`** for the production website the same as you would your **`Default base path`** in **`Settings->URL and Path Settings`** in the **EE CP**
9. Set your **`URL`** for the production website the same as you would your **`Default base URL`** in **`Settings->URL and Path Settings`** in the **EE CP**
10. Set your database information the same as you would for a typical install using your production **`Database Name`**, **`Username`**, **`Password`**, etc...
11. Click **`Save Settings`**

Once you click **`Save Settings`**, **Environmentall:EE Friendly** adds the variables and logic needed to test against your fields to determine which database and files to load to your main **`config.php`** file for you. No need to edit or manage this file again. For safety reasons, a backup of that file is created in the **`user/config/`** folder so if anything were to happen you can simply delete the new file and rename the backup.

**`Save Settings`** also triggers **Environmentall:EE Friendly** to build a **`development_config.php`** and a **`production_config.php`** file to overwrite the main **`config.php`** file variables depending on where you are.

## Changelog

### 1.0.0

- Released!

### 1.0.1

- Updated an out of place method call.

### 1.0.2

- Updated to allow the usage of sub-domains. Sub-domains were killing the path outputs in the written files.

### 1.0.3

- Updated to allow the usage of proper Docs using the ExpressionEngine preferred format.

## Disclaimer

BBD is not affiliated with WAMP, MAMP, or EllisLab

## License

#### Commercial License Agreement

---

This license is a legal agreement between you and Black Belt Designs (BBD) for the use of BBD Software (the “Software”). By downloading the software, you agree to be bound by the terms and conditions of this license. BBD reserves the right to alter this agreement at any time, for any reason, without notice.

#### Permitted Use

---

A purchased license is required for each installation of the software. One (1) license grants the right to perform one (1) installation of the Software. Each additional installation of the Software requires an additional purchased license.

#### Restrictions

---

Unless you have been granted prior, written consent from BBD, you may not:
• Reproduce, distribute, or transfer the Software, or portions thereof, to any third party.
• Sell, rent, lease, assign, or sublet the software, or portions thereof.
• Grant rights to any other person.
• Use this Software in violation of any US or international law or regulation.

#### Display of Copyright Notices

---

All copyright and proprietary notices and logos in the Control Panel and within the Software must remain intact.

#### Making Copies and Duplication of Software

---

You may make copies of the Software for back-up purposes, provided that you reproduce the Software in its original form and with all proprietary notices on the back-up copy.

#### Software Modification

---

You may alter, modify, or extend the Software for your own use, or commission a third-party to perform modifications for you, but you may not resell, redistribute or transfer the modified or derivative version without prior written consent from BBD. Components from this software may not be extracted and used in other programs without prior written consent from BDB.

#### Technical Support

---

Technical support is available only through devot-ee.com forums. BBD does not provide telephone support. No representations or guarantees are made regarding the response time in which support questions are answered.

#### Refunds

---

Software purchased through devot-ee.com store can be refunded within 30 days of purchase. Please contact devot-ee.com to request a refund.

#### Indemnity

---

You agree to indemnify and hold harmless BBD for any third-party claims, actions or suits, as well as any related expenses, liabilities, damages, settlements or fees arising from your use or misuse of the Software, or a violation of any terms of this license.

#### Disclaimer of Warranty

---

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, WARRANTIES OF QUALITY, PERFORMANCE, NON-INFRINGEMENT, MERCHANTABILITY, OR FITNESS FOR A PARTICULAR PURPOSE. FURTHER, BBD DOES NOT WARRANT THAT THE SOFTWARE OR ANY RELATED SERVICE WILL ALWAYS BE AVAILABLE.

#### Limitations of Liability

---

YOU ASSUME ALL RISK ASSOCIATED WITH THE INSTALLATION AND USE OF THE SOFTWARE. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS OF THE SOFTWARE BE LIABLE FOR CLAIMS, DAMAGES OR OTHER LIABILITY ARISING FROM, OUT OF, OR IN CONNECTION WITH THE SOFTWARE. LICENSE HOLDERS ARE SOLELY RESPONSIBLE FOR DETERMINING THE APPROPRIATENESS OF USE AND ASSUME ALL RISKS ASSOCIATED WITH ITS USE, INCLUDING BUT NOT LIMITED TO THE RISKS OF PROGRAM ERRORS, DAMAGE TO EQUIPMENT, LOSS OF DATA OR SOFTWARE PROGRAMS, OR UNAVAILABILITY OR INTERRUPTION OF OPERATIONS.
