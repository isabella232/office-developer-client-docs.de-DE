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
ms.localizationpriority: medium
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9ef5f6f557f177e01346beb3ffd7c7bdb00e94d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631440"
---
# <a name="xlfsetname"></a>xlfSetName

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um definierte Namen zu erstellen und zu löschen, die der DLL zugeordnet sind.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Parameter

_pxNameText_ (**xltypeStr**)
  
Der Name des Bereichs, der den üblichen Einschränkungen in Microsoft Excel für gültige Namen entsprechen sollte.
  
_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef** oder **xltypeInt**)
  
(Optional). Der Wert, der Wertesatz, die Zelle oder der Zellbereich, als den  _pxNameText_ definiert ist. Wenn sie nicht angegeben wird, wird der Name gelöscht. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

_pxRes_ (**xltypeBool** oder **xltypeErr**)
  
TRUE, wenn der Vorgang erfolgreich war, oder FALSE, wenn der Name nicht erstellt oder gelöscht werden konnte. Gibt #VALUE zurück! wenn mindestens eines der Argumente ungültig war.
  
## <a name="remarks"></a>Bemerkungen

Wenn eine Funktion oder ein Befehl mit **xlfRegister** mit einem gültigen _pxFunctionText-Argument_ registriert wird, erstellt Excel einen Namen, der der DLL-Ressource zugeordnet ist. Wenn die DLL entladen wird, sollten solche Namen mithilfe der [xlfSetName-Funktion](xlfsetname.md)gelöscht werden. Aufgrund eines bekannten Problems in Excel schlägt dieser Löschvorgang jedoch fehl. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Beispiel

Weitere Informationen finden Sie im Code für die **XlAutoClose-Funktion** in  `\SAMPLES\GENERIC\GENERIC.C` .
  
## <a name="see-also"></a>Siehe auch

- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

