---
title: "Preparing Extensions for Windows Installer Deployment"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "vsix msi"
ms.assetid: 5ee2d1ba-478a-4cb7-898f-c3b4b2ee834e
caps.latest.revision: 15
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Preparing Extensions for Windows Installer Deployment
You cannot use a Windows Installer package (MSI) to deploy a VSIX package. However, you can extract the contents of a VSIX package for MSI deployment. This document shows how to prepare a project whose default output is a VSIX package for inclusion in a Setup project.  
  
## Preparing an Extension Project for Windows Installer Deployment  
 Perform these steps on new extension projects before adding to a Setup project.  
  
#### To prepare an extension project for Windows Installer deployment  
  
1.  Create a VSPackage, MEF component, Editor Adornment, or other extensibility project type that includes a VSIX manifest.  
  
2.  Open the VSIX manifest in the code editor.  
  
3.  Set the InstalledByMsi element of the VSIX manifest to `true`. For more information about the VSIX manifest, see [VSIX Extension Schema 2.0 Reference](../extensibility/vsix-extension-schema-2.0-reference.md).  
  
     This prevents the VSIX installer from attempting to install the component.  
  
4.  Right-click the project in **Solution Explorer** and click **Properties**.  
  
5.  Select the **VSIX** tab.  
  
6.  Check the box labeled **Copy VSIX content to the following location** and type the path to where the Setup project will pick up the files.  
  
## Extracting Files from an Existing VSIX Package  
 Perform these steps to add the content of an existing VSIX package to a Setup project when you do not have the source files.  
  
#### To extract files from an existing VSIX package  
  
1.  Rename the .VSIX file containing the extension from *filename*.vsix to *filename*.zip.  
  
2.  Copy the contents of the .zip file into a directory.  
  
3.  Delete the [Content_types].xml file from the directory.  
  
4.  Edit the VSIX manifest, as shown in the previous procedure.  
  
5.  Add the remaining files to your Setup project.  
  
## See Also  
 [Visual Studio Installer Deployment](assetId:///121be21b-b916-43e2-8f10-8b080516d2a0)   
 [Walkthrough: Creating a Custom Action](assetId:///4bd4b63a-2b91-431e-839c-5752443f0eaf)