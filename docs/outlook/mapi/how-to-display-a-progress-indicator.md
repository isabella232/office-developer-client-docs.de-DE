---
title: Anzeigen einer Statusanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7b0ce0ab75ffdce045ccde5bf6ea8a7da046f463
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345129"
---
# <a name="display-a-progress-indicator"></a>Anzeigen einer Statusanzeige
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um eine Statusanzeige anzuzeigen, rufen Sie [IMAPIProgress::](imapiprogress-getflags.md) GetFlags auf, um die aktuelle Flags-Einstellung abzurufen. 
  
Wenn das MAPI_TOP_LEVEL-Flag festgelegt ist, führen Sie die folgenden Schritte aus:
  
1. Legen Sie eine Variable auf die Gesamtanzahl der Elemente fest, die im Vorgang verarbeitet werden sollen. Wenn Sie beispielsweise den Inhalt eines Ordners kopieren, entspricht dieser Wert der Anzahl der Unterordner im Ordner und der Anzahl der Nachrichten. 
    
2. Legen Sie eine Variable auf 1000 geteilt durch die Anzahl der Elemente fest. 
    
3. Wenn Sie den Fortschritt für unter Objekte anzeigen möchten, rufen Sie die [IMAPIProgress::](imapiprogress-setlimits.md) setlimits-Methode des Progress-Objekts auf, und übergeben Sie die folgenden Werte für die drei Parameter: 
    
   - Legen Sie den Parameter _lpulMin_ auf 0 fest. 
    
   - Legen Sie den _lpulMax_ -parameter auf 1000. 
    
   - Legen Sie den Parameter _lpulFlags_ auf MAPI_TOP_LEVEL. 
    
4. Führen Sie für jedes zu verarbeitende Objekt die folgenden Schritte aus:
    
   1. Rufen Sie **IMAPIProgress::** setlimits auf, und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den Parameter _lpulMin_ auf die Variable fest, die in Schritt 2 mit dem aktuellen Element minus 1 multipliziert wird. 
      
     - Legen Sie den _lpulMax_ -Parameter auf die Variable fest, die in Schritt 2 mit dem aktuellen Objekt multipliziert wird. 
      
     - Legen Sie den Parameter _lpulFlags_ auf 0 fest. 
      
   2. Führen Sie die Verarbeitung aus, die für dieses Objekt ausgeführt werden soll. Wenn es sich um ein Unterobjekt handelt und Sie den Fortschritt für unter Objekte anzeigen möchten, übergeben Sie einen Zeiger auf das Progress-Objekt im _lpProgress_ -Parameter an die Methode. 
      
   3. Rufen Sie [IMAPIProgress::P rogress](imapiprogress-progress.md) auf, und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den _ulValue_ -Parameter auf die Variable fest, die in Schritt 2 mit dem aktuellen Objekt multipliziert wird. 
      
     - Legen Sie den Parameter _ulCount_ auf das aktuelle Objekt fest. 
      
     - Legen Sie den Parameter _ulTotal_ auf die in Schritt 1 festgelegte Variable fest, die Gesamtanzahl der Objekte. 
    
Wenn das MAPI_TOP_LEVEL-Flag nicht festgelegt ist, führen Sie die folgenden Schritte aus:
  
1. Rufen Sie die [IMAPIProgress:: GetMin](imapiprogress-getmin.md) -Methode des Progress-Objekts auf, um den kleinsten Wert für die Anzeige abzurufen. 
    
2. Rufen Sie [IMAPIProgress:: GetMax](imapiprogress-getmax.md) auf, um den Maximalwert für die Anzeige abzurufen. 
    
3. Legen Sie eine Variable fest, die der Gesamtanzahl der zu verarbeitenden Objekte entspricht. 
    
4. Legen Sie eine Variable fest, die dem Ergebnis entspricht, dass der Minimalwert vom Maximalwert subtrahiert und dann durch die Gesamtanzahl der Objekte geteilt wird.
    
5. Führen Sie für jedes zu verarbeitende Objekt die folgenden Schritte aus:
    
   1. Wenn Ihr Anbieter den Fortschritt für unter Objekte anzeigt, rufen Sie **IMAPIProgress::** setlimits auf, und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den Parameter _lpulMin_ auf den Minimalwert plus dem aktuellen Element minus 1 multipliziert mit der in Schritt 4 festgelegten Variable fest. 
      
     - Legen Sie den Parameter _lpulMax_ auf den Minimalwert plus der aktuellen Einheit fest, multipliziert mit der in Schritt 4 festgelegten Variable. 
      
     - Legen Sie den Parameter _lpulFlags_ auf 0 fest. 
      
   2. Führen Sie die Verarbeitung aus, die für dieses Objekt ausgeführt werden soll. Wenn das Objekt ein Unterobjekt ist und Ihr Anbieter den Fortschritt für unter Objekte anzeigt, übergeben Sie einen Zeiger auf das Progress-Objekt im _lpProgress_ -Parameter an die Methode. 
      
   3. Rufen Sie [IMAPIProgress::P rogress](imapiprogress-progress.md) auf, und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den Parameter _ulValue_ auf Variable festgelegt, die in Schritt 2 mit dem aktuellen Objekt multipliziert wird. 
      
     - Legen Sie den Parameter _ulCount_ auf 0 fest. 
      
     - Legen Sie den Parameter _ulTotal_ auf 0 fest. 
    
Das folgende Codebeispiel veranschaulicht die Logik, die erforderlich ist, um den Fortschritt auf allen Ebenen eines Vorgangs anzuzeigen, die den Inhalt eines Ordners mit fünf Unterordnern kopiert. 
  
```cpp
lpProgress->GetFlags (lpulFlags);
ulFlags = *lpulFlags;
/* The folder in charge of the display. It contains 5 subfolders. */
if (ulFlags & MAPI_TOP_LEVEL)
{
    ulItems = 5                         // 5 subfolders in this folder
    ulScale = (ulMax / ulItems)         // 200 because ulMax = 1000
    lpProgress->SetLimits(0, ulMax, MAPI_TOP_LEVEL)
    for (i = 1; i <= ulItems; i++)      // for each subfolder to copy
    {
        lpProgress->SetLimits( (i - 1) * ulScale, i * ulScale, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        lpProgress->Progress( i * ulScale, i, ulItems)
    }
}
else
/* One of the subfolders to be copied. It contains 3 messages. */
{
    lpProgress->GetMin(&ulMin);
    lpProgress->GetMax(&ulMax);
    ulItems = 3;
    ulDelta = (ulMax - ulMin) / ulItems;
    for (i = 1; i <= ulItems; i++)
    {
        lpProgress->SetLimits(ulMin + (i - 1) * ulDelta,
                              ulMin + i * ulDelta, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        /* Pass 0 for ulCount and ulTotal because this is not the */
        /* top-level display, and that information is unavailable  */
        lpProgress->Progress( i * ulDelta, 0, 0)
    }
}
 
```

## <a name="see-also"></a>Siehe auch

- [MAPI-fortSchrittsIndikatoren](mapi-progress-indicators.md)

