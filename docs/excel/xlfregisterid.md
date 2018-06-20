---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- Xlfregisterid-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790609"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann aus einer DLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde. Wenn bereits eine Funktion registriert ist, wird die vorhandene Register-ID für diese Funktion ohne neu registrieren sie zurückgegeben. Wenn eine Funktion noch nicht registriert ist, registriert und gibt die resultierende Register-ID.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Parameter

_pxModuleText_ (**XltypeStr**)
  
Der Name der DLL, die mit der Funktion.
  
_pxProcedure_ (**XltypeStr** oder **XltypeNum**)
  
Wenn eine Zeichenfolge und den Namen der Funktion aufrufen. Wenn eine Zahl, die Ordinal-Eigenschaft Anzahl der aufzurufenden Funktion exportieren. Verwenden Sie für die Klarheit und Stabilität immer in Form einer Zeichenfolge.
  
_pxTypeText_ (**XltypeStr**)
  
Ein optionaler String gibt die Typen der alle Argumente an die Funktion und den Typ des Rückgabewerts der Funktion. Weitere Informationen finden Sie im Abschnitt "Hinweise". Dieses Argument kann für eine eigenständige DLL (XLL) definieren **XlAutoRegister**ausgelassen werden.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Gibt die Register-ID der Funktion (**XltypeNum**), die bei nachfolgenden Aufrufen von **XlfUnregister**verwendet werden kann.
  
## <a name="remarks"></a>Hinweise

Diese Funktion ist nützlich, wenn Sie keine Gedanken Wartung eine Register-ID möchten, jedoch Sie eine später zum Aufheben der Registrierung benötigen. Es ist außerdem hilfreich für das Zuweisen von Menüs, Tools und Schaltflächen in einer DLL wird die Funktion, die Sie zuweisen möchten.
  
In denen eine DLL oder XLL-Funktion mit einem gültigen _PxFunctionText_ -Argument angegeben, um **XlfRegister**registriert wurde, kann auch seine Register-ID abgerufen werden, indem Sie die _PxFunctionText_ an die Funktion **XlfEvaluate**übergeben.
  
## <a name="see-also"></a>Siehe auch

- [REGISTRIEREN](xlfregister-form-1.md)
- [AUFHEBEN DER REGISTRIERUNG](xlfunregister-form-1.md)
- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

