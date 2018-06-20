---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- XlfSetName-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790595"
---
# <a name="xlfsetname"></a>xlfSetName

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Verwendet zum Erstellen und Löschen von definierten Namen der DLL zugeordnet.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Parameter

_pxNameText_ (**XltypeStr**)
  
Der Name des Bereichs, die der üblichen eingeschränkten in Microsoft Excel gültigen Namen entsprechen soll.
  
_pxNameDefinition_ (**XltypeStr**, **XltypeNum**, **XltypeBool**, **XltypeErr**, **XltypeMulti**, **XltypeSRef**, **XltypeRef**oder **vom Typ XltypeInt**)
  
(Optional). Der Wert, den Satz von Werten, Zelle oder einen Zellbereich ist als dieser _PxNameText_ definiert. Wenn Length angegeben, wird der Name gelöscht. 
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

_pxRes_ (**XltypeBool** oder **XltypeErr**)
  
True, wenn der Vorgang erfolgreich war oder FALSE, wenn der Name nicht erstellt oder gelöscht werden konnte. Gibt #VALUE! Wenn eine oder mehrere der Argumente ungültig war.
  
## <a name="remarks"></a>Hinweise

Wenn eine Funktion oder einen Befehl mit einem gültigen _PxFunctionText_ -Argument **XlfRegister** verwenden registriert ist, erstellt Excel einen Namen der DLL-Ressource zugeordnet sind. Die DLL entladen wird, sollten diese Namen mit der [Funktion XlfSetName](xlfsetname.md)gelöscht werden. Jedoch aufgrund ein bekanntes Problem in Excel schlägt dieser Löschvorgang. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Beispiel

Finden Sie im Code die Funktion **XlAutoClose** in `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Siehe auch

- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

