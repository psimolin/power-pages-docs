---
title: Force Bing webmaster to index your site (preview)
description: Learn how to trigger Microsoft Bing to index the content of your Power Pages site immediately after you add a chatbot.
ms.topic: how-to
ms.date: 09/08/2023
author: nageshbhat-msft
ms.author: nabha
ms.reviewer: kkendrick
contributors:
  - nickdoelman
  - ProfessorKendrick
  - nageshbhat-msft
ms.custom: bap-template
---

# Force Bing webmaster to index your site

The Power Pages chatbot is powered by Microsoft Bing. When you [add a chatbot to your Power Pages website](./enable-chatbot.md), the URL is shared with Bing to index the content. Bing may not start indexing your site right away, however. It can take from several hours to a day. If you don't want to wait for Bing to get around to your site, you can use Bing Webmaster Tools to force it to index your site's content immediately.

> [!IMPORTANT]
>
> - [Understand the capabilities and limitations of AI-powered Copilot features in Power Pages](../transparency-note.md).

## Add your site to your Bing Webmaster Tools account

1. Open [Webmaster Tools](https://www.bing.com/webmasters).
1. [Create a Bing Webmaster Tools account](https://www.bing.com/webmasters/help/getting-started-checklist-66a806de) if you don't have one yet.
1. [Add to your site to your account](https://www.bing.com/webmasters/help/add-and-verify-site-12184f8b).

    - If your site is already verified on Google Search Console, you can import it to Bing Webmaster Tools.
    - If your site isn't verified on Google Search Console, you can add your site manually.

## Verify your ownership

Next, verify that you're the owner of the site. Use either of the following methods, which are also described in [the Bing Webmaster Tools help](https://www.bing.com/webmasters/help/add-and-verify-site-12184f8b).

### XML file authentication

With this method, you upload an XML file to your site's root folder. In Power Pages, it's as simple as adding the file to a note on the site's home page.

1. On the **Add & verify site** page in [Webmaster Tools](https://www.bing.com/webmasters), select **XML File**.
1. Select **BingSiteAuth.xml** to download the file to your local drive.

    :::image type="content" source="media/force-bing-index/xml-verification.png" alt-text="Screenshot of the XML File option in Bing Webmaster Tools.":::

1. In the Power Pages design studio, select **More items** (**&vellip;**) > **Portal Management**.
1. In the sitemap under **Content**, select **Web Files**.
1. Select **+ New**.
1. In **Name**, enter: *BingSiteAuth.xml*
1. In **Website**, search for and select your site.
1. In **Parent Page**, search for and select your site's home page.
1. In **Partial Url**, enter: *BingSiteAuth.xml*
1. In **Publishing State**, search for and select **Published**.
1. Select **Save**.
1. Select the **Notes** tab.
1. Upload the `BingSiteAuth.xml` file.
1. Select **Save & Close**.

### Meta tag authentication

With this method, you add a metadata tag to your site's header HTML. In Power Pages, it's as simple as adding a content snippet.

1. On the **Add & verify site** page in [Webmaster Tools](https://www.bing.com/webmasters), select **HTML Meta Tag**.
1. Select **Copy**.

    :::image type="content" source="media/force-bing-index/meta-content.png" alt-text="Screenshot of the HTML Meta Tag option in Bing Webmaster Tools.":::

1. In the Power Pages design studio, select **More items** (**&vellip;**) > **Portal Management**.
1. In the sitemap under **Content**, select **Content Snippets**.
1. Select **+ New**.
1. In **Name**, enter: *Head/Bottom*
1. In **Website**, search for and select your site.
1. In **Display Name**, enter: *Head/Bottom*
1. Leave **Type** set to **Text**.
1. In **Content Snippet Language**, search for and select **English**.
1. In the **Value** box, paste the metadata you copied in step 2.
1. Select **Save & Close**.

## Add a Robots.txt file

Add a file to your site to tell Bing, Google, and other search engines, or *robots*, how much of its content to index. The Robots.txt file in this example allows search engines to index the entire site, but you can control what pages they're allowed to index. Use Bing Webmaster Tools to easily [edit and test your Robots.txt file](https://blogs.bing.com/webmaster/september-2020/Bing-Webmaster-Tools-makes-it-easy-to-edit-and-verify-your-robots-txt).

1. On your local drive, create a text file and name it **Robots.txt**.
1. Enter the following content in the file:

    ```txt
    User-agent: *
    Disallow:
    ```

1. Save and close the file.
1. In the Power Pages design studio, select **More items** (**&vellip;**) > **Portal Management**.
1. In the sitemap under **Content**, select **Web Files**.
1. Select **+ New**.
1. In **Name**, enter: *Robots.txt*
1. In **Website**, search for and select your site.
1. In **Parent Page**, search for and select your site's home page.
1. In **Partial Url**, enter: *Robots.txt*
1. In **Publishing State**, search for and select **Published**.
1. Select **Save**.
1. Select the **Notes** tab.
1. Upload the `Robots.txt` file.
1. Select **Save & Close**.

## Add a meta description to pages to index

The *meta description* tells search engines what text to display along with the page title. It's an important part of making your site easy to find, so you should put some thought into the description of each page you plan to index. Enter the key phrase "meta description" in your favorite search engine to find guidance for creating effective meta descriptions.

1. In the Power Pages design studio, select **More items** (**&vellip;**) > **Portal Management**.
1. In the sitemap under **Content**, select **Web Pages**.
1. Open a page that you want to force Bing to index.
1. Enter or update the **Description** on both the **Information** form and the **Content Page** form.

    :::image type="content" source="media/force-bing-index/meta-description-example.png" alt-text="Screenshot of a web page's Information form, with the Description highlighted.":::

1. Select **Save & Close**.
1. Repeat for all pages to be indexed.

## Run an SEO scan and fix issues

It's a good idea to scan for common issues with search engine optimization (SEO) that make your site harder to find.

1. Open [Webmaster Tools Site Scan](https://www.bing.com/webmasters/sitescan).
1. Select **Start new scan**.
1. [Follow the instructions](https://www.bing.com/webmasters/help/site-scan-623520c9) to analyze your site and view the report.
1. Fix as many of the issues the scan discovered as you reasonably can.

## Submit URLs

As the final step, index individual page URLs directly. It's a good idea to submit the URLs of any important new pages or pages with new content to get them indexed faster. You can submit up to 100 URLs per day.

1. Open [Webmaster Tools URL Submission](https://www.bing.com/webmasters/submiturl).
1. Select **Submit URLs**.
1. Enter the URLs to index, one per line.
1. Select **Submit**.

To verify the indexing status, select **URL Inspection** in the left side panel. Enter a URL, and then select **Inspect**.

Indexing should complete within a few minutes, but it may take up to an hour to see the results.

### See also

- [Create an AI-generated webpage using Copilot (preview)](../getting-started/create-page-copilot.md)
- [Create a form in a webpage using a Copilot (preview)](../getting-started/add-form-copilot.md)
- [Use Copilot to generate text and it to a webpage (preview)](../getting-started/add-text-copilot.md)
- [Enable chatbot in Power Pages site (preview)](../getting-started/enable-chatbot.md)
- [Add AI-generated code using Copilot (preview)](../configure/add-code-copilot.md)
