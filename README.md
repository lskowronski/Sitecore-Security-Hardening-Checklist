# Sitecore-Security-Hardening-Checklist
Checklist of things to validate to make Sitecore instances better secured

1. [ ] Do you use the latest version of Sitecore?
   - [ ] Do you have installed all available service packs to your Sitecore?
2. [ ] Do servers which you use have got installed all available updates? 
3. [ ] Have you deleted default admin user and created at least one new account with secure password?
4. [ ] Have you changed configuration of membership provider to force users to use more secure passwords? Default settings are not secure enough.
5. [ ] Are you sure that your Content Management servers are not visible and accessible for people outside your network/company?
6. [ ] Do you use HTTPS to secure communication with your Content Delivery and Content Management servers?
7. [ ] Have you got encrypted connectionStrings section in your config files?
8. [ ] Are you registered on „security notification” maling list? (https://www.sitecore.com/landing/xc/2016/xc-ops-sitecore-security-notifications)
9. [ ] Have you set properly level of access to the App_Config, Sitecore and Admin directories on your servers? (https://doc.sitecore.net/sitecore_experience_platform/setting_up_and_maintaining/security_hardening/configuring/deny_anonymous_users_access_to_a_folder)
10. [ ] Have you changed the hash algorithm for passwords stored in Sitecore from default SHA1 into SHA512?
11. [ ] Are you sure that you disabled (by adding .disabled extension) all administrative tools on Content Delivery servers (and Content Management servers if they are exposed to the internet)?
12. [ ] If you do not use RSS Feeds you should remove from configuration handler responsible for feed generation – have you done that?
13. [ ] If you do not use WebDav (Web Distributed Authoring and Versioning) you should disable that feature – have you done that?
14. [ ] Have you changed permissions of upload directory to be sure that files cannot be executed there? All files in this directory should be readonly.
15. [ ] Do you use Upload Filter tool to filter extensions of files uploaded by content authors? (https://doc.sitecore.net/sitecore_experience_platform/setting_up_and_maintaining/security_hardening/configuring/secure_the_file_upload_functionality#_The_upload_filter)
16. [ ] Are you sure that /data and /indexes directories are stored outside website directory?
17. [ ] Have you set limited access to the xml, xslt and mrt files?
18. [ ] Have you disabled access to SQL Server from XSLT ?
19. [ ] Do you have updated and set properly configuration for Telerik library? (https://doc.sitecore.net/sitecore_experience_platform/setting_up_and_maintaining/security_hardening/configuring/secure_the_telerik_controls)
20. [ ] Have you removed phantomJS directory from Content Delivery server?
    - [ ] Have you disabled getScreenshotForUrl pipeline on Content Delivery server? 
21. [ ] Have you changed Media.RequestProtection.SharedSecret to random string to protect media requests?
22. [ ] Have you removed the X-Aspnet-Version HTTP header from responses sent by you servers?
23. [ ] Have you removed the X-Powered-By HTTP header from responses sent by you servers?
24. [ ] Have you removed the X-AspNetMvc-Version HTTP header from responses sent by you servers?


To change that file into PDF please use following url:
- [GitPrint online service](https://gitprint.com/lskowronski/Sitecore-Security-Hardening-Checklist)

To read more about all the points from the list please check following websites
- [Sitecore Security Hardening](https://doc.sitecore.net/sitecore_experience_platform/setting_up_and_maintaining/security_hardening)

If you would like to add anything to this list - please create pull request or contact me directly. 
If you are not sure how to format text on this page, please follow [basic writing and formating syntax page](https://help.github.com/articles/basic-writing-and-formatting-syntax/)