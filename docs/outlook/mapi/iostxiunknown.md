---
title: IOSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9fd43e4a0e01e774231ddd250a5f20df175f6981
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556336"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Synchronisierungsmethoden bereit. Diese Schnittstelle ruft die erforderlichen Informationen ab, um lokale Änderungen auf dem Server und Serveränderungen im lokalen Speicher zu replizieren.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](iostx-getlasterror.md) <br/> |Ruft erweiterte Informationen zum letzten Fehler ab.  <br/> |
|[InitSync](iostx-initsync.md) <br/> |Informiert den lokalen Speicher, dass die Synchronisierung gestartet werden soll.  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |Bereitet den lokalen Speicher für die Synchronisierung in einem bestimmten Zustand vor und ruft die erforderlichen Informationen zum Replizieren ab.  <br/> |
|[SyncEnd](iostx-syncend.md) <br/> |Beendet die Synchronisierung im aktuellen Zustand und beendet diesen Zustand.  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |Startet die Synchronisierung für einen Nachrichtenkopf.  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |Beendet die Synchronisierung für einen Nachrichtenkopf.  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |Legt das Ergebnis der Synchronisierung fest.  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn ein Client Ordner und Ordnerinhalte in einem lokalen Speicher hochlädt oder synchronisiert, wird der lokale Speicher von einem Zustand in einen anderen verschoben, wie im Zustandsübergangsdiagramm unter ["Informationen zum Replikationsstatuscomputer"](about-the-replication-state-machine.md)dargestellt. Es folgt die Reihenfolge der Ereignisse, in der der Client den lokalen Speicher von einem Zustand in einen anderen verschieben kann:
  
1. Der Client ruft **IOSTX::InitSync** auf, um den lokalen Speicher darüber zu informieren, dass die Replikation gestartet werden soll. 
    
2. Abhängig von der Replikationsrichtung und den zu replizierenden Objekten ruft der Client **IOSTX::SyncBeg** auf, um die Replikation im entsprechenden Zustand zu starten. Outlook stellt dem Client die erforderlichen Informationen bereit, und der Client führt die Replikation aus. 
    
3. Der Client ruft **IOSTX::SetSyncResult** auf, um das Ergebnis der Replikation zurückzugeben. 
    
4. Der Client ruft **IOSTX::SyncEnd** auf, um die Replikation zu beenden, und stellt Outlook die erforderlichen Informationen für die nachfolgende Replikation bereit. 
    
Insbesondere beim Herunterladen von Nachrichtenelementen verwendet der Client **IOSTX::SyncHdrBeg** und **IOSTX::SyncHdrEnd,** um ein vollständiges Nachrichtenelement mit dem Nachrichtenheader im lokalen Speicher zu aktualisieren: 
  
1. Bei **IOSTX::SyncHdrBeg** wechselt der lokale Speicher in den Headerstatus der Downloadnachricht. Outlook stellt dem Client zunächst den aktuellen Nachrichtenheader im lokalen Speicher bereit.
    
2. Der Client lädt ein vollständiges Nachrichtenelement zusammen mit dem Nachrichtenkopf herunter.
    
3. Outlook aktualisiert das Element im lokalen Speicher mit dem vollständigen Nachrichtenelement.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

