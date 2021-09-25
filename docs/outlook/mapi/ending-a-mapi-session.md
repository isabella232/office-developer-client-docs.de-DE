---
title: Beenden einer MAPI-Sitzung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 746b14323bfb1b75f4fd0db6ff7e6f0f6c25d0fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596504"
---
# <a name="ending-a-mapi-session"></a>Beenden einer MAPI-Sitzung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients können ihre Sitzungen als Reaktion auf die Anforderung eines Benutzers beenden, entweder unmittelbar oder nachdem alle ausgehenden Nachrichten verarbeitet wurden und wenn ein schwerwiegender Fehler auftritt. Einige Clients müssen angemeldet bleiben, damit ausstehende ausgehende Nachrichten den Transportanbieter und das Zielnachrichtensystem erreichen können. Wenn ein solcher Client eine Nachricht sendet und sich sofort abmeldet, bleibt die Nachricht möglicherweise in der ausgehenden Warteschlange, bis sich ein Benutzer wieder anmeldet und lange genug angemeldet bleibt, damit die Nachricht übertragen werden kann.
  
 **Wenn Sie Ihre Sitzung mit dem MAPI-Subsystem beenden müssen**
  
1. Brechen Sie die Registrierungen für alle Benachrichtigungen ab, indem Sie die **Unadvise-Methode** jedes registrierten Objekts aufrufen. 
    
2. Geben Sie alle geöffneten Objekte frei, indem Sie ihre [IUnknown::Release-Methoden](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) aufrufen. Zu den Arten von geöffneten Objekten gehören Empfehlungssenken, die Statustabelle, der Ordner "Postausgang", ein oder mehrere Nachrichtenspeicher und das Adressbuch. 
    
3. Rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) auf, um den Speicher für alle zwischengespeicherten Eintragsbezeichner freizugeben, z. **B. PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
4. Call [IMAPISession::Logoff](imapisession-logoff.md), setting the MAPI_LOGOFF_UI flag if you allow a user interface and the MAPI_LOGOFF_SHARED flag if you own the current shared session. **Abmelden** benachrichtigt alle anderen Clients, die die aktuelle freigegebene Sitzung verwenden, dass sie sich durch Senden einer Fehlerbenachrichtigung abmelden sollten. 
    
5. Geben Sie den Sitzungszeiger frei, indem Sie die **IUnknown::Release-Methode** der Sitzung aufrufen. 
    
6. Wenn Sie [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) während des Sitzungsstarts aufgerufen haben, um die OLE-Bibliotheken zu initialisieren, heben Sie diese jetzt auf, indem Sie [OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx)aufrufen. Nur Clients, die **OleInitialize** aufgerufen haben, müssen **OleUninitialize** aufrufen. 
    
7. Initialisieren Sie die MAPI-Bibliotheken, indem [Sie MAPIUninitialize](mapiuninitialize.md)aufrufen. Wenn Sie **OleInitialize** zu einem bestimmten Zeitpunkt aufgerufen haben, stellen Sie sicher, dass vor diesem Aufruf von **MAPIUninitialize** ein Aufruf von **OleUninitialize** erfolgt. Der Zeitpunkt ist entscheidend. Wenn der Aufruf von **OleUninitialize** dem Aufruf von **MAPIUninitialize** folgt, wird Ihr Client möglicherweise fehlerhaft beendet. 
    
8. Wenn Sie [ScInitMapiUtil](scinitmapiutil.md) während des Sitzungsstarts aufgerufen haben, um die MAPI-Hilfsprogrammbibliothek zu initialisieren, entinitialisieren Sie sie jetzt, indem Sie [DenitMapiUtil](deinitmapiutil.md)aufrufen. Nur Clients, die **ScInitMapiUtil** aufgerufen haben, müssen **DenitMapiUtil** aufrufen.
    
> [!NOTE]
> Alle geöffneten Objekte müssen vor dem Aufruf von **IMAPISession::Logoff** freigegeben werden. Objekte, die geöffnet bleiben, nachdem **Logoff** aufgerufen wurde, werden ungültig. Sie können keine Anrufe annehmen und werden möglicherweise nie freigegeben. Wenn ein Aufruf an eines dieser Objekte erfolgt, gehen Sie davon aus, dass der Aufruf fehlschlägt. 
  
 Die MAPI verfügt über keinen Mechanismus zum Löschen von DLLs während des Herunterfahrens der Sitzung. Die DLL eines Dienstanbieters kann nur gelöscht werden, wenn ein Konfigurationsclient wie die Systemsteuerung seine Nachrichtendienst-Einstiegspunktfunktion mit dem MSG_SERVICE_INSTALL-Ereignis aufruft. 
  

