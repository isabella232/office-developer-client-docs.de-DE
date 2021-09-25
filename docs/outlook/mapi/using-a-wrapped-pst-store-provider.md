---
title: Verwenden eines Anbieters von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 7df7e09410d069d53cea57acc49346d0ee74d967
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623901"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Verwenden eines Anbieters von umschlossenem PST-Speicher

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie einen Anbieter von umschlossenen PST-Speicherdateien (Personal Folders File) verwenden können, müssen Sie den Anbieter des umschlossenen PST-Speichers initialisieren und konfigurieren. Nachdem der Anbieter des umschlossenen PST-Speichers konfiguriert wurde, müssen Sie Funktionen implementieren, damit sich MAPI und der MAPI-Spooler beim Nachrichtenspeicheranbieter anmelden können. Weitere Informationen zum Initialisieren und Anmelden bei einem Anbieter von umschlossenen PST-Speicher finden Sie unter [Initialisieren eines umschlossenen PST-Store Anbieters](initializing-a-wrapped-pst-store-provider.md) und [Anmelden bei einem umschlossenen PST-Store Anbieter.](logging-on-to-a-wrapped-pst-store-provider.md)
  
Die **[IMAPISupport::IUnknown-Schnittstelle](imapisupportiunknown.md)** stellt Implementierungen für Aufgaben bereit, die häufig von Nachrichtenspeicheranbietern ausgeführt werden. Diese Schnittstelle muss umbrochen werden, damit der Beispiel-PST-Store-Anbieter funktioniert. Die **[IMAPISupport::OpenProfileSection-Funktion](imapisupport-openprofilesection.md)** erfordert eine spezielle Implementierung. Alle anderen Funktionen können ihre Parameter an das zugrunde liegende umschlossene Objekt übergeben. 
  
In diesem Thema wird die **IMAPISupport::OpenProfileSection-Funktion** anhand eines Codebeispiels aus dem Beispiel für ein umschlossenes PST-Store-Anbieter veranschaulicht. Das Beispiel implementiert einen umschlossenen PST-Anbieter, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zum Herunterladen und Installieren des Beispiel-Anbieters für umbrochene PST-Store finden Sie unter [Installieren des Beispiels für einen umschlossenen PST-Store Anbieter.](installing-the-sample-wrapped-pst-store-provider.md) Weitere Informationen zur Replikations-API finden Sie unter ["Informationen zur Replikations-API".](about-the-replication-api.md)
  
Wenn Sie mit der Verwendung eines Anbieters für einen umschlossenen PST-Speicher fertig sind, müssen Sie den Anbieter des umschlossenen PST-Speichers ordnungsgemäß herunterfahren. Weitere Informationen finden Sie unter [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Open Profile Section-Routine

Die **[IMAPISupport::OpenProfileSection-Funktion](imapisupport-openprofilesection.md)** öffnet einen Abschnitt des aktuellen Profils. Die Funktion erfordert eine spezielle Behandlung in der Implementierung des umschlossenen PST-Speicheranbieters. Wenn  `pgNSTGlobalProfileSectionGuid` dies angefordert wird, gibt die Funktion den Profilabschnitt zurück, der zwischengespeichert wird. 
  
### <a name="csupportopenprofilesection-example"></a>CSupport::OpenProfileSection() (Beispiel)

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

- [Informationen zum Beispiel für pst-Store-Anbieter mit Umschlossenen](about-the-sample-wrapped-pst-store-provider.md)
- [Installieren des PsT-Beispielanbieters Store](installing-the-sample-wrapped-pst-store-provider.md)
- [Initialisieren eines Anbieters von umschlossenen PST-Store](initializing-a-wrapped-pst-store-provider.md)
- [Anmelden bei einem Anbieter von umschlossenen PST-Store](logging-on-to-a-wrapped-pst-store-provider.md)
- [Herunterfahren eines Anbieters von umschlossenen PST-Store](shutting-down-a-wrapped-pst-store-provider.md)

