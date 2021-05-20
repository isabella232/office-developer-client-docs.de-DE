---
title: Status "Inhalt synchronisieren"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438470"
---
# <a name="synchronize-contents-state"></a>Status "Inhalt synchronisieren"

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Synchronisierungsinhaltsstatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Verwandte Datenstruktur:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|In diesem Zustand:  <br/> |[Zustand „Synchronisieren“](synchronize-state.md) <br/> |
|In diesem Zustand:  <br/> |[Tabellenstatus herunterladen,](download-table-state.md) [Tabellenstatus hochladen](upload-table-state.md)oder Synchronisieren  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Zustand initiiert einen der beiden Replikationsprozesse: Das Hochladen des Inhalts der angegebenen Ordner in einem lokalen Speicher oder eine vollständige Synchronisierung. Bei einer vollständigen Synchronisierung werden die Inhalte für jeden der angegebenen Ordner zuerst hochgeladen und dann heruntergeladen. Abhängig von *den ulFlags,* die in der entsprechenden **[SYNC-Struktur](sync.md)** im vorherigen Synchronisierungsstatus festgelegt sind, initialisiert Outlook [out]-Elemente in der **SYNCCONT-Struktur,** um Informationen zu den Inhalten zur Verfügung zu stellen. 
  
Über die gleiche **SYNCCONT-Struktur** ruft der Client die Anzahl der Ordner ab, für die Inhalte hochgeladen oder heruntergeladen werden müssen. Der Client durchrundet jeden dieser Ordner, indem er den lokalen Speicher in den Status der Uploadtabelle zum Hochladen eines Ordners oder den lokalen Speicher in den Zustand der Downloadtabelle verschieben, um den Ordner herunterzuladen. 
  
Darüber hinaus ruft der Client Eintrags-IDs für die Ordner ab, die eine Replikation erfordern.
  
Wenn dieser Zustand endet, Outlook interne Informationen bereinigt. Der lokale Speicher kehrt zum Synchronisierungsstatus zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

