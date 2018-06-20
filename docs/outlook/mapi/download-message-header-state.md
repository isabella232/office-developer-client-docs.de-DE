---
title: Downloadstatus der Nachricht-Header
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7407b6606634ecc0151f582e4481ecbff5e7dc57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791574"
---
# <a name="download-message-header-state"></a>Downloadstatus der Nachricht-Header

  
  
**Betrifft**: Outlook 
  
 In diesem Thema wird beschrieben, was geschieht, während die Nachricht Header-Downloadstatus von der Replikation Zustandsautomat. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|State-ID:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Verwandte-Datenstruktur:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Leerlauf](idle-state.md) <br/> |
|Diesen Status:  <br/> |Leerlauf  <br/> |
   
> [!NOTE]
> Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat. Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben. 
  
## <a name="description"></a>Beschreibung

Während dieser Status aktualisiert den Client die Kopfzeile einer Nachricht in einem lokalen Speicher. Der lokale Speicher gibt diesen Zustand bei **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** und wird beendet, wenn **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** aufgerufen wird. Während dieser Zustand initialisiert Outlook Mitglieder der zugeordneten **HDRSYNC** -Datenstruktur mit Informationen über die Kopfzeile einer Nachricht. Der Client zunächst das vollständige e-Mail-Element vom Server heruntergeladen und aktualisiert anschließend die Kopfzeile des Nachrichtenelements lokal. 
  
Am Ende des [v2], wird der Client die Ergebnisse herunterladen. In den Leerlauf gibt der lokale Speicher zurück.
  
## <a name="see-also"></a>Siehe auch



[Über die API-Replikation](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen zu den Replikationsstatus Computer](about-the-replication-state-machine.md)
  
[SYNCHRONISIERUNGSSTATUS](syncstate.md)

