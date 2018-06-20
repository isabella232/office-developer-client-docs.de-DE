---
title: Anzeigen einer Statusanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3c4c553a000dab233eb208c1222cc427c97b1e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791851"
---
# <a name="display-a-progress-indicator"></a>Anzeigen einer Statusanzeige
 
**Betrifft**: Outlook 
  
Rufen Sie [IMAPIProgress::GetFlags](imapiprogress-getflags.md) zum Abrufen der aktuellen Flags festlegen, um eine Statusanzeige anzuzeigen. 
  
Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, führen Sie die folgenden Schritte aus:
  
1. Weisen Sie einer Variablen zur Gesamtanzahl der Elemente, die in den Vorgang verarbeitet. Angenommen, wenn Sie den Inhalt eines Ordners kopieren, wird dieser Wert gleich der Anzahl der Unterordner im Ordner plus die Anzahl der Nachrichten sein. 
    
2. Weisen Sie einer Variablen bis 1000 geteilt durch die Anzahl der Elemente. 
    
3. Wenn Sie den Fortschritt für Unterobjekte angezeigt werden, rufen Sie den Fortschritt des Objekts [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) -Methode, und übergeben Sie die folgenden Werte für die drei Parameter: 
    
   - Den Parameter _LpulMin_ auf 0 festgelegt. 
    
   - Den Parameter _LpulMax_ auf 1000 festgelegt. 
    
   - Den Parameter _LpulFlags_ auf MAPI_TOP_LEVEL festgelegt. 
    
4. Führen Sie für jedes Objekt verarbeitet werden die folgenden Schritte aus:
    
   1. Rufen Sie **IMAPIProgress::SetLimits** und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den _LpulMin_ -Parameter der Variablen, die in Schritt 2 des aktuellen Elements minus 1 multipliziert festgelegt. 
      
     - Legen Sie den _LpulMax_ -Parameter der Variablen, die in Schritt 2 multipliziert das aktuelle Objekt festgelegt. 
      
     - Den Parameter _LpulFlags_ auf 0 festgelegt. 
      
   2. Führen Sie die Verarbeitung für dieses Objekt ausgeführt werden soll. Wenn dies ein Unterobjekt ist und Fortschritt auf Unterobjekte angezeigt werden soll, übergeben Sie einen Zeiger auf das Objekt Fortschritt im _LpProgress_ -Parameter der Methode. 
      
   3. Rufen Sie [IMAPIProgress::Progress](imapiprogress-progress.md) und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den _UlValue_ -Parameter der Variablen, die in Schritt 2 multipliziert das aktuelle Objekt festgelegt. 
      
     - Den Parameter _UlCount_ auf das aktuelle Objekt festgelegt. 
      
     - Legen Sie den _UlTotal_ -Parameter der Variablen, die in Schritt 1, die Gesamtanzahl der Objekte festgelegt. 
    
Wenn das Flag MAPI_TOP_LEVEL nicht festgelegt ist, führen Sie die folgenden Schritte aus:
  
1. Rufen Sie den Fortschritt des Objekts [IMAPIProgress::GetMin](imapiprogress-getmin.md) -Methode zum Abrufen des Mindestwert für die Anzeige. 
    
2. Rufen Sie [IMAPIProgress::GetMax](imapiprogress-getmax.md) , um den Maximalwert für die Anzeige abzurufen. 
    
3. Weisen Sie einer Variablen zur Gesamtanzahl der Objekte verarbeitet werden. 
    
4. Weisen Sie einer Variablen auf das Ergebnis der Subtraktion des kleinsten Werts in den Höchstwert und klicken Sie dann Division durch die Gesamtanzahl der Objekte.
    
5. Führen Sie für jedes Objekt verarbeitet werden die folgenden Schritte aus:
    
   1. Wenn der Anbieter für Unterobjekte Fortschritt angezeigt wird, rufen Sie **IMAPIProgress::SetLimits** , und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den _LpulMin_ -Parameter auf den kleinsten Wert sowie das aktuelle Element minus 1 multipliziert die Variable, die in Schritt 4 festgelegt. 
      
     - Legen Sie den _LpulMax_ -Parameter auf den kleinsten Wert plus die aktuelle Maßeinheit multipliziert die Variable, die in Schritt 4 festgelegt. 
      
     - Den Parameter _LpulFlags_ auf 0 festgelegt. 
      
   2. Führen Sie die Verarbeitung für dieses Objekt ausgeführt werden soll. Wenn das Objekt ein Unterobjekt ist und Ihrem Anbieter zeigt den Status Unterobjekte, übergeben Sie einen Zeiger auf das Objekt Fortschritt im _LpProgress_ -Parameter an die-Methode. 
      
   3. Rufen Sie [IMAPIProgress::Progress](imapiprogress-progress.md) und übergeben Sie die folgenden Werte für die drei Parameter: 
      
     - Legen Sie den _UlValue_ -Parameter auf Variable, die in Schritt 2 multipliziert das aktuelle Objekt festgelegt. 
      
     - Den Parameter _UlCount_ auf 0 festgelegt. 
      
     - Den Parameter _UlTotal_ auf 0 festgelegt. 
    
Das folgende Codebeispiel veranschaulicht die Logik erforderlich, um den Fortschritt auf allen Ebenen eines Vorgangs angezeigt, die den Inhalt eines Ordners kopiert, die fünf Unterordner enthält. 
  
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

- [MAPI-Statusanzeigen](mapi-progress-indicators.md)

