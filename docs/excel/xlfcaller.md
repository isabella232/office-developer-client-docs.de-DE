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
  
Gibt Informationen über die Zelle, den Zellbereich, den Befehl in einem Menü, ein Tool auf einer Symbolleiste oder ein Objekt zurück, das den aktuell ausgeführten DLL-Befehl oder die -Funktion aufgerufen hat.
  
|**Code, der von aufgerufen wird**|**gibt zurück**|
|:-----|:-----|
|DLL  <br/> |Die Register-ID.  <br/> |
|Eine einzelne Zelle  <br/> |Ein Einzelzellenverweis.  <br/> |
|Eine Arrayformel mit mehreren Zellen  <br/> |Ein Verweis auf mehrere Zellen.  <br/> |
|Ein bedingter Formatierungsausdruck  <br/> |Ein Verweis auf die Zelle, auf die die Formatierungsbedingung angewendet wird.  <br/> |
|Ein Menü  <br/> | Ein Array mit vier Elementen in einer Zeile:  <br/>  Die Balken-ID.  <br/>  Die Menüposition.  <br/>  Die Untermenüposition.  <br/>  Die Befehlsposition.  <br/> |
|Eine Symbolleiste  <br/> | Ein Array mit zwei Elementen in einer Zeile:  <br/>  Die Symbolleistennummer für integrierte Symbolleisten oder der Symbolleistenname für benutzerdefinierte Symbolleisten.  <br/>  Die Position auf der Symbolleiste.  <br/> |
|Ein Grafikobjekt  <br/> |Der Objektbezeichner (Objektname).  <br/> |
|Ein Befehl, der einem xlcOnEnter-On-Wert zugeordnet ist. ENTER, Ereignisfalle  <br/> |Ein Verweis auf die eingegebene Zelle oder Zelle.  <br/> |
|Ein Befehl, der einem xlcOnDoubleclick, ON, zugeordnet ist. DOUBLECLICK, Ereignisfalle.  <br/> |Die Zelle, auf die doppelgeklickt wurde (nicht unbedingt die aktive Zelle).  <br/> |
|Auto_Open, AutoClose, Auto_Activate oder Auto_Deactivate Makros  <br/> |Der Name des Anrufblatts.  <br/> |
|Andere Methoden nicht aufgeführt  <br/> |#REF! Fehler  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Der Rückgabewert ist einer der folgenden **XLOPER** /  **XLOPER12-Datentypen:** **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr** oder **xltypeMulti**. Da drei dieser Typen auf zugewiesenen Arbeitsspeicher verweisen, sollte der Rückgabewert von **xlfCaller** immer in einem Aufruf der [xlFree-Funktion](xlfree.md) frei, wenn er nicht mehr benötigt wird. 
  
Weitere Informationen zu **XLOPERs** /  **XLOPER12s** finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
## <a name="remarks"></a>Hinweise

Diese Funktion ist die einzige Nicht-Arbeitsblatt-Funktion, die von einer DLL/XLL-Arbeitsblattfunktion aufgerufen werden kann. Andere XLM-Informationsfunktionen können nur von Befehlen oder makroblattäquivalenten Funktionen aufgerufen werden.
  
## <a name="example"></a>Beispiel

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Diese Funktion ruft ein Befehlsmakro (xlcSelect) auf und funktioniert nur dann ordnungsgemäß, wenn sie von einem Makroblatt aufgerufen wird.
  
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

