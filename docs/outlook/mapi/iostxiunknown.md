---
title: IOSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6d7de4d6c14179ddaba4e2ad907f1acc1c53b125
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431995"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Synchronisierungsmethoden bereit. Diese Schnittstelle ruft die erforderlichen Informationen ab, um lokale Änderungen an den Server-und Server Änderungen im lokalen Speicher zu replizieren.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterroraufzurufen](iostx-getlasterror.md) <br/> |Ruft erweiterte Informationen zum letzten Fehler ab.  <br/> |
|[InitSync](iostx-initsync.md) <br/> |Informiert den lokalen Speicher über die Synchronisierung, die gestartet werden soll.  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |Bereitet den lokalen Speicher für die Synchronisierung in einem bestimmten Zustand vor und ruft die erforderlichen Informationen zum Replizieren ab.  <br/> |
|[SyncEnd](iostx-syncend.md) <br/> |Beendet die Synchronisierung im aktuellen Zustand und beendet diesen Status.  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |Startet die Synchronisierung für einen Nachrichtenkopf.  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |Beendet die Synchronisierung für einen Nachrichtenkopf.  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |Legt das Ergebnis der Synchronisierung fest.  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn ein Clientordner und Ordnerinhalte in einem lokalen Speicher hochlädt oder synchronisiert, verschiebt er den lokalen Speicher von einem Status in einen anderen, wie er im Zustandsübergang-Diagramm in [über den Replikationsstatus Computer](about-the-replication-state-machine.md)dargestellt ist. Im folgenden finden Sie die Reihenfolge der Ereignisse für den Client zum Verschieben des lokalen Speichers von einem Status in einen anderen:
  
1. Der Client ruft **IOSTX:: InitSync** auf, um den lokalen Speicher zu informieren, dass die Replikation gestartet werden soll. 
    
2. Abhängig von der Replikationsrichtung und den zu replizierenden Objekten ruft der Client **IOSTX:: SyncBeg** auf, um die Replikation im entsprechenden Zustand zu starten. Outlook stellt dem Client die erforderlichen Informationen bereit, und der Client führt die Replikation aus. 
    
3. Der Client ruft **IOSTX:: SetSyncResult** auf, um das Ergebnis der Replikation zurückzugeben. 
    
4. Der Client ruft **IOSTX:: SyncEnd** auf, um die Replikation zu beenden, sodass Outlook die erforderlichen Informationen für die nachfolgende Replikation bereitstellt. 
    
Insbesondere verwendet der Client beim Herunterladen von Nachrichtenelementen **IOSTX:: SyncHdrBeg** und **IOSTX:: SyncHdrEnd** , um ein vollständiges Nachrichtenelement mit dem Nachrichtenkopf im lokalen Speicher zu aktualisieren: 
  
1. Bei **IOSTX:: SyncHdrBeg**wechselt der lokale Speicher in den Status des Download Nachrichtenkopfs. Outlook stellt dem Client anfänglich den aktuellen Nachrichtenkopf des lokalen Speichers zur Verfügung.
    
2. Der Client lädt ein vollständiges Nachrichtenelement zusammen mit dem Nachrichtenkopf herunter.
    
3. Outlook aktualisiert das Element im lokalen Speicher mit dem vollständigen Nachrichtenelement.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

