---
title: Verwenden von einem gepackten PST-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Zuletzt geändert: 03 Juli 2012'
ms.openlocfilehash: 4a2ccbbcdd3459af6b69156d80b37695251ba8d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795817"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Verwenden von einem gepackten PST-Anbieter

**Betrifft**: Outlook 
  
Bevor Sie einen gepackten Anbieter für Persönliche Ordner-Datei (PST) anmelden verwenden können, müssen Sie initialisieren und der gepackten PST-Informationsdienst konfigurieren. Nachdem der gepackten PST-Speicher-Anbieter konfiguriert ist, müssen Sie Funktionen implementieren, sodass MAPI und die MAPI-Warteschlange auf die Nachricht-Anbieter anmelden können. Weitere Informationen zu initialisieren und Anmelden bei einem gepackten PST-Anbieter finden Sie unter [Initialisieren einer gewrappt PST Store Provider](initializing-a-wrapped-pst-store-provider.md) und [Protokollierung für den Zugriff auf einen umbrochen PST-speichern-Anbieter](logging-on-to-a-wrapped-pst-store-provider.md).
  
Die **[IMAPISupport::IUnknown](imapisupportiunknown.md)** -Schnittstelle stellt Implementierungen für die Nachricht häufig ausgeführten Aufgaben Anbieter. Diese Schnittstelle muss für den umfließendem PST Store Beispielanbieter funktioniert eingeschlossen werden. Die Funktion **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** erfordert spezielle Implementierung. Alle anderen Funktionen können ihren Parametern an das zugrunde liegende gepackten Objekt übergeben werden. 
  
In diesem Thema wird die Funktion **IMAPISupport::OpenProfileSection** mithilfe eines Codebeispiels aus der umbrochen PST Store Beispielanbieter veranschaulicht. Das Beispiel implementiert einen gepackten PST-Anbieter, der in Verbindung mit der API für die Replikation verwendet werden soll. Weitere Informationen zum Herunterladen und Installieren der umbrochen PST Store Beispielanbieter finden Sie unter [Sample umfließendem PST Store Provider installieren](installing-the-sample-wrapped-pst-store-provider.md). Weitere Informationen zur Replikation-API finden Sie unter [Über die Replikation-API](about-the-replication-api.md).
  
Wenn Sie fertig sind, mit einem gepackten PST-Anbieter, müssen Sie die gepackten PST-Speicheranbieter ordnungsgemäß herunterfahren. Weitere Informationen finden Sie unter [Herunterfahren nach unten ein umfließendem PST Store Anbieter](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Open Benutzerprofilabschnitt routine

Die **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** -Funktion wird das aktuelle Profil einen Abschnitt geöffnet. Die Funktion erfordert besondere Behandlung in der gepackten PST-Speicher-Anbieter-Implementierung. Wenn die `pgNSTGlobalProfileSectionGuid` angefordert, Profilabschnitt, die zwischengespeichert wird von der Funktion zurückgegeben. 
  
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

- [Informationen über das Beispiel für einen Anbieter von umschlossenem PST-Speicher](about-the-sample-wrapped-pst-store-provider.md)
- [Installieren des Beispiel für einen Anbieter von umschlossenem PST-Speicher](installing-the-sample-wrapped-pst-store-provider.md)
- [Initialisieren eines Anbieters von umschlossenem PST-Speicher](initializing-a-wrapped-pst-store-provider.md)
- [Anmelden bei einem Anbieter von umschlossenem PST-Speicher](logging-on-to-a-wrapped-pst-store-provider.md)
- [Herunterfahren eines Anbieters von umschlossenem PST-Speicher](shutting-down-a-wrapped-pst-store-provider.md)

