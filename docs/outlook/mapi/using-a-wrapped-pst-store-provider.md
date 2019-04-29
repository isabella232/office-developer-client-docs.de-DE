---
title: Verwenden eines Anbieters von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Zuletzt geändert: 03 Juli, 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420822"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Verwenden eines Anbieters von umschlossenem PST-Speicher

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie einen eingebundenen PST-Speicheranbieter verwenden können, müssen Sie den eingebundenen PST-Speicheranbieter initialisieren und konfigurieren. Nach der Konfiguration des eingebundenen PST-Speicheranbieters müssen Sie Funktionen implementieren, damit MAPI und der MAPI-Spooler sich beim Nachrichtenspeicher Anbieter anmelden können. Weitere Informationen zum Initialisieren und Anmelden bei einem eingebundenen PST-Speicheranbieter finden Sie unter [Initialisieren eines EingebundenEN PST-Speicheranbieters](initializing-a-wrapped-pst-store-provider.md) und [Anmelden bei einem](logging-on-to-a-wrapped-pst-store-provider.md)eingebundenen PST-Speicheranbieter.
  
Die **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** -Schnittstelle stellt Implementierungen für Aufgaben bereit, die häufig von Nachrichtenspeicher Anbietern ausgeführt werden. Diese Schnittstelle muss umbrochen werden, damit der beispielhafte PST-Speicheranbieter funktioniert. Die **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** -Funktion erfordert eine spezielle Implementierung. Alle anderen Funktionen können Ihre Parameter an das zugrunde liegende Wrapped-Objekt übergeben. 
  
In diesem Thema wird die **IMAPISupport:: OpenProfileSection** -Funktion anhand eines Codebeispiels aus dem eingebundenen PST-Speicheranbieter demonstriert. Im Beispiel wird ein eingebundener PST-Anbieter implementiert, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zum herunterladen und Installieren des eingeWickelten Beispiel-PST-Speicheranbieters finden Sie unter [Installing the Sample Wrapped Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Weitere Informationen zur Replikations-API finden Sie unter Informationen zur [Replikations-API](about-the-replication-api.md).
  
Wenn Sie einen eingebundenen PST-Speicheranbieter abgeschlossen haben, müssen Sie den eingebundenen PST-Speicheranbieter ordnungsgemäß herunterfahren. Weitere Informationen finden Sie unter [Herunterfahren eines EingebundenEN PST-Speicheranbieters](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Open profile section-Routine

Die **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** -Funktion öffnet einen Abschnitt des aktuellen Profils. Die Funktion erfordert eine besondere Behandlung in der eingebundenen PST-Speicheranbieter Implementierung. Wenn der `pgNSTGlobalProfileSectionGuid` angefordert wird, gibt die Funktion den Profil Abschnitt zurück, der zwischengespeichert wird. 
  
### <a name="csupportopenprofilesection-example"></a>CSupport:: OpenProfileSection ()-Beispiel

```cpp
STDMETHODIMP CSupport::OpenProfileSection( 
    LPMAPIUID lpUid,     
    ULONG ulFlags, 
    LPPROFSECT * lppProfileObj) 
{ 
    Log(true,"CSupport::OpenProfileSection\n"); 
    if (lpUid &&  
        IsEqualMAPIUID(lpUid, (void *)&pbNSTGlobalProfileSectionGuid) &&  
        m_lpProfSect) 
    {      
        // Allow the opening of the Global Section 
        if (m_lpProfSect) 
        { 
            *lppProfileObj = m_lpProfSect; 
            (*lppProfileObj)->AddRef(); 
            return S_OK; 
        } 
    } 
    return m_pMAPISup->OpenProfileSection(lpUid, ulFlags, lppProfileObj); 
}
```

## <a name="see-also"></a>Siehe auch

- [Informationen zum einGebundenen PST-Speicheranbieter](about-the-sample-wrapped-pst-store-provider.md)
- [Installieren des eingeWickelten Beispiel-PST-Speicheranbieters](installing-the-sample-wrapped-pst-store-provider.md)
- [Initialisieren eines einGebundenen PST-Speicheranbieters](initializing-a-wrapped-pst-store-provider.md)
- [Anmelden bei einem einGebundenen PST-Speicheranbieter](logging-on-to-a-wrapped-pst-store-provider.md)
- [Herunterfahren eines einGebundenen PST-Speicheranbieters](shutting-down-a-wrapped-pst-store-provider.md)

