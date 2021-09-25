---
title: Synchronisieren des Inhaltsstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 94707184461794fd64af05a9f19b109c60e9af5f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624083"
---
# <a name="synchronize-contents-state"></a>Synchronisieren des Inhaltsstatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was beim Synchronisieren des Inhaltsstatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Verwandte Datenstruktur:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Zustand „Synchronisieren“](synchronize-state.md) <br/> |
|In diesem Zustand:  <br/> |[Tabellenstatus herunterladen,](download-table-state.md) [Tabellenstatus hochladen](upload-table-state.md)oder Status synchronisieren  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Bundesland in einen anderen wechselt, muss schließlich von letzterem zum ersten Zurückkehren zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert einen der beiden Replikationsprozesse: das Hochladen des Inhalts der angegebenen Ordner in einen lokalen Speicher oder eine vollständige Synchronisierung. Bei einer vollständigen Synchronisierung wird der Inhalt für jeden der angegebenen Ordner zuerst hochgeladen und dann heruntergeladen. Abhängig von den *ulFlags,* die in der entsprechenden **[SYNC-Struktur](sync.md)** im vorherigen Synchronisierungsstatus festgelegt sind, initialisiert Outlook [out]-Elemente in der **SYNCCONT-Struktur,** um Informationen über den Inhalt bereitzustellen. 
  
Über dieselbe **SYNCCONT-Struktur** ruft der Client die Anzahl der Ordner ab, deren Inhalt hochgeladen oder heruntergeladen werden soll. Der Client durchläuft jeden dieser Ordner, indem er den lokalen Speicher in den Uploadtabellenstatus verschiebt, um einen Ordner hochzuladen, oder den lokalen Speicher in den Downloadtabellenstatus verschieben, um den Ordner herunterzuladen. 
  
Darüber hinaus ruft der Client Eintrags-IDs für die Ordner ab, die eine Replikation erfordern.
  
Wenn dieser Zustand endet, bereinigt Outlook die internen Informationen. Der lokale Speicher kehrt in den Synchronisierungsstatus zurück.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

