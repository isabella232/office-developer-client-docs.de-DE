---
title: Synchronisieren von Text und Formatierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435103"
---
# <a name="synchronizing-text-and-formatting"></a>Synchronisieren von Text und Formatierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die größte Herausforderung beim Senden von Rich Text Format (RTF)-Nachrichten besteht darin, den Text mit der Formatierung zu synchronisieren. Um sicherzustellen, dass Nachrichten, wenn sie am Ziel ankommen, wie ihre Ermittler vorgesehen sind und dass Text und Formatierung synchronisiert werden, stellt MAPI die [RTFSync-Funktion](rtfsync.md) zur Verwendung. **RTFSync wird** in der Regel von RTF-unterstützenden Clients aufgerufen, bevor eingehende Nachrichten angezeigt werden, und vom MAPI-Spooler, wenn Nachrichten an einen Transportanbieter heruntergeladen werden. Anrufer geben den Bereich möglicher Abweichungen an, indem sie ein oder zwei Flags an **RTFSync übergeben:**
  
- RTF_SYNC_BODY_CHANGED, um eine Änderung im Nachrichtentext anzugeben.
    
- RTF_SYNC_RTF_CHANGED, um eine Änderung der Nachrichtenformatierung anzugeben.
    
Der Synchronisierungsprozess in **RTFSync** ist eine ausgefeilte zyklische Redundanzprüfung (CrC) des Nachrichtentexts, die einige Zeichen ignoriert und andere konvertiert. Zeichen, die wahrscheinlich von Transportanbietern hinzugefügt wurden, werden ignoriert. MAPI definiert verschiedene Eigenschaften für die Arbeit mit RTF, wie in der folgenden Tabelle beschrieben. 
  
|**RTF-Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Gibt den Anfang des tatsächlichen Nachrichtentexts an.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Enthält das Ergebnis der zyklischen Redundanzüberprüfung des Nachrichtentexts.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Enthält die Anzahl der Zeichen in **PR_RTF_SYNC_BODY_CRC**.  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |Wird auf TRUE festgelegt, wenn der Nachrichtentext und die Formatierung synchronisiert wurden.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Enthält die Anzahl der Nicht-Whitespace-Zeichen, die dem Nachrichtentext voraus waren.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Enthält die Anzahl der Nicht-Whitespace-Zeichen, die dem Nachrichtentext nachgestellt werden.  <br/> |
   

