---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- xlfregisterid-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303878"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann von einer DLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde. Wenn eine Funktion bereits registriert ist, wird die vorhandene Register-ID für diese Funktion zurückgegeben, ohne Sie erneut zu registrieren. Wenn eine Funktion noch nicht registriert ist, registriert Sie Sie und gibt die resultierende Register-ID zurück.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Parameter

_pxModuleText_ (**xltypeStr**)
  
Der Name der DLL, die die Funktion enthält.
  
_pxProcedure_ (**xltypeStr** oder **xltypeNum**)
  
Wenn eine Zeichenfolge, der Name der Funktion, die aufgerufen werden soll. Wenn eine Zahl, die ordinale Export Nummer der Funktion, die aufgerufen werden soll. Aus Gründen der Klarheit und Robustheit sollte immer die Zeichenfolgeform verwendet werden.
  
_pxTypeText_ (**xltypeStr**)
  
Eine optionale Zeichenfolge, die die Typen aller Argumente für die Funktion und den Typ des Rückgabewerts der Funktion angibt. Weitere Informationen finden Sie im Abschnitt "Hinweise". Dieses Argument kann für eine eigenständige DLL (XLL), die **xlAutoRegister**definiert, ausgelassen werden.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt die Register-ID der Funktion (**xltypeNum**) zurück, die in nachfolgenden Aufrufen von **xlfUnregister**verwendet werden kann.
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nützlich, wenn Sie sich nicht um die Verwaltung einer Register-ID kümmern möchten, aber Sie müssen Sie später für die Registrierung aufheben. Es eignet sich auch für die Zuweisung zu Menüs, Tools und Schaltflächen, wenn die Funktion, die Sie zuweisen möchten, sich in einer DLL befindet.
  
Wenn eine DLL-oder XLL-Funktion mit einem gültigen _pxFunctionText_ -Argument registriert wurde, das an **xlfRegister**übermittelt wurde, kann die Register-ID auch abgerufen werden, indem die _pxFunctionText_ an die Funktion **xlfEvaluate**übergeben wird.
  
## <a name="see-also"></a>Siehe auch

- [Registrieren](xlfregister-form-1.md)
- [Registrierung](xlfunregister-form-1.md)
- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

