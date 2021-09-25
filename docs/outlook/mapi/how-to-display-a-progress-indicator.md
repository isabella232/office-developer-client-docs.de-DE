---
title: Anzeigen einer Statusanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 892882531df4fd857e7eb525a615657f5ef4e4e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551429"
---
# <a name="display-a-progress-indicator"></a>Anzeigen einer Statusanzeige
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Rufen Sie zum Anzeigen einer Statusanzeige [IMAPIProgress::GetFlags](imapiprogress-getflags.md) auf, um die aktuelle Flags-Einstellung abzurufen. 
  
Wenn das flag MAPI_TOP_LEVEL festgelegt ist, führen Sie die folgenden Schritte aus:
  
1. Legen Sie eine Variable fest, die der Gesamtanzahl der elemente entspricht, die im Vorgang verarbeitet werden sollen. Wenn Sie z. B. den Inhalt eines Ordners kopieren, entspricht dieser Wert der Anzahl der Unterordner im Ordner plus der Anzahl der Nachrichten. 
    
2. Legen Sie eine Variable auf 1000 fest, dividiert durch die Anzahl der Elemente. 
    
3. Wenn Sie den Fortschritt für Unterobjekte anzeigen, rufen Sie die [IMAPIProgress::SetLimits-Methode](imapiprogress-setlimits.md) des Fortschrittsobjekts auf, und übergeben Sie die folgenden Werte für die drei Parameter: 
    
   - Legen Sie den  _lpulMin-Parameter_ auf 0 fest. 
    
   - Legen Sie den  _Parameter lpulMax_ auf 1000 fest. 
    
   - Legen Sie den  _Parameter lpulFlags_ auf MAPI_TOP_LEVEL fest. 
    
4. Führen Sie für jedes zu verarbeitende Objekt die folgenden Schritte aus:
    
   1. Rufen Sie **IMAPIProgress::SetLimits auf,** und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den  _lpulMin-Parameter_ auf die in Schritt 2 festgelegte Variable fest, multipliziert mit dem aktuellen Element minus 1. 
      
     - Legen Sie den  _lpulMax-Parameter_ auf die Variable fest, die in Schritt 2 mit dem aktuellen Objekt multipliziert wurde. 
      
     - Legen Sie den  _lpulFlags-Parameter_ auf 0 fest. 
      
   2. Führen Sie die Verarbeitung für dieses Objekt aus. Wenn es sich um ein Unterobjekt handelt und Sie den Fortschritt von Unterobjekten anzeigen möchten, übergeben Sie einen Zeiger auf das Statusobjekt im  _lpProgress-Parameter_ an die Methode. 
      
   3. Rufen Sie [IMAPIProgress::P rogress auf,](imapiprogress-progress.md) und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den  _ulValue-Parameter_ auf die Variable fest, die in Schritt 2 mit dem aktuellen Objekt multipliziert wurde. 
      
     - Legen Sie den  _ulCount-Parameter_ auf das aktuelle Objekt fest. 
      
     - Legen Sie den  _ulTotal-Parameter_ auf die in Schritt 1 festgelegte Variable fest, die Gesamtzahl der Objekte. 
    
Wenn das flag MAPI_TOP_LEVEL nicht festgelegt ist, führen Sie die folgenden Schritte aus:
  
1. Rufen Sie die [IMAPIProgress::GetMin-Methode](imapiprogress-getmin.md) des Statusobjekts auf, um den Minimalwert für die Anzeige abzurufen. 
    
2. Rufen Sie [IMAPIProgress::GetMax](imapiprogress-getmax.md) auf, um den Maximalwert für die Anzeige abzurufen. 
    
3. Legen Sie eine Variable fest, die der Gesamtanzahl der zu verarbeitenden Objekte entspricht. 
    
4. Legen Sie eine Variable fest, die dem Ergebnis entspricht, dass der Mindestwert vom Maximalwert subtrahiert und dann durch die Gesamtanzahl der Objekte geteilt wird.
    
5. Führen Sie für jedes zu verarbeitende Objekt die folgenden Schritte aus:
    
   1. Wenn ihr Anbieter den Fortschritt für Unterobjekte anzeigt, rufen Sie **IMAPIProgress::SetLimits auf,** und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den  _Parameter lpulMin_ auf den Minimalwert plus das aktuelle Element minus 1 multipliziert mit der in Schritt 4 festgelegten Variablen fest. 
      
     - Legen Sie den  _Parameter lpulMax_ auf den Minimalwert plus die aktuelle Einheit multipliziert mit der in Schritt 4 festgelegten Variablen fest. 
      
     - Legen Sie den  _lpulFlags-Parameter_ auf 0 fest. 
      
   2. Führen Sie die Verarbeitung für dieses Objekt aus. Wenn es sich bei dem Objekt um ein Unterobjekt handelt und ihr Anbieter den Fortschritt für Unterobjekte anzeigt, übergeben Sie einen Zeiger auf das Statusobjekt im  _lpProgress-Parameter_ an die Methode. 
      
   3. Rufen Sie [IMAPIProgress::P rogress auf,](imapiprogress-progress.md) und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den  _ulValue-Parameter_ auf eine Variable fest, die in Schritt 2 multipliziert mit dem aktuellen Objekt festgelegt wird. 
      
     - Legen Sie den  _ulCount-Parameter_ auf 0 fest. 
      
     - Legen Sie den  _ulTotal-Parameter_ auf 0 fest. 
    
Im folgenden Codebeispiel wird die Logik veranschaulicht, die zum Anzeigen des Fortschritts auf allen Ebenen eines Vorgangs erforderlich ist, der den Inhalt eines Ordners kopiert, der fünf Unterordner enthält. 
  
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

- [MAPI-Fortschrittsindikatoren](mapi-progress-indicators.md)

