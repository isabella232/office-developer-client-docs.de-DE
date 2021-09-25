---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- xlfcaller-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c4728136a34cc2b2cd60c6f7ec2e057d366df7c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605596"
---
# <a name="xlfcaller"></a>xlfCaller

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt Informationen über die Zelle, den Zellbereich, den Befehl in einem Menü, ein Tool auf einer Symbolleiste oder ein Objekt zurück, das den aktuell ausgeführten DLL-Befehl oder die dll-Funktion aufgerufen hat.
  
|**Von aufgerufener Code**|**gibt zurück**|
|:-----|:-----|
|DLL  <br/> |Die Register-ID.  <br/> |
|Eine einzelne Zelle  <br/> |Ein Einzelzellenverweis.  <br/> |
|Eine Arrayformel mit mehreren Zellen  <br/> |Ein mehrzeiliger Bezug.  <br/> |
|Ein Ausdruck für bedingte Formatierung  <br/> |Ein Verweis auf die Zelle, auf die die Formatierungsbedingung angewendet wird.  <br/> |
|Ein Menü  <br/> | Ein einzeiliges Array mit vier Elementen:  <br/>  Die Balken-ID.  <br/>  Die Menüposition.  <br/>  Die Untermenüposition.  <br/>  Die Befehlsposition.  <br/> |
|Symbolleiste  <br/> | Ein einzeiliges Array mit zwei Elementen:  <br/>  Die Symbolleistennummer für integrierte Symbolleisten oder der Symbolleistenname für benutzerdefinierte Symbolleisten.  <br/>  Die Position auf der Symbolleiste.  <br/> |
|Ein Grafikobjekt  <br/> |Der Objektbezeichner (Objektname).  <br/> |
|Ein Befehl, der einem xlcOnEnter, ON, zugeordnet ist. EINGABETASTE, Ereignistrapping  <br/> |Ein Verweis auf die eingegebenen Zellen.  <br/> |
|Ein Befehl, der einem XlcOnDoubleclick,ON zugeordnet ist. DOUBLECLICK, Ereignistrapping.  <br/> |Die Zelle, auf die doppelt geklickt wurde (nicht unbedingt die aktive Zelle).  <br/> |
|Auto_Open-, AutoClose-, Auto_Activate- oder Auto_Deactivate-Makro  <br/> |Der Name des aufrufenden Blatts.  <br/> |
|Andere Nicht aufgeführte Methoden  <br/> |#REF! Fehler  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Der Rückgabewert ist einer der folgenden **XLOPER** /  **XLOPER12-Datentypen:** **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr** oder **xltypeMulti**. Da drei dieser Typen auf zugeordneten Speicher verweisen, sollte der Rückgabewert von **xlfCaller** immer in einem Aufruf der [xlFree-Funktion](xlfree.md) freigegeben werden, wenn er nicht mehr benötigt wird. 
  
Weitere Informationen zu **XLOPERs** /  **XLOPER12s** finden Sie [unter Speicherverwaltung in Excel](memory-management-in-excel.md).
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion ist die einzige Nicht-Arbeitsblattfunktion, die von einer DLL/XLL-Arbeitsblattfunktion aufgerufen werden kann. Andere XLM-Informationsfunktionen können nur über Befehle oder Makrovorlagen-äquivalente Funktionen aufgerufen werden.
  
## <a name="example"></a>Beispiel

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Diese Funktion ruft ein Befehlsmakro (xlcSelect) auf und funktioniert nur dann ordnungsgemäß, wenn es von einem Makroblatt aufgerufen wird.
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

