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
ms.localizationpriority: medium
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9c5dc692b641d6ed50ad8464d397657a0f1e3ee8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596785"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann von einer DLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde. Wenn eine Funktion bereits registriert ist, gibt sie die vorhandene Register-ID für diese Funktion zurück, ohne sie erneut zu registrieren. Wenn eine Funktion noch nicht registriert ist, wird sie registriert und die resultierende Register-ID zurückgegeben.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Parameter

_pxModuleText_ (**xltypeStr**)
  
Der Name der DLL, die die Funktion enthält.
  
_pxProcedure_ (**xltypeStr** oder **xltypeNum**)
  
Wenn es sich um eine Zeichenfolge handelt, der Name der aufzurufenden Funktion. Wenn es sich um eine Zahl handelt, die Ordnungsexportnummer der aufzurufenden Funktion. Verwenden Sie aus Gründen der Übersichtlichkeit und Robustheit immer das Zeichenfolgenformular.
  
_pxTypeText_ (**xltypeStr**)
  
Eine optionale Zeichenfolge, die die Typen aller Argumente für die Funktion und den Typ des Rückgabewerts der Funktion angibt. Weitere Informationen finden Sie im Abschnitt "Hinweise". Dieses Argument kann für eine eigenständige DLL (XLL) ausgelassen werden, die **xlAutoRegister** definiert.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt die Register-ID der Funktion (**xltypeNum**) zurück, die in nachfolgenden Aufrufen von **xlfUnregister** verwendet werden kann.
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion ist nützlich, wenn Sie sich keine Gedanken über die Verwaltung einer Register-ID machen möchten, sie aber später für die Aufhebung der Registrierung benötigt wird. Es ist auch nützlich, Menüs, Tools und Schaltflächen zuzuweisen, wenn sich die funktion, die Sie zuweisen möchten, in einer DLL befindet.
  
Wenn eine DLL- oder XLL-Funktion mit einem gültigen  _pxFunctionText-Argument_ registriert wurde, das **xlfRegister** bereitgestellt wurde, kann die Register-ID auch abgerufen werden, indem der  _pxFunctionText_ an die Funktion **xlfEvaluate** übergeben wird.
  
## <a name="see-also"></a>Siehe auch

- [REGISTRIEREN](xlfregister-form-1.md)
- [REGISTRIERUNG](xlfunregister-form-1.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

