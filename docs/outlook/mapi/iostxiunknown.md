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
ms.openlocfilehash: 9c9252e83ce212bacf185d0eedb75d30617f9807
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581748"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Stellt Synchronisierungsmethoden bereit. Diese Schnittstelle ruft die erforderlichen Informationen zum Replizieren von lokaler Änderungen auf den Server und Server Änderungen an den lokalen Speicher ab.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](iostx-getlasterror.md) <br/> |Ruft Informationen über den letzten Fehler erweitert.  <br/> |
|[InitSync](iostx-initsync.md) <br/> |Informiert dem lokalen Speicher, dass Synchronisierung gestartet.  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |Bereitet den lokalen Speicher für die Synchronisierung in einen bestimmten Status und die erforderliche Informationen zum Replizieren von abgerufen.  <br/> |
|[SyncEnd](iostx-syncend.md) <br/> |Synchronisierung in den aktuellen Status beendet und diesen Status beendet.  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |Synchronisierung für ein Nachrichtenkopf gestartet.  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |Synchronisierung für ein Nachrichtenkopf endet.  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |Das Ergebnis der Synchronisierung festgelegt.  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn ein Client hochgeladen oder Ordner und Ordnerinhalte in einem lokalen Speicher synchronisiert, verschiebt es den lokalen Speicher von einem Zustand zu einem anderen wie in der Statusübergangsdiagramm in [Über die Replikation Zustandsautomat](about-the-replication-state-machine.md)dargestellt. Es folgt der Reihenfolge von Ereignissen für den Client auf den lokalen Speicher von einem Zustand in einen anderen verschieben:
  
1. Der Client ruft **IOSTX::InitSync** , um dem lokalen Speicher zu informieren, dass die Replikation zu starten. 
    
2. Abhängig von der Richtung der Replikation und die Objekte repliziert werden ruft der Client **IOSTX::SyncBeg** , um die Replikation in den entsprechenden Status zu beginnen. Outlook bietet des Clients die erforderliche Informationen und der Client führt die Replikation. 
    
3. Der Client ruft **IOSTX::SetSyncResult** , um das Ergebnis der Replikation zurückzugeben. 
    
4. Der Client ruft **IOSTX::SyncEnd** zum Beenden der Replikations Outlook die erforderliche Informationen für die nachfolgende Replikation bereitstellen. 
    
Insbesondere verwendet beim Download von Nachrichtenelemente der Client **IOSTX::SyncHdrBeg** und **IOSTX::SyncHdrEnd** so aktualisieren Sie eine vollständige e-Mail-Element mit der Nachrichtenkopf auf dem lokalen Speicher: 
  
1. Bei **IOSTX::SyncHdrBeg**Speichern der lokalen Kopie Übergänge in den Downloadstatus der Nachricht Kopfzeile. Outlook ermöglicht dem Client mit der aktuellen Nachrichtenkopf anfangs auf dem lokalen Speicher.
    
2. Der Client finden Sie eine vollständige e-Mail-Element zusammen mit der Nachrichtenkopf downloads.
    
3. Outlook aktualisiert das Element auf dem lokalen Speicher mit dem vollständigen Nachrichtenelement.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

