---
title: Herunterfahren eines einGebundenen PST-Speicheranbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Zuletzt geändert: 02 Juli, 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282782"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Herunterfahren eines einGebundenen PST-Speicheranbieters

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachdem Sie einen eingebundenen PST-Speicheranbieter verwendet haben, müssen Sie den eingebundenen PST-Speicheranbieter ordnungsgemäß herunterfahren. Weitere Informationen zur Verwendung des eingebundenen PST-Speicheranbieters finden Sie unter [Verwenden eines EingebundenEN PST-Speicheranbieters](using-a-wrapped-pst-store-provider.md).
  
Zum Herunterfahren eines eingebundenen PST-Speicheranbieters müssen Sie die **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** -Funktion aufrufen. Diese Funktionen schließen den eingebundenen PST-Speicheranbieter ordnungsgemäß ab. 
  
In diesem Thema wird die **IMSProvider:: Shutdown** -Funktion anhand eines Codebeispiels aus dem eingebundenen PST-Speicheranbieter demonstriert. Im Beispiel wird ein eingebundener PST-Anbieter implementiert, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zum herunterladen und Installieren des eingeWickelten Beispiel-PST-Speicheranbieters finden Sie unter [Installing the Sample Wrapped Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Weitere Informationen zur Replikations-API finden Sie unter Informationen zur [Replikations-API](about-the-replication-api.md).
  
## <a name="shut-down-routine"></a>Herunterfahren der Routine

Der MAPI-Spooler Ruft die **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** -Funktion kurz vor dem Aufheben des eingebundenen PST-Speicheranbieters auf, sodass der verpackte PST-Speicheranbieter ordnungsgemäß heruntergefahren werden kann. Die Funktion beendet alle Sitzungsobjekte, die dem eingebundenen PST-Speicheranbieter zugeordnet sind. 
  
## <a name="cmsprovidershutdown-example"></a>CMSProvider:: ShutDown ()-Beispiel

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



[Informationen zum einGebundenen PST-Speicheranbieter](about-the-sample-wrapped-pst-store-provider.md)
  
[Installieren des eingeWickelten Beispiel-PST-Speicheranbieters](installing-the-sample-wrapped-pst-store-provider.md)
  
[Initialisieren eines einGebundenen PST-Speicheranbieters](initializing-a-wrapped-pst-store-provider.md)
  
[Anmelden bei einem einGebundenen PST-Speicheranbieter](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Verwenden eines einGebundenen PST-Speicheranbieters](using-a-wrapped-pst-store-provider.md)

