---
title: Herunterfahren eines Anbieters von umschlossenen PST-Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 3f4aa55a8b557c8c14678bea618b761a22d7f96a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619757"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Herunterfahren eines Anbieters von umschlossenen PST-Store

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachdem Sie mit der Verwendung eines ANBIETERs für einen umschlossenen PST-Speicher (Personal Folders File) fertig sind, müssen Sie den Anbieter des umschlossenen PST-Speichers ordnungsgemäß herunterfahren. Weitere Informationen zur Verwendung des Anbieters des umschlossenen PST-Speichers finden Sie unter [Verwenden eines umschlossenen PST-Store Anbieters.](using-a-wrapped-pst-store-provider.md)
  
Um einen anbieterumschlossenen PST-Speicher herunterzufahren, müssen Sie die **[IMSProvider::Shutdown-Funktion](imsprovider-shutdown.md)** aufrufen. Mit diesen Funktionen wird der Anbieter des umschlossenen PST-Speichers in geordneter Reihenfolge geschlossen. 
  
In diesem Thema wird die **IMSProvider::Shutdown-Funktion** anhand eines Codebeispiels aus dem Beispiel für ein umbrochenes PST-Store-Anbieter veranschaulicht. Das Beispiel implementiert einen umschlossenen PST-Anbieter, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zum Herunterladen und Installieren des Beispiel-Anbieters für umbrochene PST-Store finden Sie unter [Installieren des Beispiel-Anbieters für umschlossene PST-Store.](installing-the-sample-wrapped-pst-store-provider.md) Weitere Informationen zur Replikations-API finden Sie unter ["Informationen zur Replikations-API".](about-the-replication-api.md)
  
## <a name="shut-down-routine"></a>Herunterfahren-Routine

Der MAPI-Spooler ruft die **[IMSProvider::Shutdown-Funktion](imsprovider-shutdown.md)** direkt vor der Veröffentlichung des Anbieters des umschlossenen PST-Speichers auf, sodass der Anbieter des umschlossenen PST-Speichers ordnungsgemäß heruntergefahren werden kann. Die Funktion beendet alle Sitzungsobjekte, die dem anbieterumschlossenen PST-Speicher zugeordnet sind. 
  
## <a name="cmsprovidershutdown-example"></a>CMSProvider::ShutDown() (Beispiel)

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



[Informationen zum Beispiel für pst-Store-Anbieter mit Umschlossenen](about-the-sample-wrapped-pst-store-provider.md)
  
[Installieren des Beispielanbieters für pst-Store](installing-the-sample-wrapped-pst-store-provider.md)
  
[Initialisieren eines Anbieters von umschlossenen PST-Store](initializing-a-wrapped-pst-store-provider.md)
  
[Anmelden bei einem Anbieter von umschlossenen PST-Store](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Verwenden eines Anbieters von umschlossenen PST-Store](using-a-wrapped-pst-store-provider.md)

