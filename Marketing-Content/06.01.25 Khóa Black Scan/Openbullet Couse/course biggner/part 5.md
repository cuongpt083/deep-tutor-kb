---
title: "Private Proxy & Keyword Configuration"
course: "mang-ads-seo-marketing"
module: "06.01.25 Black Scan/Openbullet"
instructor: "Unknown"
difficulty: "Beginner"
tags:
  - "proxy"
  - "netflix"
summary: "This lesson covers the setup and configuration of private proxies for Netflix and scanning tools, emphasizing the distinction between private and public keywords, and step-by-step workflow using Slayer/Leecher tools to achieve successful config setup."
---

# Private Proxy & Keyword Configuration

## 💡 Tóm Tắt Cốt Lõi (Key Takeaways)
- Netflix and scanning configurations require private proxies and private keywords to function properly; public defaults result in failed configs.
- The Slayer and Slayer Leecher tools rely on correct keyword input; using default settings exposes public keywords which must be deleted and replaced.
- Successful setup involves testing SSL proxies, extracting necessary attributes, and performing config fixes while selecting the appropriate private proxy.

## 📖 Nội Dung Chi Tiết
### 1. Proxy & Keyword Configuration
- **Private Proxy Requirement**: Netflix and similar services strictly require private HQ proxies. Public proxies will not work and will cause config failures.
- **SSL Proxy Testing**: Instructors tested SSL proxy connections to verify attribute extraction; failure to extract attributes indicates incorrect proxy or keyword setup.
- **Keyword Distinction**: A critical part of the configuration is the use of private keywords versus public keywords. The default configuration exposes public keywords, which must be explicitly deleted and replaced with private keywords for the tool to work.
- **Tool Workflow (Slayer/Leecher)**: Using tools like Slayer and Slayer Leecher requires proper keyword configuration. The process involves searching for the config, fixing issues, and opening the appropriate profile/settings to apply the private proxy and keyword.

> **Ví dụ / Case Study**: The instructor demonstrated testing a config in Netflix, noting that without a private proxy and private keyword, the system defaults to public keywords and fails. By switching to a private proxy and replacing the keyword, the config becomes functional. The steps include: selecting private proxy → testing SSL → verifying attributes → deleting default public keyword → inputting private keyword → final config validation.

### 2. Config Fix & Setup Workflow
- **Search & Fix**: Locate the config file, identify issues (e.g., missing attributes, wrong proxy type), and apply fixes.
- **Profile Opening**: Open the relevant profile or setting to apply changes.
- **Final Validation**: Ensure the config works by testing the connection and verifying that private proxy and keyword are correctly loaded.

## ❓ Câu Hỏi & Trả Lời Trọng Tâm (Q&A for Search)
- **Hỏi:** How to fix a Netflix config that isn't working?
  - **Đáp:** Ensure you are using a private HQ proxy and a private keyword. Delete any default public keywords, test the SSL proxy for attribute extraction, and re-configure the Slayer/Leecher tool with the corrected settings.
- **Hỏi:** What is the difference between private and public keywords in scanning tools?
  - **Đáp:** Private keywords are specific, restricted inputs that allow the tool to access protected or premium configurations, while public keywords are default settings that expose the tool to broader, often non-functional or blocked, access. Always replace public keywords with private ones for successful operation.
- **Hỏi:** What are the essential steps to set up Slayer or Slayer Leecher for the first time?
  - **Đáp:** Begin by selecting a private proxy, test the SSL connection to extract required attributes, search and fix the config file, delete default public keywords, input your private keyword, and open the target profile to validate the setup.