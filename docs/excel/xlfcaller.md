---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- xlfCaller-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405730"
---
# <a name="xlfcaller"></a>xlfCaller

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt Informationen zu der Zelle, dem Zellbereich, dem Befehl in einem Menü, dem Tool auf einer Symbolleiste oder einem Objekt zurück, das den DLL-Befehl oder die aktuell laufende Funktion aufgerufen hat.
  
|**Code aufgerufen von**|**gibt zurück**|
|:-----|:-----|
|DLL  <br/> |Die Register-ID.  <br/> |
|Eine einzelne Zelle  <br/> |Ein Einzelzellen Verweis.  <br/> |
|Eine Arrayformel mit mehreren Zellen  <br/> |Ein mehr zellenverweis.  <br/> |
|Ein Ausdruck für bedingte Formatierung  <br/> |Ein Verweis auf die Zelle, auf die die Formatierungsbedingung angewendet wird.  <br/> |
|Ein Menü  <br/> | Ein Einreihiges Array mit vier Elementen:  <br/>  Die ID des Barcodes.  <br/>  Die Menü Position.  <br/>  Die unter Menü Position.  <br/>  Die Befehlsposition.  <br/> |
|Eine Symbolleiste  <br/> | Ein Array mit zwei Elementen mit einer einzelnen Zeile:  <br/>  Die Symbolleisten Nummer für integrierte Symbolleisten oder den Namen der Symbolleiste für benutzerdefinierte Symbolleisten.  <br/>  Die Position auf der Symbolleiste.  <br/> |
|Ein Grafikobjekt  <br/> |Der Objektbezeichner (Objektname).  <br/> |
|Ein Befehl, der mit einem xlcOnEnter verknüpft ist, ON. ENTER, Ereignistrap  <br/> |Ein Verweis auf die Zelle oder die Zellen, die eingegeben werden.  <br/> |
|Ein Befehl, der mit einem xlcOnDoubleclick verknüpft ist, ON. DOUBLECLICK, Ereignistrap.  <br/> |Die Zelle, auf die doppelgeklickt wurde (nicht unbedingt die aktive Zelle).  <br/> |
|Auto_Open-, autoSchließ-, Auto_Activate-oder Auto_Deactivate-Makro  <br/> |Der Name des aufrufenden Blatts.  <br/> |
|Andere Methoden nicht aufgeführt  <br/> |#REF! Fehler  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Der Rückgabewert ist einer der folgenden **XLOPER**/ **-XLOPER12** -Datentypen: **externen xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**oder **xltypeMulti**. Da drei dieser Typen auf den zugewiesenen Arbeitsspeicher zeigen, sollte der Rückgabewert von **xlfCaller** immer in einem Aufruf der xlFree- [Funktion](xlfree.md) freigegeben werden, wenn er nicht mehr benötigt wird. 
  
Weitere Informationen zu **XLOPERs**/ **XLOPER12s** finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion ist die einzige nicht-Arbeitsblattfunktion, die von einer DLL/XLL-Arbeitsblattfunktion aufgerufen werden kann. Andere XML-Informationsfunktionen können nur über Befehle oder äquivalente Funktionen des Makros aufgerufen werden.
  
## <a name="example"></a>Beispiel

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Diese Funktion Ruft ein Befehlsmakro (xlcSelect) auf und funktioniert nur dann ordnungsgemäß, wenn es von einem Makroblatt aufgerufen wird.
  
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

