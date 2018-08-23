---
title: Status „Inhalts synchronisieren“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a2bdbeb39cce1e62569f364875c3828cdd530c63
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577247"
---
# <a name="synchronize-contents-state"></a>Status „Inhalts synchronisieren“

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was geschieht, während die Synchronize Inhalt Zustand des Computers Zustand Replikation. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|State-ID:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Verwandte-Datenstruktur:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Synchronisieren von Zustand](synchronize-state.md) <br/> |
|Diesen Status:  <br/> |[Tabelle Zustand herunterladen](download-table-state.md), [Hochladen Tabelle Zustand](upload-table-state.md), oder Zustand synchronisieren  <br/> |
   
> [!NOTE]
> Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat. Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben. 
  
## <a name="description"></a>Beschreibung

Dieser Status wird initiiert einen der beiden Replikationsprozesse: Hochladen der Inhalt der Ordner auf einem lokalen Speicher oder eine vollständige Synchronisierung angegeben. In eine vollständige Synchronisierung, für die einzelnen von den angegebenen Ordnern Inhalt zuerst hochgeladen und dann heruntergeladen. Synchronisieren je nach den *UlFlags* legen Sie in der entsprechenden **[SYNC](sync.md)** -Struktur in der vorherigen Zustand, Outlook initialisiert [out] Member in der Struktur **SYNCCONT** um Informationen zu den Inhalt bereitzustellen. 
  
Über die gleiche **SYNCCONT** -Struktur erhält der Client die Anzahl der Ordner, die Inhalt besitzen, hoch- oder heruntergeladen werden. Der Client wird jeder dieser Ordner durchlaufen werden durch den lokalen Speicher auf den Status des Upload-Tabelle einen Ordner hochladen verschieben oder verschieben den lokalen Speicher in den Downloadstatus Tabelle, um den Ordner herunterzuladen. 
  
Darüber hinaus erhält der Client Eintrags-IDs für die Ordner Replikation erfordern.
  
Wenn dieser Status beendet wird, bereinigt Outlook internen Informationen. Der lokale Speicher zurück in den Synchronize-Zustand.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCHRONISIERUNGSSTATUS](syncstate.md)

