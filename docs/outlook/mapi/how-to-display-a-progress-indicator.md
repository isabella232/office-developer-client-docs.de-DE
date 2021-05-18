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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408026"
---
# <a name="display-a-progress-indicator"></a>Anzeigen einer Statusanzeige
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Rufen Sie zum Anzeigen eines Statusindikators [IMAPIProgress::GetFlags](imapiprogress-getflags.md) auf, um die aktuelle Flagseinstellung abzurufen. 
  
Wenn das MAPI_TOP_LEVEL festgelegt ist, führen Sie die folgenden Schritte aus:
  
1. Legen Sie eine Variable fest, die der Gesamtanzahl von Elementen entspricht, die im Vorgang zu verarbeiten sind. Wenn Sie z. B. den Inhalt eines Ordners kopieren, entspricht dieser Wert der Anzahl der Unterordner im Ordner plus der Anzahl der Nachrichten. 
    
2. Legen Sie eine Variable auf 1000 dividiert durch die Anzahl der Elemente fest. 
    
3. Wenn Sie den Fortschritt für Unterobjekte anzeigen, rufen Sie die [IMAPIProgress::SetLimits-Methode](imapiprogress-setlimits.md) des Progress-Objekts auf, und übergeben Sie die folgenden Werte für die drei Parameter: 
    
   - Legen Sie  _den lpulMin-Parameter_ auf 0. 
    
   - Legen Sie  _den lpulMax-Parameter_ auf 1000. 
    
   - Legen Sie  _den Parameter lpulFlags_ auf MAPI_TOP_LEVEL. 
    
4. Führen Sie für jedes zu verarbeitende Objekt die folgenden Schritte aus:
    
   1. Rufen **Sie IMAPIProgress::SetLimits auf,** und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie  _den lpulMin-Parameter_ auf die Variable fest, die in Schritt 2 multipliziert mit dem aktuellen Element minus 1 festgelegt ist. 
      
     - Legen Sie  _den lpulMax-Parameter_ auf die Variable fest, die in Schritt 2 multipliziert mit dem aktuellen Objekt festgelegt ist. 
      
     - Legen Sie  _den Parameter lpulFlags_ auf 0. 
      
   2. Führen Sie alle Verarbeitungsschritte aus, die für dieses Objekt durchgeführt werden sollen. Wenn es sich um ein Unterobjekt handelt und Sie den Fortschritt für Unterobjekte anzeigen möchten, übergeben Sie einen Zeiger an das Progress-Objekt im  _lpProgress-Parameter_ an die -Methode. 
      
   3. Rufen [Sie IMAPIProgress::P rogress](imapiprogress-progress.md) auf, und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie  _den ulValue-Parameter_ auf die Variable fest, die in Schritt 2 multipliziert mit dem aktuellen Objekt festgelegt ist. 
      
     - Legen Sie  _den ulCount-Parameter_ auf das aktuelle Objekt. 
      
     - Legen Sie  _den ulTotal-Parameter_ auf die Variable fest, die in Schritt 1 festgelegt ist, die Gesamtanzahl der Objekte. 
    
Wenn das MAPI_TOP_LEVEL nicht festgelegt ist, führen Sie die folgenden Schritte aus:
  
1. Rufen Sie die [IMAPIProgress::GetMin-Methode](imapiprogress-getmin.md) des Progress-Objekts auf, um den Minimalwert für die Anzeige abzurufen. 
    
2. Rufen [Sie IMAPIProgress::GetMax auf,](imapiprogress-getmax.md) um den maximalen Wert für die Anzeige abzurufen. 
    
3. Legen Sie eine Variable fest, die der Gesamtanzahl der zu verarbeitende Objekte entspricht. 
    
4. Legen Sie eine Variable fest, die dem Ergebnis entspricht, indem Sie den Minimalwert vom Maximalwert subtrahieren und dann durch die Gesamtanzahl der Objekte dividieren.
    
5. Führen Sie für jedes zu verarbeitende Objekt die folgenden Schritte aus:
    
   1. Wenn Ihr Anbieter den Fortschritt für Unterobjekte zeigt, rufen Sie **IMAPIProgress::SetLimits** auf, und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie  _den lpulMin-Parameter_ auf den Minimalwert plus das aktuelle Element minus 1 multipliziert mit der variablen Einstellung in Schritt 4 fest. 
      
     - Legen Sie  _den lpulMax-Parameter_ auf den Minimalwert plus die aktuelle Einheit fest, multipliziert mit der Variablen in Schritt 4. 
      
     - Legen Sie  _den Parameter lpulFlags_ auf 0. 
      
   2. Führen Sie alle Verarbeitungsschritte aus, die für dieses Objekt durchgeführt werden sollen. Wenn es sich bei dem Objekt um ein Unterobjekt handelt und ihr Anbieter den Fortschritt für Unterobjekte anzeigt, übergeben Sie einen Zeiger an das Progress-Objekt im  _lpProgress-Parameter_ an die -Methode. 
      
   3. Rufen [Sie IMAPIProgress::P rogress](imapiprogress-progress.md) auf, und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie  _den ulValue-Parameter_ auf eine Variable fest, die in Schritt 2 multipliziert mit dem aktuellen Objekt festgelegt ist. 
      
     - Legen Sie  _den ulCount-Parameter_ auf 0. 
      
     - Legen Sie  _den ulTotal-Parameter_ auf 0. 
    
Im folgenden Codebeispiel wird die Logik veranschaulicht, die erforderlich ist, um den Fortschritt auf allen Ebenen eines Vorgangs anzuzeigen, der den Inhalt eines Ordners kopiert, der fünf Unterordner enthält. 
  
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

