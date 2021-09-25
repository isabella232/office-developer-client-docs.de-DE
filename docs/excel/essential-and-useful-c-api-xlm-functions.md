---
title: Wichtige und nützliche XLM-Funktionen der C-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api xlm
ms.localizationpriority: medium
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6aff86a29f22331e4e40e878a7c5e2541e5b3b34
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592998"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a>Wichtige und nützliche XLM-Funktionen der C-API

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Die in diesem Abschnitt beschriebenen Funktionen sind Microsoft Excel Rückruffunktionen, die besonders nützlich für DLL- und XLL-Entwickler sind. Die **xlfRegister-Funktion** ist von entscheidender Bedeutung für XLLs und DLLs, die ihre Funktionen und Befehle registrieren möchten, damit sie direkt von Excel aufgerufen werden können. Die Funktionen **xlfUnregister** und **xlfSetName** werden in Kombination verwendet, um die Registrierung von DLL- und XLL-Funktionen und -Befehlen aufzuheben. 
  
Viele weitere Funktionen werden durch Excel über die C-API verfügbar gemacht, die nützlich sind, wenn Sie XLLs entwickeln. Sie entsprechen den Excel Arbeitsblattfunktionen und -funktionen und -befehle, die in XLM-Makrovorlagen verfügbar sind.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[xlfCaller](xlfcaller.md)
  
[xlfEvaluate](xlfevaluate.md)
  
[xlfGetDef](xlfgetdef.md)
  
[xlfGetName](xlfgetname.md)
  
[xlfRegister (Formular 1)](xlfregister-form-1.md)
  
[xlfRegister (Formular 2)](xlfregister-form-2.md)
  
[xlfRegisterId](xlfregisterid.md)
  
[xlfUnregister (Formular 1)](xlfunregister-form-1.md)
  
[xlfUnregister (Formular 2)](xlfunregister-form-2.md)
  
[xlfSetName](xlfsetname.md)
  

