# running .heic files onn windows
- When I installed a new windows, I found that all of my images with .heic extension is not working
I started to find a solution
and After some time, I found a tutorial asking to install Hevc extension and I did and Images worked
- On a new windows installation, I did the same steps and it didn't work
- I did all the steps and I installed all the attached extensions and no hope
- I installed a Heic viewer, It works but not showing images thumbnails preview
- so I had to uninstall those extensions again and uninstalled windows photos application also using the following commands
  Use one of the following commads and remove the extensions below
  ```
  Remove-AppxPackage -Package
  Remove-AppxProvisionedPackage -Online -PackageName
  ```

  ```
  Microsoft.HEIFImageExtension_1.1.861.0_x64__8wekyb3d8bbwe
  Microsoft.HEVCVideoExtensions_2.1.2192.0_x64__8wekyb3d8bbwe
  Microsoft.AV1VideoExtension_1.2.2331.0_x64__8wekyb3d8bbwe
  45907smallapp.HEICViewer_1.0.3.0_x64__z9hw59krvrfng
  ```

  and I got this packages list by typing the follwoing list, as versions will vary
  ```
  Get-AppxPackage -AllUsers | Format-List -Property PackageFullName,PackageUserInformation
  ```

-  remove the ones that you already installed with your versions
-  after, reinstall windows photos application again
-  and thentry to run the .heic, It will work and ask to install another extension from the windows store, do this and it will work successfully

  
