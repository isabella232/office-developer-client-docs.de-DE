---
title: Verwenden eines Anbieters von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Letzte Änderung: 03. Juli 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420822"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Verwenden eines Anbieters von umschlossenem PST-Speicher

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie einen umschlossenen Anbieter für persönliche Ordner (PST)-Speicher verwenden können, müssen Sie den umschlossenen ANBIETER für den PST-Speicher initialisieren und konfigurieren. Nachdem der umschlossene PST Store-Anbieter konfiguriert wurde, müssen Sie Funktionen implementieren, damit sich MAPI und der MAPI-Spooler beim Nachrichtenspeicheranbieter anmelden können. Weitere Informationen zum Initialisieren und Anmelden bei einem umschlossenen PST Store-Anbieter finden Sie unter [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) und [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).
  
Die **[IMAPISupport::IUnknown-Schnittstelle](imapisupportiunknown.md)** stellt Implementierungen für Aufgaben bereit, die häufig von Nachrichtenspeicheranbietern ausgeführt werden. Diese Schnittstelle muss umschlossen werden, damit der Beispielanbieter für umschlossenes PST Store funktioniert. Die **[IMAPISupport::OpenProfileSection-Funktion](imapisupport-openprofilesection.md)** erfordert eine spezielle Implementierung. Alle anderen Funktionen können ihre Parameter an das zugrunde liegende umschlossene Objekt übergeben. 
  
In diesem Thema wird die **IMAPISupport::OpenProfileSection-Funktion** mithilfe eines Codebeispiels aus dem Beispiel umschlossenen PST-Store demonstriert. Das Beispiel implementiert einen umschlossenen PST-Anbieter, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zum Herunterladen und Installieren des Beispielanbieters für umbrochene PST Store finden Sie unter [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Weitere Informationen zur Replikations-API finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md).
  
Wenn Sie die Verwendung eines umschlossenen PST Store-Anbieters abgeschlossen haben, müssen Sie den umschlossenen ANBIETER für den PST Store ordnungsgemäß herunterfahren. Weitere Informationen finden Sie unter [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Open Profile Section-Routine

Die **[IMAPISupport::OpenProfileSection-Funktion](imapisupport-openprofilesection.md)** öffnet einen Abschnitt des aktuellen Profils. Die Funktion erfordert eine spezielle Behandlung in der Implementierung des umschlossenen PST Store-Anbieters. Wenn der  `pgNSTGlobalProfileSectionGuid` angefordert wird, gibt die Funktion den zwischengespeicherten Profilabschnitt zurück. 
  
### <a name="csupportopenprofilesection-example"></a>CSupport::OpenProfileSection()-Beispiel

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

- [Informationen zum Beispiel umschlossenen STORE Anbieter](about-the-sample-wrapped-pst-store-provider.md)
- [Installieren des Umschlossenen Store -Beispielanbieters](installing-the-sample-wrapped-pst-store-provider.md)
- [Initialisieren eines umschlossenen STORE Anbieters](initializing-a-wrapped-pst-store-provider.md)
- [Anmelden bei einem umschlossenen STORE Anbieter](logging-on-to-a-wrapped-pst-store-provider.md)
- [Herunterfahren eines umschlossenen STORE Anbieters](shutting-down-a-wrapped-pst-store-provider.md)

