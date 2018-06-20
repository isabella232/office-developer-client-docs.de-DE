---
title: Herunterfahren von einem Anbieter gepackten PST-Datei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Zuletzt geändert: 02 Juli 2012'
ms.openlocfilehash: 5c8ad7443b0c1aa05f48284e4b09859ab53dd2c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795533"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Herunterfahren von einem Anbieter gepackten PST-Datei

 
  
**Betrifft**: Outlook 
  
Nachdem Sie mithilfe eines gepackten Anbieters für Persönliche Ordner-Datei (PST) anmelden, müssen Sie die gepackten PST-Speicheranbieter ordnungsgemäß herunterfahren. Weitere Informationen zur Verwendung der gepackten PST Informationsdienst finden Sie unter [Verwenden einer gewrappt PST Store Provider](using-a-wrapped-pst-store-provider.md).
  
Um einem gepackten PST-Anbieter zu beenden, müssen Sie die Funktion **[IMSProvider::Shutdown](imsprovider-shutdown.md)** aufrufen. Diese Funktionen wird die gepackten PST Speicheranbieter ordnungsgemäß geschlossen. 
  
In diesem Thema wird die Funktion **IMSProvider::Shutdown** mithilfe eines Codebeispiels aus der umbrochen PST Store Beispielanbieter veranschaulicht. Das Beispiel implementiert einen gepackten PST-Anbieter, der in Verbindung mit der API für die Replikation verwendet werden soll. Weitere Informationen zum Herunterladen und Installieren der umbrochen PST Store Beispielanbieter finden Sie unter [Sample umfließendem PST Store Provider installieren](installing-the-sample-wrapped-pst-store-provider.md). Weitere Informationen zur Replikation-API finden Sie unter [Über die Replikation-API](about-the-replication-api.md).
  
## <a name="shut-down-routine"></a>Routine Herunterfahren

Die MAPI-Warteschlange Ruft die **[IMSProvider::Shutdown](imsprovider-shutdown.md)** -Funktion, bevor der gepackten PST Informationsdienst freigegeben, damit der gepackten PST Informationsdienst ordnungsgemäß heruntergefahren werden kann. Die Funktion wird beendet, alle Sitzungsobjekte, die den gepackten PST-Speicheranbieter zugeordnet. 
  
## <a name="cmsprovidershutdown-example"></a>CMSProvider::ShutDown()-Beispiel

```cpp
STDMETHODIMP CMSProvider::Shutdown(ULONG * pulFlags) 
{ 
    HRESULT hRes = S_OK; 
    Log(true,"CMSProvider::Shutdown\n"); 
    hRes =m_pPSTMS->Shutdown(pulFlags); 
    Log(true,"CMSProvider::Shutdown returned: 0x%08X\n", hRes); 
    return hRes ;  
}
```

## <a name="see-also"></a>Siehe auch



[Zum Beispiel umgebrochen PST-Anbieter](about-the-sample-wrapped-pst-store-provider.md)
  
[Installieren des Beispiels umfließendem PST-Anbieter](installing-the-sample-wrapped-pst-store-provider.md)
  
[Initialisieren einen Anbieter für umbrochenen PST anmelden](initializing-a-wrapped-pst-store-provider.md)
  
[Anmelden bei einem Anbieter gepackten PST-Datei](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Verwenden eines Anbieters gepackten PST-Speichers](using-a-wrapped-pst-store-provider.md)

