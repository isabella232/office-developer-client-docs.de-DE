---
title: Synchronisieren des Inhaltsstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349567"
---
# <a name="synchronize-contents-state"></a>Synchronisieren des Inhaltsstatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Status "Inhalt synchronisieren" des Replikationsstatus Computers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Status-ID:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Zugehörige Datenstruktur:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|Aus folgendem Zustand:  <br/> |[Zustand „Synchronisieren“](synchronize-state.md) <br/> |
|Zu folgendem Status:  <br/> |[Tabellenstatus herunterladen](download-table-state.md), [Tabellenstatus hochladen](upload-table-state.md)oder Status Synchronisieren  <br/> |
   
> [!NOTE]
> Der Replikationsstatus Computer ist ein deterministischer Statuscomputer. Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert einen der beiden Replikationsprozesse: Hochladen der Inhalte bestimmter Ordner in einem lokalen Speicher oder eine vollständige Synchronisierung. Bei einer vollständigen Synchronisierung für jeden der angegebenen Ordner werden die Inhalte zuerst hochgeladen und dann heruntergeladen. Abhängig vom *ulFlags* -Satz in der entsprechenden **[Synchronisierungs](sync.md)** Struktur im vorherigen Synchronisierungsstatus initialisiert Outlook [out]-Elemente in der **SYNCCONT** -Struktur, um Informationen zu den Inhalten bereitzustellen. 
  
Über dieselbe **SYNCCONT** -Struktur ruft der Client die Anzahl der Ordner ab, die Inhalte hoch-oder heruntergeladen werden sollen. Der Client durchläuft jeden dieser Ordner, indem er den lokalen Speicher in den Status der hochgeladenen Tabelle verschiebt, um einen Ordner hochzuladen, oder den lokalen Speicher in den Status der Download Tabelle verschiebt, um den Ordner herunterzuladen. 
  
Darüber hinaus erhält der Client Eintrags-IDs für die Ordner, die eine Replikation erfordern.
  
Wenn dieser Status endet, bereinigt Outlook seine internen Informationen. Der lokale Speicher wird zum Synchronisierungsstatus zurückgegeben.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

