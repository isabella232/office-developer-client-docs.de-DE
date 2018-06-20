---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- XlfCaller-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790592"
---
# <a name="xlfcaller"></a>xlfCaller

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt Informationen zu der Zelle, einen Bereich von Zellen, Befehl auf ein Menü, das Tool auf einer Symbolleiste oder das Objekt, das aufgerufen wird, die DLL-Befehl oder eine Funktion, die derzeit ausgeführt wird.
  
|**Aufgerufen von Code**|**gibt zurück**|
|:-----|:-----|
|DLL-DATEI  <br/> |Die Register-ID.  <br/> |
|Eine einzelne Zelle  <br/> |Bezug auf eine einzelne Zelle.  <br/> |
|Eine Zelle mit mehreren Arrayformel  <br/> |Ein mit mehreren Zellbezug.  <br/> |
|Eine bedingte Formatierung Ausdruck  <br/> |Ein Verweis auf die Zelle, die auf der die Formatierung Bedingung angewendet wird.  <br/> |
|Ein Menü  <br/> | Ein Array mit vier Elementen einzeilige:  <br/>  Die Leiste-ID.  <br/>  Die Menüposition im.  <br/>  Die Position des Untermenü.  <br/>  Die Position des Befehls.  <br/> |
|Eine Symbolleiste  <br/> | Eine einzeilige Matrix mit zwei Elementen:  <br/>  Die Anzahl der Symbolleiste für die integrierten Symbolleisten oder den Namen der Symbolleiste für benutzerdefinierte Symbolleisten.  <br/>  Die Position auf der Symbolleiste.  <br/> |
|Ein Graphic-Objekt  <br/> |Der Objektbezeichner (Objektname).  <br/> |
|Ein Befehl eine XlcOnEnter auf zugeordnet. Geben SIE Ereignis Trapping  <br/> |Ein Verweis auf die Zelle oder die Zellen eingegeben werden.  <br/> |
|Ein Befehl eine XlcOnDoubleclick auf zugeordnet. DOUBLECLICK, Ereignis Trapping.  <br/> |Die Zelle, die wurde doppelgeklickt (was nicht notwendigerweise die aktive Zelle).  <br/> |
|Auto_öffnen-, AutoClose-, Auto_aktivieren- oder Auto_deaktivieren-Makro  <br/> |Der Name des Blatts aufrufen.  <br/> |
|Andere Methoden nicht aufgeführt  <br/> |#REF! Fehler  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Der Rückgabewert ist eines der folgenden **XLOPER**/ **XLOPER12** Datentypen: **XltypeRef**, **XltypeSRef**, **XltypeNum**, **XltypeStr**, **XltypeErr**oder **XltypeMulti**. Da drei der folgenden Arten auf reservierter Speicher zeigen, sollten der Rückgabewert der **XlfCaller** immer freigegeben werden in einem Aufruf der [Funktion XlFree](xlfree.md) Wenn es nicht mehr benötigt wird. 
  
Weitere Informationen zu **XLOPERs**/ **XLOPER12s** finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
## <a name="remarks"></a>Hinweise

Diese Funktion ist nur nicht-Arbeitsblatt, die aus einer Tabellenfunktion DLL/XLL aufgerufen werden können. Andere XLM-Informationsfunktionen können nur von Befehlen oder Makroblatt Äquivalent aufgerufen werden Funktionen.
  
## <a name="example"></a>Beispiel

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Diese Funktion ruft ein Makro mit Befehlen (XlcSelect) und funktionieren ordnungsgemäß nur, wenn von einem Makroblatt aufgerufen.
  
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



[Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

