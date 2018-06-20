---
title: Synchronisieren von Inhalt Zustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 216691f2c1f94d658a5aa968d6a19148a9b3c06a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795688"
---
# <a name="synchronize-contents-state"></a>Synchronisieren von Inhalt Zustand

  
  
**Betrifft**: Outlook 
  
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



[Über die API-Replikation](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen zu den Replikationsstatus Computer](about-the-replication-state-machine.md)
  
[SYNCHRONISIERUNGSSTATUS](syncstate.md)

