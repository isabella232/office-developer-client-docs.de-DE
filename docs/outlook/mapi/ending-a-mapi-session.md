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
  
Clients können Ihre Sitzungen als Reaktion auf die Anforderung eines Benutzers beenden, entweder sofort oder nachdem alle ausgehenden Nachrichten verarbeitet wurden und wenn ein kritischer Fehler auftritt. Einige Clients müssen angemeldet bleiben, damit Ausstehende ausgehende Nachrichten den Transportanbieter und das Ziel Messagingsystem erreichen können. Wenn ein solcher Client eine Nachricht sendet und sofort abmeldet, verbleibt die Nachricht möglicherweise in der ausgehenden Warteschlange, bis ein Benutzer sich wieder anmeldet und lange genug angemeldet bleibt, damit die Nachricht übertragen werden kann.
  
 **Wenn Sie Ihre Sitzung mit dem MAPI-Subsystem beenden müssen**
  
1. Brechen Sie die Registrierungen für alle Benachrichtigungen ab, **** indem Sie die Unadvise-Methode jedes registrierten Objekts aufrufen. 
    
2. Geben Sie alle geöffneten Objekte frei, indem Sie Ihre [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) -Methoden aufrufen. Zu den Typen offener Objekte können Advise-Senken, die Statustabelle, der Ausgangsordner, ein oder mehrere Nachrichtenspeicher und das Adressbuch hinzugefügt werden. 
    
3. Rufen Sie [mapifreebufferfreigegeben](mapifreebuffer.md) auf, um den Arbeitsspeicher für alle zwischengespeicherten Eintragsbezeichner wie **PR_IPM_SUBTREE_ENTRYID** ([pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md)) freizugeben.
    
4. Rufen Sie [IMAPISession:: Logoff](imapisession-logoff.md)auf, indem Sie das MAPI_LOGOFF_UI-Flag festlegen, wenn Sie eine Benutzeroberfläche zulassen, und das MAPI_LOGOFF_SHARED-Flag, wenn Sie die aktuelle freigegebene Sitzung besitzen. **Abmelden** benachrichtigt alle anderen Clients, die die aktuelle freigegebene Sitzung verwenden, die Sie abmelden sollten, indem Sie eine Fehlerbenachrichtigung senden. 
    
5. Lassen Sie den Sitzungs Zeiger Los, indem Sie die **IUnknown:: Release** -Methode der Sitzung aufrufen. 
    
6. Wenn Sie [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) während des Starts der Sitzung aufgerufen haben, um die OLE-Bibliotheken zu initialisieren, können Sie die Initialisierung jetzt durch Aufrufen von [OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx)auffordern. Nur Clients, die **OleInitialize** aufgerufen haben, müssen **OleUninitialize**aufrufen. 
    
7. Deinitialisieren Sie die MAPI-Bibliotheken, indem Sie [MAPIUninitialize](mapiuninitialize.md)aufrufen. Wenn Sie **OleInitialize** an einem bestimmten Punkt aufgerufen haben, stellen Sie sicher, dass ein Aufruf von **OleUninitialize** vor diesem Aufruf von **MAPIUninitialize**erfolgt. Das Timing ist entscheidend. Wenn der Aufruf von **OleUninitialize** dem Aufruf von **MAPIUninitialize**folgt, wird der Client möglicherweise unordnungs gemäß beendet. 
    
8. Wenn Sie während des Sitzungsstarts [ScInitMapiUtil](scinitmapiutil.md) aufgerufen haben, um die MAPI-Dienstprogrammbibliothek zu initialisieren, müssen Sie die Initialisierung jetzt durch Aufrufen von [DeinitMapiUtil](deinitmapiutil.md)auffordern. Nur Clients, die **ScInitMapiUtil** aufgerufen haben, müssen **DeinitMapiUtil**aufrufen.
    
> [!NOTE]
> Alle geöffneten Objekte müssen vor dem Aufruf von **IMAPISession:: Logoff**freigegeben werden. Objekte, die nach der **Abmeldung** geöffnet bleiben, werden ungültig. Sie können keine Anrufe annehmen und werden möglicherweise nie freigegeben. Wenn ein Aufruf an eines dieser Objekte erfolgt, erwarten Sie, dass der Aufruf fehlschlägt. 
  
 MAPI hat keinen Mechanismus zum Löschen von DLLs während des Sitzungs Ablaufs. DLL eines Dienstanbieters kann nur gelöscht werden, wenn ein Konfigurations Client, wie die Systemsteuerung, seine Nachrichtendienst-Einstiegspunktfunktion mit dem MSG_SERVICE_INSTALL-Ereignis aufruft. 
  

