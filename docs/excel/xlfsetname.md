---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- xlfSetName-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310276"
---
# <a name="xlfsetname"></a>xlfSetName

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird zum Erstellen und löschen definierter Namen verwendet, die der DLL zugeordnet sind.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Parameter

_pxNameText_ (**xltypeStr**)
  
Der Name des Bereichen, der den üblichen Einschränkungen in Microsoft Excel für gültige Namen entsprechen sollte.
  
_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **externen xltypeRef**oder **xltypeInt**)
  
(Optional). Der Wert, der Satz von Werten, die Zelle oder der Zellbereich, in dem _pxNameText_ definiert ist. Wenn dieser Wert nicht angegeben wird, wird der Name gelöscht. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

_pxRes_ (**xltypeBool** oder **xltypeErr**)
  
TRUE, wenn der Vorgang erfolgreich war, oder FALSE, wenn der Name nicht erstellt oder gelöscht werden konnte. Gibt #VALUE zurück. , wenn eines oder mehrere der Argumente ungültig waren.
  
## <a name="remarks"></a>Bemerkungen

Wenn eine Funktion oder ein Befehl mithilfe von **xlfRegister** mit einem gültigen _pxFunctionText_ -Argument registriert wird, erstellt Excel einen Namen, der der dll-Ressource zugeordnet ist. Wenn Ihre DLL entladen wird, sollten solche Namen mit der [xlfSetName-Funktion](xlfsetname.md)gelöscht werden. Aufgrund eines bekannten Problems in Excel schlägt dieser Löschvorgang jedoch fehl. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Beispiel

Weitere Informationen finden Sie im **** Code für die `\SAMPLES\GENERIC\GENERIC.C`xlAutoClose-Funktion in.
  
## <a name="see-also"></a>Siehe auch

- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

