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
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08ab69252520e76a5631c5e32a3970d2d95b1ff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436657"
---
# <a name="xlabort"></a>xlAbort

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt den Prozessor anderen Aufgaben im System zu und überprüft, ob der Benutzer **esC** gedrückt hat, um ein Makro abgesagt zu haben. Wenn der Benutzer während einer Neuberechnung der Arbeitsmappe **esC** gedrückt hat, kann er auch innerhalb einer Arbeitsblattfunktion erkannt werden, indem diese Funktion aufruft. 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a>Parameter

 _pxRetain_ (**xltypeBool**)
  
(Optional). Bei **FALSE** überprüft diese Funktion die Unterbrechungsbedingung und alle ausstehenden Unterbrechungen. Dadurch kann der Benutzer trotz der Unterbrechungsbedingung fortfahren. Wenn dieses Argument ausgelassen wird oder **TRUE** ist, sucht die Funktion nach einem Benutzerabbruch, ohne es zu löschen.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt **TRUE** (**xltypeBool**) zurück, wenn der Benutzer **ESC gedrückt hat.**
  
## <a name="remarks"></a>Hinweise

### 

#### <a name="frequent-calls-may-be-needed"></a>Häufige Anrufe sind möglicherweise erforderlich

Funktionen und Befehle, die sehr lange dauern können, sollten diese Funktion häufig aufrufen, um dem Prozessor andere Aufgaben im System zu ermöglichen.
  
#### <a name="avoid-sensitive-language"></a>Vermeiden vertraulicher Sprache

Vermeiden Sie die Verwendung des Begriffs "Abort" in Der Benutzeroberfläche. Erwägen Sie stattdessen die Verwendung von "Cancel", "Halt", "Break" oder "Stop".
  
## <a name="example"></a>Beispiel

Der folgende Code verschiebt die aktive Zelle auf einem Blatt wiederholt, bis eine Minute verstrichen ist oder bis der Benutzer **ESC drückt.** Die Funktion **xlAbort** wird gelegentlich aufruft. Dies führt zu einer Beschleunigung des kooperativen Multitaskings durch den Prozessor. 
  
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

