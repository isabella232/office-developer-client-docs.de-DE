---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- xlfregisterid-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420059"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann von einer DLL aufgerufen werden, die selbst von der Microsoft Excel. Wenn eine Funktion bereits registriert ist, gibt sie die vorhandene Register-ID für diese Funktion zurück, ohne sie erneut zu registrieren. Wenn eine Funktion noch nicht registriert ist, registriert sie sie und gibt die resultierende Register-ID zurück.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Parameter

_pxModuleText_ (**xltypeStr**)
  
Der Name der DLL, die die Funktion enthält.
  
_pxProcedure_ (**xltypeStr** oder **xltypeNum**)
  
Wenn eine Zeichenfolge, der Name der zu aufrufende Funktion. Wenn eine Zahl, die Ordnungsexportnummer der zu aufrufende Funktion. Verwenden Sie aus Gründen der Übersichtlichkeit und Robustheit immer das Zeichenfolgenformular.
  
_pxTypeText_ (**xltypeStr**)
  
Eine optionale Zeichenfolge, die die Typen aller Argumente für die Funktion und den Typ des Rückgabewerts der Funktion an gibt. Weitere Informationen finden Sie im Abschnitt "Hinweise". Dieses Argument kann für eine eigenständige DLL (XLL), die xlAutoRegister definiert, **ausgelassen werden.**
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt die Register-ID der Funktion (**xltypeNum**) zurück, die bei nachfolgenden Aufrufen von **xlfUnregister verwendet werden kann.**
  
## <a name="remarks"></a>Hinweise

Diese Funktion ist nützlich, wenn Sie sich keine Gedanken über die Verwaltung einer Register-ID machen möchten, sie jedoch später zum Aufheben der Registrierung benötigen. Es ist auch hilfreich, Menüs, Tools und Schaltflächen zuzuordnen, wenn sich die funktion, die Sie zuweisen möchten, in einer DLL befindet.
  
Wenn eine DLL- oder XLL-Funktion mit einem gültigen _pxFunctionText-Argument_ registriert wurde, das **xlfRegister** bereitgestellt wurde, kann die Register-ID auch durch Übergeben des _pxFunctionText_ an die Funktion **xlfEvaluate erhalten werden.**
  
## <a name="see-also"></a>Siehe auch

- [REGISTRIEREN](xlfregister-form-1.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

