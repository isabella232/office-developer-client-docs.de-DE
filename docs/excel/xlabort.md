---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- xlabort-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d19bbf949bc77a67fa84417e2eead2826c970eca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596848"
---
# <a name="xlabort"></a>xlAbort

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt den Prozessor an andere Aufgaben im System zurück und überprüft, ob der Benutzer **ESC** gedrückt hat, um ein Makro abzubrechen. Wenn der Benutzer während einer Arbeitsmappenneuberechnung **ESC** gedrückt hat, kann er auch innerhalb einer Arbeitsblattfunktion erkannt werden, indem diese Funktion aufgerufen wird. 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a>Parameter

 _pxRetain_ (**xltypeBool**)
  
(Optional). Bei **FALSE** überprüft diese Funktion die Unterbrechungsbedingung und löscht alle ausstehenden Unterbrechungen. Dadurch kann der Benutzer trotz der Unterbrechungsbedingung fortfahren. Wenn dieses Argument ausgelassen wird oder **TRUE** ist, sucht die Funktion nach einem Benutzerabbruch, ohne es zu löschen.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt **TRUE** (**xltypeBool**) zurück, wenn der Benutzer **ESC** gedrückt hat.
  
## <a name="remarks"></a>HinwBemerkungeneise

### 

#### <a name="frequent-calls-may-be-needed"></a>Häufige Anrufe sind möglicherweise erforderlich.

Funktionen und Befehle, die lange dauern könnten, sollten diese Funktion häufig aufrufen, um den Prozessor anderen Aufgaben im System zu übergeben.
  
#### <a name="avoid-sensitive-language"></a>Vermeiden vertraulicher Sprache

Vermeiden Sie die Verwendung des Begriffs "Abort" auf der Benutzeroberfläche. Erwägen Sie stattdessen die Verwendung von "Abbrechen", "Anhalten", "Unterbrechen" oder "Beenden".
  
## <a name="example"></a>Beispiel

Der folgende Code verschiebt die aktive Zelle wiederholt auf ein Blatt, bis eine Minute verstrichen ist oder bis der Benutzer **ESC** drückt. Die Funktion **xlAbort** wird gelegentlich aufgerufen. Dies ergibt den Prozessor und erleichtert das kooperative Multitasking. 
  
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



[C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

