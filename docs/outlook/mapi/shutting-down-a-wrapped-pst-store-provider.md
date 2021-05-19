---
title: Herunterfahren eines umbrochenen PST Store-Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Letzte Änderung: 02. Juli 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409944"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Herunterfahren eines umbrochenen PST Store-Anbieters

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachdem Sie die Verwendung eines umschlossenen Anbieters für persönliche Ordner (PST)-Speicher abgeschlossen haben, müssen Sie den umschlossenen ANBIETER für den PST-Speicher ordnungsgemäß herunterfahren. Weitere Informationen zur Verwendung des umschlossenen PST Store-Anbieters finden Sie unter [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).
  
Zum Herunterfahren eines umschlossenen PST Store-Anbieters müssen Sie die **[IMSProvider::Shutdown-Funktion](imsprovider-shutdown.md)** aufrufen. Mit diesen Funktionen wird der umschlossene ANBIETER für den PST Store in geordneter Weise geschlossen. 
  
In diesem Thema wird die **IMSProvider::Shutdown-Funktion** mithilfe eines Codebeispiels aus dem Anbieter für den Pst Store mit Beispielwickeln demonstriert. Das Beispiel implementiert einen umschlossenen PST-Anbieter, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zum Herunterladen und Installieren des Beispielanbieters für den umschlossenen PST Store finden Sie unter [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Weitere Informationen zur Replikations-API finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md).
  
## <a name="shut-down-routine"></a>Herunterfahren der Routine

Der MAPI-Spooler ruft die **[IMSProvider::Shutdown-Funktion](imsprovider-shutdown.md)** kurz vor der Veröffentlichung des umschlossenen PST-Speicheranbieters auf, damit der umschlossene PST-Speicheranbieter ordnungsgemäß heruntergefahren werden kann. Die Funktion beendet alle Sitzungsobjekte, die dem umschlossenen ANBIETER für den PST-Speicher zugeordnet sind. 
  
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



[Informationen zum Beispiel umschlossenen PST Store-Anbieter](about-the-sample-wrapped-pst-store-provider.md)
  
[Installieren des Beispielanbieters für den umschlossenen PST Store](installing-the-sample-wrapped-pst-store-provider.md)
  
[Initialisieren eines umbrochenen PST Store-Anbieters](initializing-a-wrapped-pst-store-provider.md)
  
[Anmelden bei einem umschlossenen PST Store-Anbieter](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Verwenden eines umbrochenen PST Store-Anbieters](using-a-wrapped-pst-store-provider.md)

