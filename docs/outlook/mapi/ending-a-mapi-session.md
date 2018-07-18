---
title: Beenden einer MAPI-Sitzung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 844880e5a1e40b51ece30baafd969372e7d43121
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791628"
---
# <a name="ending-a-mapi-session"></a>Beenden einer MAPI-Sitzung

  
  
**Betrifft**: Outlook 
  
Clients können beenden, deren Sitzung als Antwort auf Anforderung eines Benutzers, entweder sofort oder erst, nachdem alle ausgehende Nachrichten verarbeitet wurden, und wenn ein schwerwiegender Fehler auftritt. Einige Clients müssen bleiben angemeldet damit ausstehende ausgehende Nachrichten der Adressbuchhierarchie erreicht werden kann und das Ziel messaging-System. Wenn solche ein Client eine Nachricht sendet und sofort abmeldet, bleiben die Nachricht in der ausgehenden Warteschlange, bis ein Benutzer Back anmeldet und bleibt angemeldet sind lange genug für die Nachricht zu übermitteln.
  
 **Wenn Sie die Sitzung mit MAPI-Subsystems beendet müssen**
  
1. Brechen Sie für alle Benachrichtigungen für Registrierungen durch Aufrufen der **Unadvise** -Methode jedes registrierten Objekts ab. 
    
2. Lassen Sie alle geöffneten Objekte durch ihre [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) -Methoden aufrufen. Die open-Objekte können Typen advise-senken, die Statustabelle, der Ordner Postausgang, eine oder mehrere Nachrichtenspeicher und im Adressbuch. 
    
3. Rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) , um den Speicherplatz für alle zwischengespeicherten Eintragsbezeichner wie **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) freizugeben.
    
4. Rufen Sie [IMAPISession::Logoff](imapisession-logoff.md), das MAPI_LOGOFF_UI-Flag festlegen, wenn Sie eine Benutzeroberfläche und das Flag MAPI_LOGOFF_SHARED zulassen, wenn Sie die aktuelle freigegebene Sitzung besitzen. **Abmelden** benachrichtigt alle anderen Clients mit der aktuellen freigegebenen Sitzung, die durch Senden einer Benachrichtigung Fehler Abmelden sollte. 
    
5. Version der Sitzung Zeiger durch Aufrufen der Sitzung **IUnknown** -Methode. 
    
6. Wenn Sie während der Sitzung zum Starten des OLE-Bibliotheken initialisieren [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) aufgerufen, initialisieren sie nun durch Aufrufen von [OleUninitialize](http://msdn.microsoft.com/en-us/library/ms691326%28VS.85%29.aspx). Nur Clients, die **OleInitialize** aufgerufen haben, müssen **OleUninitialize**aufrufen. 
    
7. Aufhebung der Initialisierung der MAPI-Bibliotheken durch Aufrufen von [MAPIUninitialize](mapiuninitialize.md). Wenn Sie zu einem bestimmten Zeitpunkt **OleInitialize** aufgerufen wird, stellen Sie sicher, dass ein Aufruf von **OleUninitialize** vor dieser Aufruf **MAPIUninitialize**auftritt. Der Zeitpunkt ist entscheidend. Wenn der Aufruf von **OleUninitialize** den Anruf an **MAPIUninitialize**folgt, möglicherweise Netzwerkkkabel Ihrer Client beenden. 
    
8. Wenn Sie während des Starts beim Initialisieren der MAPI-Dienstprogrammbibliothek Sitzung [ScInitMapiUtil](scinitmapiutil.md) aufgerufen, initialisieren sie nun durch Aufrufen von [DeinitMapiUtil](deinitmapiutil.md). Nur Clients, die **ScInitMapiUtil** aufgerufen haben, müssen **DeinitMapiUtil**aufrufen.
    
> [!NOTE]
> Alle geöffneten Objekte müssen vor dem Aufruf von **IMAPISession::Logoff**freigegeben werden. Objekte, die nach dem Aufruf von **Abmelden** geöffnet bleiben ungültig; Sie können keine Anrufe annehmen und möglicherweise nie freigegeben werden. Wenn eines dieser Objekte aufgerufen wird, erwarten, dass des Aufrufs fehlschlägt. 
  
 MAPI verfügt über keinen Mechanismus zum Löschen von DLLs während des Herunterfahrens Sitzung. Ein Dienst, den Anbieter DLL nur gelöscht werden kann, wenn ein Client Konfiguration wie die-Systemsteuerung seine Nachricht Service Entry Point-Funktion mit dem MSG_SERVICE_INSTALL-Ereignis aufruft. 
  

