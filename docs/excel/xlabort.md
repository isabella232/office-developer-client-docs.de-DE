---
title: Bereichsgröße
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- Bereichsgröße-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e90cbe496404b4cc602dee1ad21c91c8f5f91bfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790588"
---
# <a name="xlabort"></a>Bereichsgröße

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ergibt den Prozessor an anderen Vorgängen im System und überprüft, ob der Benutzer die **ESC-Taste** , um ein Makro abzubrechen gedrückt hat. Wenn der Benutzer während einer neuberechnung Arbeitsmappe die **ESC-Taste** gedrückt wurde, können sie auch aus innerhalb einer Tabellenfunktion erkannt werden durch Aufrufen dieser Funktion. 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a>Parameter

 _pxRetain_ (**XltypeBool**)
  
(Optional). Wenn **FALSE**, diese Funktion für die Unterbrechung überprüft und löscht alle ausstehenden Umbruch. Dies ermöglicht dem Benutzer trotz der Unterbrechung fortgesetzt. Wenn dieses Argument ausgelassen wird oder den Wert **TRUE**, überprüft die Funktion für den Abbruch eines Benutzers ohne löschen.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Gibt **TRUE** (**XltypeBool**) zurück, wenn der Benutzer die **ESC-Taste**gedrückt wurde.
  
## <a name="remarks"></a>Hinweise

### 

#### <a name="frequent-calls-may-be-needed"></a>Häufig ist eventuell erforderlich

Funktionen und Befehle, die eine lange dauern konnte sollte diese Funktion häufig, um den Prozessor an anderen Vorgängen im System zu erzielen aufrufen.
  
#### <a name="avoid-sensitive-language"></a>Vermeiden Sie vertrauliche Sprache

Vermeiden der Verwendung des Begriffs "Abbrechen" auf der Benutzeroberfläche. Erwägen, "Abbrechen", "Anhalten", "Unterbrochen" oder "Stop" stattdessen.
  
## <a name="example"></a>Beispiel

Mit dem folgende Code wird die aktive Zelle wiederholt auf einem Blatt verschoben, bis eine Minute vergangen ist oder der Benutzer die **ESC-Taste**drückt. Sie ruft die Funktion **Bereichsgröße** gelegentlich. Dies ergibt Prozessor, gemeinsame Multitasking Beschleunigung. 
  
 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
int WINAPI fDance(void)
{
   DWORD dtickStart;
   XLOPER12 xAbort, xConfirm;
   int boolSheet;
   int col=0;
   XCHAR rgch[32];
//
// Check what kind of sheet is active. If it is a worksheet or macro
// sheet, this function will move the selection in a loop to show
// activity. In any case, it will update the status bar with a countdown.
//
// Call xlSheetId; if that fails the current sheet is not a macro sheet or
// worksheet. Next, get the time at which to start. Then start a while
// loop that will run for one minute. During the while loop, check if the
// user has pressed ESC. If true, confirm the abort. If the abort is
// confirmed, clear the message bar and return; if the abort is not
// confirmed, clear the abort state and continue. After checking for an
// abort, move the active cell if on a worksheet or macro. Then
// update the status bar with the time remaining.
//
// This block uses TempActiveCell12(), which creates a temporary XLOPER12.
// The XLOPER12 contains a reference to a single cell on the active sheet.
// This function is part of the framework library.
//
   boolSheet = (Excel12f(xlSheetId, 0, 0) == xlretSuccess);
   dtickStart = GetTickCount();
   while (GetTickCount() < dtickStart + 60000L)
   {
      Excel12f(xlAbort, &xAbort, 0);
      if (xAbort.val.xbool)
      {
         Excel12f(xlcAlert, &xConfirm, 2,
           TempStr12(L"Are you sure you want to cancel this operation?"),
              TempNum12(1));
         if (xConfirm.val.xbool)
         {
            Excel12f(xlcMessage, 0, 1, TempBool12(0));
            return 1;
         }
         else
         {
            Excel12f(xlAbort, 0, 1, TempBool12(0));
         }
      }
      if (boolSheet)
      {
         Excel12f(xlcSelect, 0, 1,
            TempActiveCell12(0,(BYTE)col));
         col = (col + 1) & 3;
      }
      wsprintfW(rgch,L"0:%lu",
         (60000 + dtickStart - GetTickCount()) / 1000L);
      Excel12f(xlcMessage, 0, 2, TempBool12(1), TempStr12(rgch));
   }
   Excel12f(xlcMessage, 0, 1, TempBool12(0));
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

