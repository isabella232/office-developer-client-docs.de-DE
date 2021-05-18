---
title: Beenden einer MAPI-Sitzung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 74c2a7247df02570761247a9e4a6fae378f37312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287153"
---
# <a name="ending-a-mapi-session"></a>Beenden einer MAPI-Sitzung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients können ihre Sitzungen als Reaktion auf die Anforderung eines Benutzers beenden, entweder sofort oder nachdem alle ausgehenden Nachrichten verarbeitet wurden und wenn ein kritischer Fehler auftritt. Einige Clients müssen angemeldet bleiben, damit ausstehende ausgehende Nachrichten den Transportanbieter und das Zielnachrichtensystem erreichen können. Wenn ein solcher Client eine Nachricht sendet und sich sofort abmeldet, bleibt die Nachricht möglicherweise in der ausgehenden Warteschlange, bis sich ein Benutzer anmeldet und lange genug angemeldet bleibt, damit die Nachricht übermittelt wird.
  
 **Wenn Sie Ihre Sitzung mit dem MAPI-Subsystem beenden müssen**
  
1. Brechen Sie die Registrierungen für alle Benachrichtigungen ab, indem Sie die **Unadvise-Methode** jedes registrierten Objekts aufrufen. 
    
2. Geben Sie alle geöffneten Objekte frei, indem Sie ihre [IUnknown::Release-Methoden](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) aufrufen. Die Arten von geöffneten Objekten können Ratensenken, die Statustabelle, den Ordner "Posteingang", einen oder mehrere Nachrichtenspeicher und das Adressbuch enthalten. 
    
3. Rufen [Sie MAPIFreeBuffer auf,](mapifreebuffer.md) um den Arbeitsspeicher für alle zwischengespeicherten Eintragsbezeichner frei zu machen, z. B. **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
4. Rufen [Sie IMAPISession::Logoff](imapisession-logoff.md)auf, und setzen Sie das MAPI_LOGOFF_UI,wenn Sie eine Benutzeroberfläche und das MAPI_LOGOFF_SHARED zulassen, wenn Sie der Besitz der aktuellen freigegebenen Sitzung sind. **Logoff** benachrichtigt alle anderen Clients, die die aktuelle freigegebene Sitzung verwenden, dass sie sich abmelden sollten, indem sie eine Fehlerbenachrichtigung senden. 
    
5. Geben Sie den Sitzungszeiger frei, indem Sie die **IUnknown::Release-Methode der Sitzung** aufrufen. 
    
6. Wenn Sie [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) während des Sitzungsstarts aufgerufen haben, um die OLE-Bibliotheken zu initialisieren, müssen Sie die Initialisierung jetzt durch Aufrufen von [OleUninitialize beenden.](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx) Nur Clients mit dem Namen **OleInitialize** müssen **OleUninitialize aufrufen.** 
    
7. Uninitialize the MAPI libraries by calling [MAPIUninitialize](mapiuninitialize.md). Wenn Sie **OleInitialize** zu einem bestimmten Zeitpunkt aufgerufen haben, stellen Sie sicher, dass vor diesem Aufruf von **MAPIUninitialize** ein Aufruf von **OleUninitialize** erfolgt. Der Zeitpunkt ist entscheidend. Wenn der Aufruf von **OleUninitialize** dem Aufruf von **MAPIUninitialize** folgt, wird ihr Client möglicherweise unracefully beendet. 
    
8. Wenn Sie [ScInitMapiUtil](scinitmapiutil.md) während des Sitzungsstarts aufgerufen haben, um die MAPI-Hilfsbibliothek zu initialisieren, müssen Sie die Initialisierung jetzt durch Aufrufen von [DeinitMapiUtil auf deinitialisieren.](deinitmapiutil.md) Nur Clients, die **ScInitMapiUtil aufgerufen haben,** müssen **DeinitMapiUtil aufrufen.**
    
> [!NOTE]
> Alle geöffneten Objekte müssen vor dem Aufruf von **IMAPISession::Logoff freigegeben werden.** Objekte, die nach dem Aufgerufen von **Logoff** geöffnet bleiben, werden ungültig. Sie können keine Anrufe annehmen und werden möglicherweise niemals frei. Wenn ein Aufruf an eines dieser Objekte erfolgt, erwarten Sie, dass der Aufruf fehlschlägt. 
  
 MAPI verfügt über keinen Mechanismus zum Löschen von DLLs während des Sitzungsabschaltvorgangs. Die DLL eines Dienstanbieters kann nur gelöscht werden, wenn ein Konfigurationsclient wie die Systemsteuerung seine Nachrichtendienst-Einstiegspunktfunktion mit dem MSG_SERVICE_INSTALL aufruft. 
  

