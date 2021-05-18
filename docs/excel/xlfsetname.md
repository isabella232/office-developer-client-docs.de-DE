---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- xlfsetname-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404260"
---
# <a name="xlfsetname"></a>xlfSetName

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um der DLL zugeordnete definierte Namen zu erstellen und zu löschen.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Parameter

_pxNameText_ (**xltypeStr**)
  
Der Name des Bereichs, der den üblichen Einschränkungen in der Microsoft Excel gültigen Namen entsprechen sollte.
  
_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef** oder **xltypeInt**)
  
(Optional). Der Wert, der Wertesatz, die Zelle oder der Zellbereich, als  _die pxNameText_ definiert ist. Wenn sie nicht angegeben wird, wird der Name gelöscht. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

_pxRes_ (**xltypeBool** oder **xltypeErr**)
  
TRUE, wenn der Vorgang erfolgreich war, oder FALSE, wenn der Name nicht erstellt oder gelöscht werden konnte. Gibt #VALUE! wenn mindestens eines der Argumente ungültig war.
  
## <a name="remarks"></a>Hinweise

Wenn eine Funktion oder ein Befehl mithilfe von **xlfRegister** mit einem gültigen _pxFunctionText-Argument_ registriert wird, erstellt Excel einen Namen, der der DLL-Ressource zugeordnet ist. Wenn Ihre DLL entladen wird, sollten diese Namen mit der [xlfSetName-Funktion gelöscht werden.](xlfsetname.md) Aufgrund eines bekannten Problems in Excel fehler dieser Löschvorgang. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Beispiel

Weitere Informationen finden Sie im Code für die **xlAutoClose-Funktion** in  `\SAMPLES\GENERIC\GENERIC.C` .
  
## <a name="see-also"></a>Siehe auch

- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

